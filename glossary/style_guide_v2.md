# UMFF 프로그램북 번역 스타일 가이드 (v2)
**울산울주세계산악영화제 2026 · 작년(2025) 확정 원고 기반**

이 문서는 AI 번역 모델이 초벌 번역 시 참조하는 스타일 가이드다.
규칙은 2025년 확정 원고 97편 전수 분석에서 도출했으며,
표기법은 조직위 「표기법 주의사항」 시트(이하 **표기 시트**)를 따른다.
확인되지 않은 추정은 포함하지 않았다.

> **v2 개정 요지** — 표기 시트와의 충돌·누락을 반영했다.
> 따옴표 규칙(규칙 8)을 시트 기준으로 수정, 영문 제목 이탤릭 표기 명시(규칙 11·22),
> 6장(표기법 세칙) 신설, 0장(출처 위계) 추가.

---

## 0. 출처 위계 (먼저 읽을 것)

번역·표기 시 참조 출처가 셋이며, 충돌하면 아래 우선순위를 따른다.

1. **표기 시트** — 표기법, 고정 명칭(섹션·시상·장소·영화제·학교), 고유명사 표기의 최우선 권위.
2. **translation_memory** (json / csv) — 작품별 인명·제목의 한↔영 대조. 시트에 없는 항목을 보조한다.
3. **본 스타일 가이드** — 문장 구조·문체·번역 방향.

> 충돌 시: **표기 시트 > translation_memory > 스타일 가이드**.
> 시트·TM에 등록된 표기와 다르게 번역할 경우 반드시 감수자가 확인한다.

---

## 1. 영→한 번역

영→한이 전체 번역량의 약 70%를 차지하며, 품질 기준이 가장 엄격하다.

---

### 1-1. 시놉시스 (영→한)

#### 규칙 1 · 관형절로 끌어당긴다

영어의 관계절과 분사구를 한국어에서는 앞으로 당긴 관형절로 변환한다.
서술어가 뒤로 미뤄지므로, 문장 전체의 무게감이 달라진다.

```
EN: Emin, in his twilight years, toils alongside his faithful horse.
KO: 황혼기에 접어든 에민은 충실한 말과 함께 묵묵히 삶을 이어간다.

EN: Pema, newly married and pregnant, tries to make the best of her new life.
KO: 결혼한 지 얼마 되지 않은 임산부 페마는 새로운 삶에 적응하려 애쓴다.

EN: The director, herself a climber, sets off to the Himalayas in her footsteps.
KO: 등반가인 감독은 그녀의 발자취를 따라 히말라야로 향한다.
```

#### 규칙 2 · 영어 단문 나열을 연결어미로 잇는다

영어가 마침표로 분리한 문장들을 한국어에서는 `~고`, `~며`, `~지만`, `~는데`, `~면서`로 이어붙인다.
반드시 모든 문장을 이어야 하는 것은 아니다. 의미 흐름이 자연스러울 때만 적용한다.

```
EN: Eventually, Hangma leaves Namsang and returns to her parents' house.
    She elopes with another man, Roydeep Shrestha, but eventually returns to Namsang
    when her family is unable to pay him compensation for her elopement.
KO: 결국 항마는 남상을 떠나 부모님의 집으로 돌아가고,
    그녀는 다른 남자 로이딥 슈레스타를 만나 떠나지만,
    가족이 배상금을 지불하지 못하자 결국 남상에게 돌아오게 되는데...

EN: Lin Cheng goes to prison for killing their father,
    while Lin Hsiang successfully becomes a licensed doctor and serves their village.
KO: 린청은 아버지를 살해한 혐의로 감옥에 가고,
    린샹은 의사 면허를 취득해 마을을 위해 헌신한다.
```

> 말줄임표는 **아래 점 3개(`...`)** 만 사용한다(표기 시트 [52]). 중간점 `···`나 유니코드 `…`는 쓰지 않는다. → 6-2 참조.

#### 규칙 3 · 현재형 시제를 유지한다

시놉시스는 영어 시제에 관계없이 한국어에서 현재형으로 서술한다.

```
EN: "Rupa and Maya (11) are best friends in a village where class discrimination..."
KO: "11살 루파와 마야는 여전히 계급 차별과 가부장제가 만연한 마을에서 가장 친한 친구다."

EN: "Sabitri takes her son Sridhar... on a coming-of-age ritual."
KO: "사비트리는 아들 스리다르를... 성인식으로 데려간다."
```

