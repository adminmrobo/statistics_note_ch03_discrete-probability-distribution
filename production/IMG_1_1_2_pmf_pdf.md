# 1.1-2번 「셀 수 있는 확률, 잴 수밖에 없는 확률 — 확률질량함수·확률밀도함수·균일분포」 이미지 제작 명세서

| 항목 | 내용 |
|---|---|
| 페이지 | 1-1-2_pmf_pdf.html |
| 모드 / 주 앵커 | 교과서 / B 연구실: 밤의 연구실 측정대 (정밀 저울·시험관 선반·눈금 실린더) |
| 시즌 | 기본 |
| 대결 | "높이에 걸까, 넓이에 걸까?" (표준정규 측정값 2,000개, 구간 적중 비율) → 결과 **F**, 차이 0.229 (0.304 vs 0.075, 이론 0.302 vs 0.080) |
| 새로 그릴 그림 | P1 2장 · P2 3장 · P3 1장 |
| 제작 경로 | 직접 4장 (페이지·파일에 넣음) · 외부 의뢰 2장 (받을 것) + 외부 선택 2장 |
| 의뢰 도구 | Genspark (기본) |
| 진행 | 받음 0 / 의뢰 2 · 마지막 반영 아직 |
| 캐릭터 팩 표정 | 96px 26장 + 192px 14장 (팩 커밋 ea5da3f) |
| 재사용 | 0장 (기존 장면 목록 없음) |
| 그림이 없을 때 | 페이지는 캐릭터 팩 표정과 CSS 배경·합성 무대로 이미 완성 상태 |

## 1. 그림체와 고정 외형
- 스타일: SKILL 18-3 (16비트 SNES 시대 픽셀 아트, 굵은 외곽선, 디더링 음영)
- 캐릭터 고정 외형: SKILL 18-4 표 그대로 (공식 저장소 `CHARACTER_CORE_EN`)
- 이 페이지 장소: 밤의 연구실 측정대. 왼쪽은 어둡고 단순하게, 오른쪽에 정밀 저울(표시창은 빈칸), 시험관 6개가 꽂힌 선반, 눈금 실린더, 막대 그래프와 넓이가 칠해진 종 곡선만 그려진 칠판(글자 없음)
- 장소 영어 묘사: *wide night laboratory measuring bench with a precision balance whose display is blank, a rack of six test tubes holding different amounts of glowing green marbles, a tall graduated cylinder without numbers, and a small chalkboard showing only a row of lollipop bars and a bell curve with a shaded band, no writing*

## 2. 필요한 그림 전체

