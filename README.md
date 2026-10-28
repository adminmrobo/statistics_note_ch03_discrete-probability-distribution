# 우연의 과학통계학 — 3장 이산확률분포

밤의 연구실에서 **박사·하루(조수)·초파리 연구원·Money-Robo** 네 캐릭터가 진행하는 인터랙티브 확률·통계 해설 시리즈입니다.
페이지마다 직접 움직여 보는 시뮬레이션, 초파리와 Money-Robo의 대결, 확인 퀴즈, 지식 색인이 들어 있습니다.
서버나 설치 없이 브라우저에서 바로 열리는 정적 HTML이라 GitHub Pages에 그대로 올릴 수 있습니다.

**사이트 주소:** https://adminmrobo.github.io/statistics_note_ch03_discrete-probability-distribution/

## 해설 페이지

| 번호 | 제목 | 다루는 개념 | 파일 |
|---|---|---|---|
| 1.1 | 성공과 실패를 세는 일곱 가지 방법 | 베르누이, 이항, 기하·음이항, 포아송, 초기하·다항분포 | [`1-1_discrete_distributions.html`](1-1_discrete_distributions.html) |
| 1.2 | 셀 수 있는 확률, 잴 수밖에 없는 확률 | 확률질량함수(PMF), 확률밀도함수(PDF), 균일분포, 누적분포함수(CDF) | [`1-2_pmf_pdf.html`](1-2_pmf_pdf.html) |

1.1에서는 **세는 값**(성공 횟수, 도착 건수)의 분포를, 1.2에서는 **재는 값**으로 넘어가 한 점의 확률이 0인 연속확률변수와 밀도함수를 다룹니다.

## 폴더 구조

```
.
├── index.html                       # 시리즈 목차 (사이트 첫 화면)
├── 1-1_discrete_distributions.html  # 1.1 이산확률분포 — 그림·데이터를 모두 품은 단일 파일
├── 1-2_pmf_pdf.html                 # 1.2 확률질량함수·밀도함수 — 단일 파일
├── assets/
│   ├── thumb_1_1.png, thumb_1_2.png # 목차 카드 썸네일 (600×400)
│   ├── og_1_1.png, og_1_2.png       # 링크 공유 미리보기 (1200×630)
│   └── characters/                  # 목차 등장인물 카드용 표정 4장 (WebP)
├── production/                      # 제작 문서 (사이트에서 링크하지 않음)
│   ├── IMG_1_2_pmf_pdf.md           # 1.2 이미지 제작 명세서 · 외부 의뢰 프롬프트
│   ├── IMG_00_index.md              # 시리즈 공용 이미지 명세서
│   └── KG_00_registry.json          # 시리즈 지식 그래프 등록부 v0.2 (1.1·1.2 개념·문헌 ID)
├── .nojekyll                        # Jekyll 처리 끄기 (파일을 그대로 서비스)
└── README.md
```

## GitHub Pages로 공개하기

1. GitHub에서 저장소 `statistics_note_ch03_discrete-probability-distribution`을 만든다(Public).
2. 이 폴더의 파일을 모두 저장소 맨 위(root)에 올린다.
   ```bash
   git init
   git add .
   git commit -m "우연의 과학통계학 3장: 1.1 이산확률분포, 1.2 확률질량·밀도함수"
   git branch -M main
   git remote add origin https://github.com/adminmrobo/statistics_note_ch03_discrete-probability-distribution.git
   git push -u origin main
   ```
   웹에서 올릴 때는 **Add file → Upload files**로 폴더째 끌어다 놓는다. 점으로 시작하는 `.nojekyll`이 빠지지 않았는지 확인한다.
3. **Settings → Pages**에서 **Source: Deploy from a branch**, **Branch: `main` / `/ (root)`**를 고르고 저장한다.
4. 1~2분 뒤 위 사이트 주소에서 목차가 열린다.

> 페이지 안의 주소(공유 미리보기 `og:image`, 인용 주소, `page_meta.json`의 `url`)는 모두 위 저장소 이름을 기준으로 적혀 있다. **저장소 이름을 바꾸면** 각 HTML에서 `statistics_note_ch03_discrete-probability-distribution`을 새 이름으로 일괄 바꾼다. GitHub Pages 주소는 대소문자를 구분하므로 저장소 이름과 철자·대소문자가 정확히 같아야 한다.

## 로컬에서 보기

`index.html`을 더블클릭하면 된다. 페이지끼리의 링크(목차 ↔ 1.1 ↔ 1.2)는 같은 폴더 안의 상대 경로라 그대로 동작한다. 인터넷이 끊기면 글꼴만 시스템 글꼴로 바뀐다.

## 새 해설 페이지 추가하기

1. 새 페이지 HTML(`{번호}_{영문 슬러그}.html`)과 썸네일 `assets/thumb_{번호}.png`(600×400), 미리보기 `assets/og_{번호}.png`(1200×630)를 올린다.
2. `index.html`의 `<a class="card" …>` 블록 하나를 복사해 주소·썸네일·번호·제목·설명·태그를 고친다.
3. 바로 앞 페이지 푸터에 "다음 페이지" 링크를 더한다.
4. 위 "해설 페이지" 표에 한 줄 더하고, 새 페이지의 개념·문헌 ID를 `production/KG_00_registry.json`에 합친다(같은 개념은 같은 ID).

## 페이지 안에 든 것

- 개념 사다리 5칸과 칸마다 직접 만지는 시뮬레이션(시드 고정 설명용 모형)
- 초파리 연구원 vs Money-Robo 대결 — 결과는 페이지 안 계산으로 정해짐
- 확인 퀴즈, 용어 말풍선(노란 점선 밑줄), 읽은 곳·퀴즈 진행 도우미
- 지식 색인(검색·관계 그래프)과 온톨로지·서지 꾸러미(JSON-LD, Turtle, CSV, CSL-JSON, BibTeX, RIS를 ZIP으로 내려받기)
- 외부 스크립트·브라우저 저장소를 쓰지 않음. 외부 요청은 Google Fonts 글꼴 하나

## 출처와 크레딧

- 글·구성: 안상선 (AI 보조 제작)
- 캐릭터 그림: [adminmrobo/fruitfly-lab-expressions](https://github.com/adminmrobo/fruitfly-lab-expressions) (커밋 `ea5da3f`)
- 각 페이지의 참고 자료(Wikipedia 분포 문서, R·SciPy 함수 문서)는 페이지 맨 아래 출처 표와 꾸러미의 `references.*` 파일에 있다.

## 이 시리즈 인용하기

안상선 (2026). 우연의 과학통계학 — 3장 이산확률분포. https://adminmrobo.github.io/statistics_note_ch03_discrete-probability-distribution/

## 라이선스

(정해지면 적는다. 글·코드와 캐릭터 그림의 라이선스를 따로 적는 것을 권한다.)