#### 규칙 4 · 등장인물 첫 소개 시 한글 이름(영문 이름)을 병기한다

외국 인명이 처음 등장할 때 한글 표기 뒤 괄호로 원문 이름을 붙인다.
이후 같은 인물이 재등장할 때는 한글 이름만 쓴다.

```
EN: "Namsang (Dayahang Rai) and his wife Hangma (Miruna Magar)"
KO: "남상(다야항 라이)과 그의 아내 항마(미루나 마가르)"

EN: "Tshiring Lhamu Lama as she mentors 17-year-old Tenzin Bhuti Gurung"
KO: "17세 소녀 텐진 부티 구룽과 그녀의 멘토인 츠히링 라무 라마"
```

인물 이름이 많지 않은 시놉시스에서는 병기를 생략해도 된다.

---

### 1-2. 프로그램 노트 (영→한)

#### 규칙 5 · 감독 본인이 쓴 노트는 1인칭을 유지한다

영어 노트에 `I`, `we`, `my`가 등장하면 한국어에서도 1인칭으로 번역한다.
한국어는 주어를 생략할 수 있으므로, 문장마다 "나는"을 반복하지 않아도 된다.

```
EN: "I hope the film will be an unshakeable, unforgettable experience for the audience."
KO: "이 영화가 관객에게 흔들림 없고 잊히지 않는 경험으로 남기를 바란다."

EN: "I was born and raised in a small town in Trentino and experienced firsthand
    the 'rispet' mentality..."
KO: "트렌티노의 작은 마을에서 나고 자라며, 때로는 비극적 결과를 낳기도 하는
    '리스페트' 정신을 몸소 겪어왔다."
```

#### 규칙 6 · 3인칭 노트에서 반복 주어를 생략한다

프로그래머가 쓴 3인칭 노트에서 "This film", "The film", 감독 이름 등이 문장마다
반복되면, 한국어에서는 첫 문장 이후 주어를 생략하고 술어만 이어간다.

```
EN: "This film documents the last traditional gold prospectors of Finnish Lapland,
    whose 150-year-old way of life is being ended by new legislation.
    It is a touching and humane portrait of their persistence."
KO: "핀란드 라플란드의 마지막 전통식 금 채굴자들을 기록한 이 영화는
    새로운 법령으로 150년간 이어져 온 생활 방식의 종말을 맞게 된 이들의
    이야기를 감동적이고 인간적으로 담아냈다."
```

#### 규칙 7 · 마지막 문장을 명사형으로 끝낼 수 있다

노트 마지막 문장을 완전한 서술문 대신 `~한 영화.`, `~이 돋보이는 애니메이션.`처럼
명사형으로 끊는 문체가 여러 작품에서 확인된다. 강제적 규칙은 아니나,
문장이 자연스럽게 수렴될 때 활용한다.

```
EN: "The film's dynamic and immersive camerawork generates a thrilling sense of velocity
    that feels almost transcendent."
KO: "역동적이고 몰입감 있는 카메라 무빙이 만들어내는 짜릿한 속도감이
    가히 환상적인 영화."

EN: "This animation, featuring a sensuous soundtrack, delicately reveals the character's
    emotions and enhances its mystical atmosphere and charm."
KO: "인물의 감정을 섬세히 드러내며 신비로운 분위기와 매력을 더하는,
    감각적인 사운드트랙이 돋보이는 애니메이션."
```

#### 규칙 8 · 강조어·의역 인용에만 작은따옴표를 쓴다 〔v2 수정〕

> **주의 — 표기 시트 [50][51]가 우선한다.** 직접 인용·대사는 국·영 모두 **큰따옴표("")** 를 유지하고,
> **작은따옴표('')는 원문을 그대로 인용하지 않는 의역 인용·강조어에만** 쓴다.
> 따라서 "영어 큰따옴표는 무조건 한국어 작은따옴표로 바꾼다"는 일반화는 **틀렸다**.
> 큰따옴표가 실제 발화·정확 인용이면 한국어에서도 큰따옴표를 유지한다.

작은따옴표가 맞는 경우(강조·개념어·의역):

```
EN: The story reveals the "cheap" and "expendable" lives of migrant workers.
KO: '싸구려'에 '소모품'이 되어버린 이주 노동자들의 삶을 드러낸다.

EN: the "rispet" mentality
KO: '리스페트' 정신
```