| # | 키 | 판 | 크기 | 상태 | 제작 | 우선 | 들어가는 곳 | 대신 쓰는 그림 |
|---|---|---|---|---|---|---|---|---|
| 1 | bg_1_1_2 | F | 1920×720 | 의뢰 | 외부 | P1 | 히어로 배경 (`.hero-bg`) | CSS 그라데이션 + 벌집 무늬 |
| 2 | sc_1_1_2_hero | E | 1200×800 | 의뢰 | 외부 | P1 | 히어로 오른쪽 위 (`.stage`, 그림을 받으면 나타남) | 없음 — 슬롯을 숨기고 대화창만 보임 |
| 3 | doc_think → doc_e09 | A | 팩 96 | 팩 | — | — | 히어로 대화창 | — |
| 4 | asst_smile → asst_e13 | B | 팩 96 | 팩 | — | — | 히어로 대화창, 등장인물 | — |
| 5 | fly_point → fly_e08 | C | 팩 96·192 | 팩 | — | — | 히어로, 대결 전 (`data-face="right"`로 뒤집음) | — |
| 6 | robo_coin → robo_e16 | D | 팩 96·192 | 팩 | — | — | 히어로, 대결 전 ($ 금화) | — |
| 7 | doc_front → doc_e08 | A | 팩 96 | 팩 | — | — | 등장인물, ④칸 박사의 한 줄 | — |
| 8 | fly_clip → fly_e10 | C | 팩 96 | 팩 | — | — | 등장인물 | — |
| 9 | robo_smile → robo_e13 | D | 팩 96 | 팩 | — | — | 등장인물 | — |
| 10 | doc_e07 | A | 팩 96 | 팩 | — | — | "왜 이 주제인가" 박사의 한 줄 | — |
| 11 | asst_e10 | B | 팩 96 | 팩 | — | — | ①칸, 정리 (숫자 확인) | — |
| 12 | fly_e07 | C | 팩 96 | 팩 | — | — | ②칸 (돋보기) | — |
| 13 | robo_e04 | D | 팩 96 | 팩 | — | — | ③칸 (함정: 밀도 2.0) | — |
| 14 | fly_e09 | C | 팩 96 | 팩 | — | — | ⑤칸 (키보드, 코드 점검) | — |
| 15 | asst_firm → asst_e12 | B | 팩 96·192 | 팩 | — | — | 대결 결과 발표 전, 아웃트로 | — |
| 16 | doc_judge → doc_e10 | A | 팩 96 | 팩 | — | — | 대결 판정 | — |
| 17 | asst_spark → asst_e01 | B | 팩 96 | 팩 | — | — | 대결 후 발표 | — |
| 18 | fly_arms → fly_e16 | C | 팩 192 | 팩 | — | — | 대결 후 (F), 아웃트로 | — |
| 19 | robo_sigh → robo_e20 | D | 팩 192 | 팩 | — | — | 대결 후 (F) | — |
| 20 | fly_coffee → fly_e13 · fly_cry → fly_e21 · robo_happy → robo_e12 · robo_meh → robo_e18 · robo_blush → robo_e14 · asst_shock → asst_e24 | C·D·B | 팩 192·96 | 팩 | — | — | 대결 후 R/D/X 대비 (부록 E-4: 결과 넷 모두의 키) | — |
| 21 | doc_scale → doc_e13 | A | 팩 96 | 팩 (저울 그림 없음) | 외부 (선택) | P2 | 무승부일 때 판정 | doc_e13 |
| 22 | doc_magic → doc_e16 | A | 팩 96·192 | 팩 | — | — | 아웃트로 (보라 불꽃) | — |
| 23 | robo_e14 | D | 팩 96·192 | 팩 | — | — | 아웃트로 (머쓱함) | — |
| 24 | asst_e07 | B | 팩 96 | 팩 | — | — | 꾸러미 섹션 조수 말풍선 | — |
| 25 | cut_1_1_2_versus | G | 960×540 | 넣음 | 직접 (팩 192 + CSS 띠) | P3 | 대결 머리 | — |
| 26 | sc_1_1_2_outro | E | 1200×800 | 넣음 (합성본) | 직접 → 외부 선택 | P2 | 아웃트로 무대 | 팩 캐릭터 CSS 무대 합성 |
| 27 | thumb_1_1_2 | I | 600×400 | 넣음 (파일) | 직접 (CSS 배경 + 칠판 SVG + 팩 2명 + 제목) | P2 | 시리즈 목차 카드 | 색 카드 |
| 28 | og_1_1_2 | K | 1200×630 | 넣음 (파일) | 직접 (합성) | P3 | 공유 미리보기 (`og:image`) | 없음 |
| — | 행동으로 보기 (주사위·시험관·시료 점·콘솔), NPC | — | — | 코드 | 직접 | — | Canvas 그림 | — |

상태 값: `팩` · `넣음`(직접 그림, 페이지에 있음) · `의뢰`(외부, 받을 것) · `받음`(검수 전) · `반영`(페이지에 넣음) · `다시 의뢰`(검수 탈락).

## 3. 새로 그릴 그림 상세

### 3-1. `bg_1_1_2` — 밤의 연구실 측정대 (히어로 배경)
| 항목 | 내용 |
|---|---|
| 판 · 크기 | F · 1920×720 (정수배 가능) |
| 제작 경로 | 외부: Genspark |
| 배경 | 그림 전체 |
| 구도 | 왼쪽 45%는 어두운 벽과 창만(제목 자리). 오른쪽 55%에 측정대: 정밀 저울, 시험관 6개 선반, 눈금 실린더, 작은 칠판. 인물 없음 |
| 표정·몸짓 | 없음 |
| 소품 | 저울(표시창 빈칸), 높이가 고른 초록 구슬이 든 시험관 6개, 눈금 없는 실린더, 칠판(막대 5개 + 넓이 칠한 종 곡선 그림만) |
| 빛·분위기 | 남보라 어둠, 왼쪽에서 들어오는 보라 조명, 시험관의 초록 형광, 모니터 청록 |
| 피할 것 | 글자·숫자·눈금 숫자, 초파리 해부·현미경 소품(생물 앵커 아님), 실존 브랜드 저울 |
| 대체 글 (alt) | 밤의 연구실 측정대: 정밀 저울과 시험관 선반, 눈금 실린더가 놓이고 보라 조명이 왼쪽에서 비친다 |
| 대신 쓰는 그림 | CSS 그라데이션 + 벌집 무늬 |

