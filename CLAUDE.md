# 울산울주세계산악영화제(UMFF) 출판물 번역기

UMFF 2026 프로그램북 콘텐츠(시놉시스·프로그램 노트·바이오 등)의 **한↔영 초벌 번역** 웹 도구.
정적 단일 페이지 + 브라우저에서 Anthropic API 직접 호출 + GitHub Pages 배포.

---

## 1. 아키텍처 & 파일 구조

빌드 단계 없음. 순수 HTML/CSS/JS 단일 페이지.

```
index.html              앱 본체 (UI + 글로서리 로더 + 프롬프트 빌더 + API 호출 + 스트림 파서)
glossary/
  proper-nouns.csv      고정 명칭 한↔영 대조표 (구분,국문,영문,비고)
  festivals-schools.csv 해외 영화제·학교 (본문에 등장할 때만 사용)
  notation-rules.md     표기 규칙
  style_guide_v2.md     번역 문체 가이드 (규칙 1~31, 길이 기준)
  tm-examples.md        유형×방향별 few-shot 예시 — 시스템 프롬프트에 주입
  translation-memory.csv  2025 확정 원고 97편 코퍼스 (전체 주입 X · tm-examples.md의 출처)
CLAUDE.md               이 파일
```

- 글로서리는 `fetch('./glossary/...')`로 런타임 로드한다. 실패 시 `index.html` 내장 폴백(`EMBEDDED_*`)으로 동작한다.

---

## 2. 실행 / 배포

```bash
# 로컬 개발 — 반드시 서버로 띄운다 (file://는 글로서리 fetch가 막혀 폴백으로만 동작)
python3 -m http.server 8000      # http://localhost:8000

# 배포 — main 브랜치 푸시 → GitHub Pages 자동 반영
```

---

## 3. 번역 역할 & 핵심 원칙

### 출처 우선순위 (충돌 시 위에서부터)
1. **proper-nouns.csv / festivals-schools.csv** — 고정 명칭의 확정 표기
2. **notation-rules.md** — 표기 규칙
3. **style_guide_v2.md** — 문장 구조·문체·번역 방향

### 절대 원칙
- **고정 명칭은 글로서리 먼저.** 글로서리에 있으면 그 표기 그대로. 더 자연스러워 보여도 바꾸지 않는다.
- **글로서리에 없으면** 원문 표기를 그대로 사용한다.
- **의미·정보를 임의로 더하거나 빼지 않는다.**

---

## 4. 글로서리

CSV 형식: `구분,국문,영문,비고` (UTF-8로 저장).

- `proper-nouns.csv` 구분값: 영화제명 · 인명 · 장소 · 섹션 · 시상 · 프로그램 · 용어 · 국가 · 등급 · 자막 · 월 · 가격 · 주소 · 전화번호.
- `festivals-schools.csv` 구분값: 해외영화제 · 해외학교. **본문에 해당 명칭이 나올 때만** 시스템 프롬프트에 주입(평소엔 토큰 절약).

---

## 5. 출력 형식 (시스템 프롬프트 ↔ 파서 계약)

모델 출력은 아래 구분자를 **그대로** 사용한다. `parseResponse()`가 이 구분자로 섹션을 추출한다.

```
[SECTION:번역문]
번역 결과 전문. 글로서리에 없는 고유명사는 원문 그대로 사용.
[/SECTION]

[SECTION:길이]
유형 / 원문 N자 / 번역문 N자 · N단어 / 한도 대비 (초과 시 표시)
[/SECTION]
```

구분자를 바꾸면 `buildSystemPrompt()`와 `parseResponse()`를 **동시에** 수정한다.

---

## 6. 코딩 규칙 & 주의사항

**API 호출**
- 엔드포인트: `POST https://api.anthropic.com/v1/messages`, 스트리밍(`stream: true`).
- 헤더: `x-api-key`, `anthropic-version: 2023-06-01`, `anthropic-beta: prompt-caching-2024-07-31`, `anthropic-dangerous-direct-browser-access: true`.
- 시스템 프롬프트는 **정적 블록 + 동적 블록 두 개**로 분리한다.
  - 블록 1 (정적): 역할·원칙·글로서리·스타일가이드·예시·출력형식 → `cache_control: { type: 'ephemeral', ttl: '1h' }` 적용 (캐시 지속시간 1시간)
  - 블록 2 (동적): 번역 방향·유형·길이 기준 → cache_control 없음
  - **순서가 핵심**: 정적 블록이 먼저여야 방향/유형이 바뀌어도 캐시가 유지된다.
- 모델: `claude-sonnet-5`(기본) / `claude-opus-4-8`(고품질). 모델 ID·가격은 변동되므로 확인 후 `MODEL_CONFIG` 갱신.
- `max_tokens: 8000`.

**보안**
- API 키는 `localStorage('umff_api_key')`에만 저장. 코드·저장소에 하드코딩하거나 커밋하지 않는다.

**일관성**
- 글로서리 CSV/MD를 고치면 `index.html` 내장 폴백(`EMBEDDED_*`)도 같이 갱신한다.
- CSV를 코드로 읽을 일이 있으면 UTF-8 BOM 대비해 `utf-8-sig`로 읽는다.

**하지 말 것**
- 고정 명칭을 글로서리 조회 없이 임의 번역.
- 길이 한도를 맞추려 원문 내용 누락.
- 글로서리 오타를 임의 교정(조직위 확정 전).