큰따옴표를 유지해야 하는 경우(대사·정확 인용):

```
EN: "I will climb it no matter what," he said.
KO: "무슨 일이 있어도 오르겠다"고 그는 말했다.
```

전체 따옴표·문장부호 총칙은 **6-1** 참조.

---

### 1-3. 바이오 (영→한)

#### 규칙 9 · 이름 없이 국적+직함으로 시작한다

영어 바이오가 `"X is a Danish film director and artist."`로 시작하더라도,
한국어에서는 이름(이미 위에 표기됨)을 생략하고 `"덴마크 출신의 영화감독이자 예술가로"`로 시작한다.

```
EN: "Robin Petré is a Danish film director and artist. In her work, she explores..."
KO: "덴마크 출신의 영화감독이자 예술가로 작품을 통해..."

EN: "Fidel Devkota is a Nepalese filmmaker and visual anthropologist (PhD). His work explores..."
KO: "네팔 출신 영화감독이자 시각 인류학 박사. 환경과 정치의..."

EN: "Valentin Rapp is a filmmaker and photographer based in the Alps,
    specialising in outdoor film production."
KO: "알프스를 기반으로 활동하는 아웃도어 전문 영화감독 겸 사진작가."
```

국적+직함 연결 패턴:
- `[국가] 출신의 [직함]` — 국가가 앞에 올 때
- `[국가] 기반의 [직함]` — 활동지가 앞에 올 때
- `[직함] 겸 [직함]` — 복수 역할을 이어줄 때

#### 규칙 10 · 현재형으로 경력을 서술한다

영어의 현재완료(`"has directed"`, `"has appeared"`)와 과거형을 한국어에서는
현재형(`"연출했다"`, `"활동하고 있다"`)으로 처리한다.

```
EN: "He has produced over a hundred works for institutions, TV networks..."
KO: "전 세계 기관과 방송사, 원정대, 다큐멘터리 작품을 100편 이상 제작해왔다."

EN: "She has made several documentaries on the relationship between humans, animals..."
KO: "인간과 동물, 산악 환경 간의 관계를 다룬 다수의 다큐멘터리를 제작해 왔다."
```

#### 규칙 11 · 작품명: 국문 꺾쇠 〈 〉, 영문 이탤릭 〔v2 수정〕

> **표기 시트 [4][5] 기준.** 한국어 작품명은 꺾쇠 `<작품명>`, 영어 작품명은 **이탤릭체**로 표기한다.
> 국·영문 병기 시에는 **꺾쇠 하나** 안에 한글·영문을 함께 넣는다: `<한글제목 English Title>`.

```
EN: "Her debut, Then Comes the Evening, won at Full Frame Documentary Festival..."
    (영문 본문에서는 Then Comes the Evening 을 이탤릭으로)
KO: "데뷔작 <그리고 저녁이 온다>는 풀프레임다큐멘터리영화제에서 수상하며..."

EN: "What happened on Pam Island, Walking Under Water and K2-Touching the Sky."
KO: "<팜 섬에서 벌어진 일>, <워킹 언더 워터>, <하늘을 향한 여정, K2>"

병기 예: <영원과 하루 Eternity and a Day>
```

> 저작권자가 별도 제목 표기를 요청한 경우 그 요청을 우선한다(표기 시트 [5]).

---

## 2. 한→영 번역

한→영은 전체의 약 30%이며, 이후 외부 원어민 감수를 거친다.
초벌에서는 의미 정확성과 자연스러운 영어 문장을 목표로 한다.

---

### 2-1. 시놉시스 (한→영)

#### 규칙 12 · 배경 맥락을 문두 부사구로 배치한다

한국어에서 본문 중간에 등장하거나 암묵적으로 처리된 시간·장소 맥락을,
영어에서는 문장 앞에 부사구로 명시한다.

```
KO: "6.25 전쟁으로 부모를 잃은 수지와 오목은 오빠 수철과 외가에 얹혀 산다."
EN: "During the Korean War, Su-ji and Oh-mok lose their parents
    and live off their maternal relatives with their older brother, Su-cheol."

KO: "혼자 경쟁에 밀려 살던 붉은발농게 큰손이는..."
EN: "In Suncheon Bay, Felix, a bowed fiddler crab who lives alone..."
```

#### 규칙 13 · 시간 전환에 전환사를 사용한다

한국어에서 연결어미로 처리된 시간 관계를 영어에서는 전환사로 명시한다.