**프롬프트 (복사해서 사용)**
```
detailed 16-bit SNES-era pixel art, limited palette, crisp pixels, dithering shading, thick dark outlines, cheerful comedy mood, consistent with the reference images, cozy night laboratory mood, purple light, soft magenta and green fluorescent accents, wide 8:3 background, left side simple and calm for title text, details on the right, wide night laboratory measuring bench with a precision balance whose display is blank, a rack of six test tubes holding equal amounts of glowing green marbles, a tall graduated cylinder without numbers, and a small chalkboard showing only a row of five lollipop bars and a bell curve with a shaded band, purple lab light spilling in from the left, a dark window with a small moon on the left wall, no characters, no text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands
```

### 3-2. `sc_1_1_2_hero` — 넷이 측정대 앞에서 핵심 질문을 바라보는 장면
| 항목 | 내용 |
|---|---|
| 판 · 크기 | E · 1200×800 (3:2) |
| 제작 경로 | 외부: Genspark |
| 배경 | 그림 전체 |
| 구도 | 위쪽 62% 안에 칠판과 얼굴. 초파리 왼쪽에서 오른쪽을 보며 저울을 가리킴, 박사 가운데 뒤 턱에 손, 하루 오른쪽 옆에서 시료 접시를 듦, Money-Robo 오른쪽에서 왼쪽을 보며 금화 하나. 크기: 박사 키 = 하루 키 ≈ 초파리 × 1.3 |
| 표정·몸짓 | 박사 doc_think(한쪽 눈썹, 턱에 손), 하루 asst_smile, 초파리 fly_point(의심하는 눈), 로봇 robo_coin(가늘게 뜬 눈, 히죽) — 승패 암시 없음 |
| 소품 | 정밀 저울(표시창 빈칸), 시료 접시, 칠판(막대 + 넓이 칠한 곡선, 글자 없음), 금화 1개($ 모양도 생략) |
| 빛·분위기 | 빛이 저울과 칠판의 칠한 넓이에 모임 |
| 피할 것 | 결과 암시(누가 이긴 듯한 표정·배치), 글자, "B" 표시 금화 |
| 대체 글 (alt) | 밤의 연구실 실험대 앞에 네 캐릭터가 서 있고, 칠판에는 막대 그래프와 넓이가 칠해진 곡선이 그려져 있다 |
| 대신 쓰는 그림 | 없음 (받기 전에는 슬롯을 숨기고 히어로 대화창만 보임) |

**프롬프트 (복사해서 사용)**
```
detailed 16-bit SNES-era pixel art, limited palette, crisp pixels, dithering shading, thick dark outlines, cheerful comedy mood, consistent with the reference images, cozy night laboratory mood, purple light, soft magenta and green fluorescent accents, 3:2 landscape scene, medium brightness, the Professor, a chibi male scientist with a big head, dark charcoal spiky hair with a white streak at the front, a small low ponytail at the back, very thick bold black eyebrows, teal-framed rectangular glasses, light peach skin, white lab coat over a black vest, black tie and black slacks, standing at the back center with a hand on his chin and one eyebrow raised; the Fruit Fly, a tiny expressive cartoon fruit fly researcher with a dark charcoal-black segmented insect body, large glossy red compound eyes, a retro dark blue helmet with a yellow-white center stripe and small round side bolts, colorful dangling cables in magenta, purple and blue curving from the back of the helmet, a tiny white lab coat over a black vest, translucent veined wings, six thin black legs with the front pair used like hands, on the left looking right and pointing at a precision balance with a suspicious look; Haru, a cute anime girl lab assistant, long straight pink hair with navy blue streaks including a thick navy streak down the center of the bangs, two round messy hair buns on top of the head, a small ahoge, big bright blue eyes, light peach skin, wearing a lavender hoodie with white drawstrings over a white t-shirt, under an open white knee-length lab coat, at the right side holding a small sample dish and smiling softly; MONEY-ROBO, a cute small floating chibi robot with a large glossy rounded-square white head and a small rounded white body with thick black outlines, a black pill-shaped screen face showing golden-yellow pixel eyes and mouth, a small round knob antenna on a short stem, stubby rounded fingerless arms, no legs, a black oval chest panel with a bright cyan pill-shaped core light, hovering above a small dark oval shadow, on the right looking left with narrowed smug eyes beside one plain shiny gold coin; behind them a night lab measuring bench with a precision balance whose display is blank, a rack of six test tubes and a small chalkboard showing only lollipop bars and a bell curve with a shaded band, light gathering on the balance and the shaded band, no text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands
```