자주 쓰이는 전환사: `Years later`, `Meanwhile`, `Eventually`, `After`, `Only then`

```
KO: "세월이 흐른 뒤 상류층이 된 수지는 죄책감에 오목을 찾지만..."
EN: "Years later, having risen to the upper class, she tries to find Oh-mok out of guilt..."

KO: "고아원 출신 일환과 결혼한 오목은 고생 끝에 세상을 떠나고,
    수지는 비로소 진실을 깨닫는다."
EN: "Meanwhile, Oh-mok... endures a life of hardship and eventually passes away.
    Only then does Su-ji finally come to terms with the truth."
```

#### 규칙 14 · 한국어 관형절을 영어 관계절·분사구문으로 변환한다

한국어에서 명사 앞으로 당겨진 수식절을 영어에서는 명사 뒤에 붙이는
관계절(`who`, `which`, `that`) 또는 분사구문으로 처리한다.

```
KO: "고아원 출신 일환과 결혼한 오목은..."
EN: "Oh-mok, who marries Il-hwan, an orphan, ..."

KO: "자신의 한계를 시험하고, 영혼을 치유하며, 내면의 어둠을 떨쳐내려는
    평범한 일상의 러너들"
EN: "everyday athletes testing their limits, healing souls, and expelling demons"
```

#### 규칙 15 · 현재 시제로 서술한다 (historical present)

한국어 시놉시스의 현재형을 영어에서도 현재 시제(historical present)로 유지한다.
영화 시놉시스의 국제 관례에 맞는다.

```
KO: "봉수는 가난한 농부로 딸의 혼례도 미룬 채 살아간다."
EN: "Bong-su is a farmer who has postponed his daughter's wedding due to poverty."

KO: "다슬이 전과 전혀 다른 사람이 되어버린다."
EN: "Da-seul is no longer herself."
```

#### 규칙 16 · 한국 고유 표현 처리

한국 문화 고유어는 아래 두 방식 중 하나로 처리한다. 둘 중 어느 쪽을 택하든
한 작품 내에서 일관되게 유지한다.

- **음차 유지**: 보편적으로 알려지지 않았지만 문화적 가치가 있는 단어
  `막걸리 → makgeolli`, `모모 → momo`, `달밧 → dal bhat`

- **풀어서 설명**: 영어권 독자에게 맥락이 필요한 제도·관계 표현
  `6.25 전쟁 → the Korean War`
  `외가 → maternal relatives`
  `성인식 → a coming-of-age ritual`

---

### 2-2. 프로그램 노트 (한→영)

#### 규칙 17 · 3인칭 노트는 "This film" 또는 "The film"으로 시작한다

프로그래머가 쓴 3인칭 노트의 첫 문장은 대부분 `"This film..."` 또는
`"The film..."` 패턴으로 시작한다.

```
KO: "감독의 장기인 슬랩스틱 코미디와 웃음기 없는 표정은... 다시 한번 빛을 발한다."
EN: "The director's trademark slapstick comedy and stone-faced expression shine once more..."

KO: "<걸 클라이머>는 에밀리 해링턴의 24시간 엘 캐피탄 등반을 따라가는 작품이다."
EN: "Girl Climber follows Emily Harrington's bold 24-hour ascent of El Capitan..."
    (영문에서 Girl Climber 는 이탤릭)
```

#### 규칙 18 · 1인칭 노트는 1인칭을 유지한다

감독 본인이 쓴 노트의 `나`, `우리`는 영어에서 `I`, `we`로 유지한다.
한국어에서 주어가 생략된 경우에도 문맥을 파악해 1인칭 주어를 명시한다.

```
KO: "나에게 있는 문제점들은 무엇일까.
    이런 부정적인 생각의 굴레에서 벗어나기 위해 다큐를 찍기 시작했다."
EN: "I started filming this documentary to confront my own problems
    and escape the cycle of negative thoughts."

KO: "조상의 뿌리를 따라가는 베넷의 여정을 보며 관객들이 가능성의 불씨를 느끼길 바란다."
EN: "We hope audiences feel the spark of possibility as they watch Bennett's journey..."
```

#### 규칙 19 · 한국어 긴 복문을 영어에서 나눈다

한국어에서 연결어미로 이어진 한 문장이 지나치게 길어지면,
영어에서 2~3개 문장으로 분리한다.

```
KO: "핀란드 라플란드의 마지막 전통식 금 채굴자들을 기록한 이 영화는
    새로운 법령으로 150년간 이어져 온 생활 방식의 종말을 맞게 된
    이들의 이야기를 감동적이고 인간적으로 담아냈다.
    정말 아이러니한 것은, 새로운 기술에 필요한 광물을 얻기 위해
    다국적 대기업들이 환경에 영향을 끼치는 대규모 채굴에 착수하는 것을
    정부가 허용하고 있다는 점이다."
EN: "This film documents the last traditional gold prospectors of Finnish Lapland,
    whose 150-year-old way of life is being ended by new legislation.
    It is a touching and humane portrait of their persistence.
    The great irony is that the government simultaneously allows large multinational
    companies to establish vast, environmentally impactful mines nearby,
    seeking minerals for new technologies."
```

---

### 2-3. 바이오 (한→영)

#### 규칙 20 · 이름을 주어로 시작한다

영→한과 반대로, 한→영 바이오는 감독의 이름을 주어로 첫 문장을 시작한다.

```
KO: "1982년 <꼬방동네 사람들>로 데뷔해..."
EN: "Bae Chang-ho made his directorial debut with People in the Slum in 1982..."

KO: "낸시 스벤센은 미국의 다큐멘터리 감독이자 프로듀서..."
EN: "Nancy Svendsen is an American documentary filmmaker, producer..."
```

#### 규칙 21 · 경력·수상을 현재완료로 서술한다

한국어의 완료된 사실(`"받았다"`, `"졸업했다"`)을 영어에서는 현재완료
(`"has won"`, `"graduated from"`)로 처리한다.

```
KO: "데뷔작 <그리고 저녁이 온다>는 풀프레임다큐멘터리영화제에서 수상하며
    아카데미시상식 예선 자격을 얻고, 50여 개의 상을 받았다."
EN: "Her debut, Then Comes the Evening, won at Full Frame Documentary Festival,
    earning OSCAR® qualification and 50+ awards."

KO: "2016년 배우로 데뷔한 이래 ... 다양한 연기 활동을 하고 있다."
EN: "Since his debut as an actor in 2016, he has appeared in
    a wide range of films and TV series..."
```

#### 규칙 22 · 한국 영화 제목은 영문 번역 제목(이탤릭)으로 표기한다 〔v2 수정〕

바이오에서 언급되는 한국 영화 제목은 **꺾쇠 없이 영문 번역 제목**으로 쓰되,
영문 본문에서는 **이탤릭체**로 표기한다(표기 시트 [4]).
공식 영문 제목이 있으면 그것을, 없으면 직역한다.

```
KO: "<꼬방동네 사람들>" → EN: People in the Slum
KO: "<적도의 꽃>"       → EN: The Flower on the Equator
KO: "<고래사냥>"        → EN: Whale Hunting
KO: "<뷰티풀 데이즈>"    → EN: Beautiful Days
```

---

## 3. 콘텐츠 유형별 길이 기준

조직위 공식 스펙이며 **공백 포함**이다. 자연스러움과 원문 뉘앙스를 해치지 않는 선에서
간결하게. **무리하게 잘라 내용을 누락하지 말 것.**

| 콘텐츠 | 국문 | 영문 글자 | 영문 단어 |
|---|---|---|---|
| 시놉시스 | 215자 | 390자 | 70단어 |
| 프로그램 노트 | 150자 | 260자 | 35단어 |
| 바이오 | 110자 | 260자 | 50단어 |

> **참고(데이터 관찰).** 2025년 확정 원고를 측정하면 바이오·프로그램 노트는 위 한도를
> 절반 이상이 초과한다(바이오 영문 중앙값 283자, 노트 영문 중앙값 38단어).
> 따라서 위 수치는 **목표 상한**으로 다루되, 원문 정보량이 많아 한도를 넘기는 경우
> **내용 누락보다 한도 초과를 우선 허용**하고 감수 단계에서 조정한다.
> 반대로 짧은 원문을 한도까지 늘려 채우지 않는다.

---

## 4. 고유명사 표기 원칙

> 고유명사·고정 명칭의 1차 권위는 **표기 시트**다. 시트에 있으면 시트를,
> 시트에 없으면 translation_memory를, 둘 다 없으면 아래 원칙을 따른다.

#### 4-1. 외국 인명 한글 표기