### 3-3. `sc_1_1_2_outro` — 결과 후 (F): 초파리 앞, 로봇 인정
| 항목 | 내용 |
|---|---|
| 판 · 크기 | E · 1200×800 |
| 제작 경로 | 직접 합성본이 페이지에 있음 → 외부 의뢰는 **선택** (P2) |
| 배경 | 그림 전체 |
| 구도 | 초파리가 앞·크게 팔짱(반짝이), Money-Robo는 같은 화면 뒤쪽에서 머쓱하게 볼을 붉힘(조롱 없음), 박사 왼쪽 보라 불꽃, 하루 오른쪽 주먹 쥔 응원 |
| 소품 | 칠판에 넓게 칠한 곡선 아래 넓이(글자 없음) |
| 피할 것 | 패자를 비웃는 몸짓, 글자 |
| 대체 글 (alt) | 연구실에서 초파리 연구원이 앞에 서서 팔짱을 끼고, 뒤에서 Money-Robo가 머쓱해하며, 박사와 하루가 지켜보는 장면 |
| 대신 쓰는 그림 | 팩 캐릭터 CSS 무대 합성 (doc_e16, fly_e16, robo_e14, asst_e12) |

**프롬프트 (선택 의뢰 시)**
```
detailed 16-bit SNES-era pixel art, limited palette, crisp pixels, dithering shading, thick dark outlines, cheerful comedy mood, consistent with the reference images, cozy night laboratory mood, purple light, soft magenta and green fluorescent accents, 3:2 landscape scene, medium brightness, the Fruit Fly, a tiny expressive cartoon fruit fly researcher with large glossy red compound eyes, a retro dark blue helmet with a yellow-white center stripe and magenta, purple and blue cables, a tiny white lab coat over a black vest, translucent veined wings, standing in front and larger with arms crossed and confident sparkling eyes; MONEY-ROBO, a cute small floating chibi robot with a glossy rounded-square white head, a black pill-shaped screen face with golden-yellow pixel eyes, pink blush lines beside the eyes, a cyan chest core light, hovering slightly behind with an embarrassed but good-natured look; the Professor, a chibi male scientist with dark charcoal spiky hair with a white streak, very thick black eyebrows, teal-framed rectangular glasses, white lab coat over a black vest and tie, on the left laughing with purple flames on both palms; Haru, an anime girl lab assistant with long straight pink hair with navy streaks and two round hair buns, a lavender hoodie under an open white lab coat, on the right cheering with a raised fist; a chalkboard behind showing a bell curve with a wide shaded band, no text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands
```