원어 발음에 최대한 가깝게 표기하되, 현행 외래어 표기법을 준수한다(표기 시트 [38]).
국내에 이미 익숙하게 알려진 인물은 기존 관례 표기를 따른다(표기 시트 [39]).

```
Wanda Rutkiewicz → 반다 루트키에비츠
Reinhold Messner → 라인홀트 메스너
Tshiring Lhamu Lama → 츠히링 라무 라마
Dayahang Rai → 다야항 라이
```

#### 4-2. 한국 인명 영문 로마자 표기

McCune-Reischauer 또는 Revised Romanization 중 하나를 일관되게 사용한다.
TM·시트에 등록된 표기가 있으면 그것을 따른다.

- 성과 이름은 **띄어쓰기**로 구분한다: `성 + 공백 + 이름` (예: `Bae Chang-ho`).
- 이름의 음절 사이는 **하이픈**으로 잇는다 (예: `Chang-ho`, `Hong-gil`).
- 성의 첫 글자는 대문자로 쓴다.
- **본인이 별도로 사용하는 영문명이 있으면 표준 로마자보다 우선**한다(표기 시트 [47], 예: `이순걸 → Lee Soon-geol`).

```
이정진 → Jinna Lee (관례적/본인 표기 우선)
배창호 → Bae Chang-ho
장동윤 → Jang Dong-yoon
오지인 → Oh Ji-in
엄홍길 → Um Hong-gil
```

> 한·중·일 한자식 이름은 성을 앞에, 영문식 이름은 성을 뒤에 둔다(표기 시트 [40][42]).
> 작품 속 캐릭터 이름도 같은 원칙을 따른다(표기 시트 [44]).

#### 4-3. 산 이름·지명

TM·시트에 등록된 표기를 우선한다. 없는 경우 외래어표기법을 따른다.

```
Denali → 드날리
Kumbhakarna → 쿰바카르나
Vatnajokull → 바트나요쿨
Chamonix → 샤모니
Patagonia → 파타고니아
```

---

## 5. translation_memory 활용

- 작품명, 감독명, 인명의 한↔영 대조 표기는 **시트 → TM** 순으로 조회한다.
- 등록 표기와 다르게 번역할 경우 감수자가 확인한다.
- TM·시트에 없는 신규 표기는 번역 후 추가 등록을 요청한다.
- TM은 json/csv 두 형식이 동일 내용이다. **CSV는 UTF-8 BOM이 있으므로 `utf-8-sig`로 읽을 것**(일반 `utf-8`로 읽으면 첫 컬럼명이 깨진다).

---

## 6. 표기법 세칙 (표기 시트 기반)

번역 문체와 별개로, 아래 기계적 표기 규칙은 표기 시트를 그대로 따른다.
국·영문 동일 적용이 기본이다.

### 6-1. 따옴표 (시트 [50][51][234][235])

- **대화·정확 인용** → 큰따옴표 `" "` (국·영문 동일).
- **원문 그대로가 아닌 의역 인용·강조어** → 작은따옴표 `' '` (국·영문 동일).
- 규칙 8은 이 총칙의 시놉시스·노트 적용 사례다.

### 6-2. 말줄임표 (시트 [52])

- **아래 점 3개(`...`)만** 사용한다. 중간점 `···`·유니코드 `…`는 쓰지 않는다(국·영문 동일).
- 현재 TM 데이터에 `···`·`…`·`...`가 혼재하므로 표준화 필요.

### 6-3. 콜론·세미콜론 간격 (시트 [53])

- 콜론(`:`)·세미콜론(`;`)은 **앞 글자에 붙이고, 뒤 글자와 한 칸 띄운다**(국·영문 동일).

### 6-4. 작품 정보(영화정보) (시트 [10][11][16]~[23])

- 표기 순서: **제작국가 | 제작연도 | 러닝타임 | 색채 | 카테고리 | 관람등급**
  예) `Korea | 2015 | 114min | Color | Documentary | G`
- **제작연도**: 최종 작업 완료 시점만 표기 (`2002-2003` ✗ → `2003` ✓).
- **러닝타임**: 분·초 모두 올림하여 분 단위, 숫자 뒤 `min`(마침표 없음). 예) `53min`.
- **색채**: 컬러 `Color`, 흑백 `B&W`.
- **프리미어**: `World Premiere` / `International Premiere` / `Asian Premiere` / `Korean Premiere` 중 해당 표기.
- **관람등급**: 전체 `General (G)` · 12세 `Under 12 not admitted (12)` · 15세 `Under 15 not admitted (15)` · 18세 `Under 18 not admitted (18)`.
- **자막**: `English Subtitles` / `No English Subtitles` / `No Dialogue`.
- **국가명 대조**: 한국 `Korea`, 미국 `USA`, 대만 `Taiwan`, 홍콩 `Hong Kong, China`.

> TM의 `영화정보` 영문 칸은 비어 있으나, 국문 칸이 이미 위 영문 형식을 담고 있다.
> 영화정보는 **번역 대상이 아니라 위 형식 규칙에 맞춰 정렬·검증**하는 필드로 다룬다.

### 6-5. 서적·논문·음반·전시·공연 (시트 [29]~[37])

| 종류 | 국문 | 영문 |
|---|---|---|
| 도서 | 겹낫표 `『 』`, 저자명 `( )` | 이탤릭, 저자명 `( )` |
| 논문·정기간행물·TV 프로그램 | 낫표 `「 」`, 저자명 `( )` | 이탤릭, 저자명 `( )` |
| 전시 | 겹화살괄호 `《 》` | 국·영문 동일 `《 》` |
| 음반 | 낫표 `「 」` | 낫표 `「 」` |
| 노래(곡) 제목 | 작은따옴표 `' '` | 작은따옴표 `' '` |
| 공연 | 작은따옴표 `' '` | 따옴표 없이 첫 글자 대문자 + 이탤릭 |

예) 음반 「애비 로드」에 수록된 'Come Together'

### 6-6. 별명·애칭 (시트 [45][46])

- 첫 언급 시 작은따옴표 `' '` 안에 표기하고, 이후 재언급 시에는 부호 없이 쓴다.
  예) `his 62-year-old father, Francisco Marín 'Novato'` → 이후 `Novato`.

### 6-7. 학교·단체·회사명 (시트 [35][233])

- 학교·단체·회사 등의 **한글 표기는 띄어쓰기 없이** 붙여 쓴다.
  예) `울산울주세계산악영화제조직위원회`.
- 회사 공식 표기는 `Co.` / `Inc.` / `Ltd.` / `Co.,Ltd.` 등 회사 자체 표기를 따른다.

### 6-8. 숫자·날짜·시간·통화 (시트 [165]~[180][231][232])

- **시간**: 24시간 4자리 표기(`04:00`, `16:00`), AM/PM 미사용.
- **범위 기호**: ` - ` 앞뒤로 한 칸씩 띄움. 예) `09:00 - 20:00`, `Sep. 26(Fri) - 30(Tue)`.
- **날짜(국문)**: `9. 26.(금) 19:00` / **(영문)**: `Sep. 26(Fri) 19:00`.
- **월 약어(영문)**: Jan. / Feb. / Mar. / Apr. / **May** / June / July / Aug. / Sep. / Oct. / Nov. / Dec.
  *(시트 [171]에는 `May.`로 마침표가 있으나 May는 약어가 아니므로 조직위 확인 필요.)*
- **통화**: `15,000원 → 15,000 KRW`.

### 6-9. 고정 명칭 (섹션·시상·장소·영화제·학교) — 시트 대조표 그대로

아래 범주의 명칭은 **표기 시트의 대조표를 그대로** 사용한다. 임의 번역 금지.

- **섹션명**(시트 [182]~[206]): 국제경쟁 `International Competition`, 산 `Mountain`, 자연 `Nature`,
  인간 `Human`, 올해의 산 `Guest Country`, 코리안 웨이브 `Korean Wave` 등.
- **시상명**(시트 [183]~[210]): 대상 `Grand Prize`, 작품상 `Best Film`, 감독상 `Best Director`,
  넷팩상 `NETPAC Award` 등.
- **장소명**(시트 [131]~[158]): 움프 시네마 `UMFF Cinema (UC)`, 언덕 극장 `Hill Cinema (HC)` 등.
- **해외 영화제·학교**(시트 [58]~[120]): 칸영화제 `Cannes Film Festival`,
  런던예술대학교 `University of the Arts London` 등.
- **영화제 공식명**(시트 [127][128]): `9th Ulsan Ulju Mountain Film Festival`,
  약칭 `UMFF 2026`. 표지 등에서 `th`는 윗첨자, 본문에서는 윗첨자 미사용.

> 위 목록은 발췌이며, 실제 적용 시 표기 시트 원본을 1차 출처로 조회한다.