### 3-4. `doc_scale` (E25 후보) — 박사, 수평 놋쇠 저울
| 항목 | 내용 |
|---|---|
| 판 · 크기 | A · 약 390×390 (저장소 원본과 같게) |
| 제작 경로 | 외부 (선택, P2). 받으면 저장소에 `images/doctor/E25_scale.png` + `specs/doctor/expressions/E25_scale.md`로 먼저 올린 뒤 팩 재빌드 |
| 배경 | 연회색 단색 (안 되면 #00ff00) |
| 표정·몸짓 | 차분한 미소, 수평인 놋쇠 저울을 두 손으로 든다 |
| 대신 쓰는 그림 | doc_e13 |

**프롬프트:** 저장소 `specs/doctor/expressions/E13_neutral` 항목의 `prompt_en`을 복사해 얼굴·몸짓 구절만 *calm gentle smile, holding a perfectly level brass balance scale with both hands*로 바꾼다(SKILL 18-9 "새 표정").

### 3-5. 직접 그림 (이미 만듦)
- `cut_1_1_2_versus`: 대결 머리. 팩 192px 초파리(오른쪽을 보게 뒤집음)·Money-Robo + 빨강→청록 그라데이션 띠 + "VS" 글자(HTML).
- `thumb_1_1_2.png` (600×400), `og_1_1_2.png` (1200×630): 어두운 연구실 그라데이션 + 칠판 SVG(막대·넓이 곡선) + 팩 초파리(E08, 뒤집음)·Money-Robo(E16) + 제목(HTML 글자). bg_1_1_2를 받으면 thumb은 그 배경을 3:2로 다시 잘라 만든다.

## 4. 일관성 지침
- 참고 이미지: 공식 저장소 `refs/original/keyart_rivals.png`(넷이 함께) + `images/fruitfly/E08_guiding.png`, `images/money_robo/E16_proud.png`, `images/doctor/E09_thinking.png`, `images/haru/E13_neutral.png`
- 같은 캐릭터는 같은 세션에서, 시드 고정 가능하면 고정: 박사 1101, 조수 1102, 초파리 1103, 로봇 1104
- 표정만 바꿀 때 추가 문장: *same character, same size and position, only change the facial expression and pose to ...*
- 투명 배경이 안 되면: *solid flat #00ff00 background*

## 5. 넘겨받은 뒤 처리
SKILL 18-15 절차 그대로 (키 맞추기 → 눈으로 검수 → `--ingest` → 페이지에 넣기 → 새 표정이면 저장소용 파일 → 상태 갱신 → 점검 → 전달).
```bash
python3 build_character_pack.py --ingest 받은폴더/ --plates bg_1_1_2=F,sc_1_1_2_hero=E --out received_1_1_2
```
페이지는 `.hero-bg`와 `.stage`가 `data-img` 키로 `SPRITE`를 찾으므로, 나온 `Object.assign(SPRITE,{…})` 조각을 `SPRITE` 정의 뒤에 붙이면 된다. 히어로 무대(`.stage`)는 평소 숨겨져 있다가, `SPRITE`에 `sc_1_1_2_hero`가 생기면 대화창 위에 3:2 그림으로 나타난다.

## 6. 체크리스트
- [x] HTML의 모든 `data-img` 키가 명세서에 있고, 명세서의 모든 키가 HTML에 쓰임 (thumb은 목차 카드용 파일)
- [x] 대결 결과 후 표정이 5-8절 표와 일치 (F: fly_e16 / robo_e20 / asst_e01 / doc_e10), 결과 넷 모두의 키가 들어 있음
- [x] 결과 전 그림에 승패 암시 없음 (fly_e08, robo_e16)
- [x] 판별 크기·바라보는 쪽·배경이 18-2 표와 일치
- [x] 모든 프롬프트에 18-4 고정 외형 영어 묘사와 금지 구절
- [x] 팩에 있는 표정을 "새로 그림"에 넣지 않음 (doc_scale만 그림 없음 키)
- [x] 직접 그림 4장은 이미 들어가 있음, 외부 의뢰 2장은 의뢰 묶음에 참고 이미지·파일 이름·배경 지시
- [x] 장소가 B 연구실 앵커와 일치, 초파리 해부·현미경 소품 없음
- [x] 그림 안 글자 없음, 실존 브랜드 없음, Money-Robo "B" 금화(E19·E21)는 눈에 띄는 자리에 쓰지 않음
- [x] P1 2장 (6장 이하), 페이지 그림 합계 base64 약 373 KB (530 KB 이하)

## 8. 외부 의뢰 묶음 (Genspark 에 그대로 붙여 넣기)

같은 세션에서 이 순서대로: 배경 → 장면.

### 의뢰 1/2 · `bg_1_1_2`
- **올릴 참고 이미지:** 없음 (배경만). 그림체 맞춤용으로 `refs/original/keyart_rivals.png` 1장을 넣어도 됨
- **크기·비율:** 1920×720 (8:3) 이상
- **배경:** 그림 전체
- **받을 파일 이름:** `bg_1_1_2.png`
- **프롬프트:** 3-1의 완성 프롬프트 그대로
- **네거티브:** `blurry, smooth vector art, 3D render, photorealistic, anti-aliased painting, inconsistent character, off-model, text, letters, watermark`
- **확인할 것:** 저울 표시창·실린더에 숫자가 생기면 다시. 왼쪽 45%가 복잡하면 다시

### 의뢰 2/2 · `sc_1_1_2_hero`
- **올릴 참고 이미지:** `refs/original/keyart_rivals.png`, `images/doctor/E09_thinking.png`, `images/fruitfly/E08_guiding.png`, `images/money_robo/E16_proud.png`, `images/haru/E13_neutral.png`
- **크기·비율:** 1200×800 (3:2) 이상
- **배경:** 그림 전체
- **받을 파일 이름:** `sc_1_1_2_hero.png`
- **프롬프트:** 3-2의 완성 프롬프트 그대로
- **네거티브:** `blurry, smooth vector art, 3D render, photorealistic, anti-aliased painting, inconsistent character, off-model, text, letters, watermark`
- **확인할 것:** 박사 안경이 둥글게 나오면 다시. 하루 앞머리 가운데 남색 줄과 번 2개 확인. 금화에 "B"나 기호가 생기면 다시

## 7. 매니페스트
```json
{
  "page": "1-1-2_pmf_pdf",
  "anchor": "B:measuring-bench",
  "season": "default",
  "duel": {"result": "F", "gap": 0.229},
  "images": [
    {"key":"bg_1_1_2","plate":"F","size":[1920,720],"maker":"external","tool":"genspark","status":"requested","priority":"P1","slot":"hero-bg","fallback":"css","alt":"밤의 연구실 측정대: 정밀 저울과 시험관 선반, 눈금 실린더가 놓이고 보라 조명이 왼쪽에서 비친다"},
    {"key":"sc_1_1_2_hero","plate":"E","size":[1200,800],"maker":"external","tool":"genspark","status":"requested","priority":"P1","slot":"hero-stage","fallback":"hidden","alt":"밤의 연구실 실험대 앞에 네 캐릭터가 서 있고, 칠판에는 막대 그래프와 넓이가 칠해진 곡선이 그려져 있다"},
    {"key":"sc_1_1_2_outro","plate":"E","size":[1200,800],"maker":"claude","status":"placed","priority":"P2","slot":"outro","fallback":"composite","external_optional":true,"alt":"연구실에서 초파리 연구원이 앞에 서서 팔짱을 끼고, 뒤에서 Money-Robo가 머쓱해하며, 박사와 하루가 지켜보는 장면"},
    {"key":"cut_1_1_2_versus","plate":"G","size":[960,540],"maker":"claude","status":"placed","priority":"P3","slot":"duel-head","alt":""},
    {"key":"thumb_1_1_2","plate":"I","size":[600,400],"maker":"claude","status":"placed","priority":"P2","slot":"index-card","alt":"확률질량함수·밀도함수 페이지 카드"},
    {"key":"og_1_1_2","plate":"K","size":[1200,630],"maker":"claude","status":"placed","priority":"P3","slot":"og","alt":"1.1-2 확률질량·밀도 함수 페이지 미리보기"},
    {"key":"doc_scale","pack":"doc_e13","plate":"A","size":96,"status":"pack-substitute","priority":"P2","maker":"external-optional","slot":"duel-verdict-draw","alt":""},
    {"key":"doc_think","pack":"doc_e09","plate":"A","size":96,"status":"pack","slot":"hero-dialog","alt":""},
    {"key":"asst_smile","pack":"asst_e13","plate":"B","size":192,"status":"pack","slot":"hero-dialog","alt":""},
    {"key":"fly_point","pack":"fly_e08","plate":"C","size":192,"status":"pack","slot":"duel-before","alt":""},
    {"key":"robo_coin","pack":"robo_e16","plate":"D","size":192,"status":"pack","slot":"duel-before","alt":""},
    {"key":"fly_arms","pack":"fly_e16","plate":"C","size":192,"status":"pack","slot":"duel-after","alt":""},
    {"key":"robo_sigh","pack":"robo_e20","plate":"D","size":192,"status":"pack","slot":"duel-after","alt":""},
    {"key":"asst_spark","pack":"asst_e01","plate":"B","size":96,"status":"pack","slot":"duel-result","alt":""},
    {"key":"doc_judge","pack":"doc_e10","plate":"A","size":96,"status":"pack","slot":"duel-verdict","alt":""},
    {"key":"doc_magic","pack":"doc_e16","plate":"A","size":192,"status":"pack","slot":"outro","alt":""}
  ],
  "character_pack": {"repo":"adminmrobo/fruitfly-lab-expressions","commit":"ea5da3f"},
  "status_values": "pack | placed(직접, 넣음) | requested(의뢰) | received(받음) | applied(반영) | rejected(다시 의뢰)"
}
```
