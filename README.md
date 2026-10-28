# 우연의 과학통계학

밤의 연구실에서 **박사·하루(조수)·초파리 연구원·Money-Robo** 네 캐릭터가 진행하는 인터랙티브 확률·통계 해설 시리즈입니다.
페이지마다 직접 움직여 보는 시뮬레이션, 초파리와 Money-Robo의 대결, 확인 퀴즈, 지식 색인이 들어 있습니다.
서버나 설치 없이 브라우저에서 바로 열리는 정적 HTML이라 GitHub Pages에 그대로 올릴 수 있습니다.

## 해설 페이지

| 번호 | 제목 | 다루는 개념 | 파일 |
|---|---|---|---|
| 1.1 (2) | 셀 수 있는 확률, 잴 수밖에 없는 확률 | 확률질량함수(PMF), 확률밀도함수(PDF), 균일분포, 누적분포함수(CDF) | [`1-1-2_pmf_pdf.html`](1-1-2_pmf_pdf.html) |

## 폴더 구조

```
.
├── index.html                 # 시리즈 목차 (GitHub Pages 첫 화면)
├── 1-1-2_pmf_pdf.html         # 1.1(2) 해설 페이지 — 그림·데이터를 모두 품은 단일 파일
├── assets/
│   ├── thumb_1_1_2.png        # 목차 카드 썸네일 (600×400)
│   ├── og_1_1_2.png           # 공유 미리보기 이미지 (1200×630)
│   └── characters/            # 목차 등장인물 카드용 표정 4장 (WebP)
├── production/                # 제작 문서 (사이트에는 링크하지 않음)
│   ├── IMG_1_1_2_pmf_pdf.md   # 1.1(2) 이미지 제작 명세서 · 외부 의뢰 프롬프트
│   ├── IMG_00_index.md        # 시리즈 공용 이미지 명세서
│   └── KG_00_registry.json    # 시리즈 지식 그래프 등록부 (개념·문헌 ID)
├── .nojekyll                  # Jekyll 처리 끄기 (파일을 그대로 서비스)
└── README.md
```

## GitHub Pages로 공개하기

1. GitHub에서 새 저장소를 만든다 (예: `uyeon-stats`). 공개(Public) 저장소여야 무료 요금제에서 Pages를 쓸 수 있다.
2. 이 폴더의 파일을 모두 저장소 맨 위(root)에 올린다.
   ```bash
   git init
   git add .
   git commit -m "우연의 과학통계학 1.1(2) 공개"
   git branch -M main
   git remote add origin https://github.com/<사용자명>/<저장소>.git
   git push -u origin main
   ```
   웹에서 올릴 때는 저장소의 **Add file → Upload files**로 폴더째 끌어다 놓으면 된다. 이때 `.nojekyll`처럼 점으로 시작하는 파일이 빠지지 않았는지 확인한다.
3. 저장소 **Settings → Pages**에서 **Source: Deploy from a branch**, **Branch: `main` / `/ (root)`**를 고르고 저장한다.
4. 1~2분 뒤 `https://<사용자명>.github.io/<저장소>/`에서 목차가 열린다. 해설 페이지는 `…/<저장소>/1-1-2_pmf_pdf.html`이다.

### 공개 후 한 번만 고칠 것

- **공유 미리보기 이미지:** 카카오톡·슬랙 등은 `og:image`의 **절대 주소**만 읽는다. 주소가 정해지면 `index.html`과 `1-1-2_pmf_pdf.html`의 `<meta property="og:image" content="assets/og_1_1_2.png">`를 `https://<사용자명>.github.io/<저장소>/assets/og_1_1_2.png`로 바꾼다.
- **라이선스:** 해설 페이지 맨 끝 꾸러미의 `page_meta.json`에 라이선스와 공개 주소가 비어 있다. 정한 뒤 페이지 안 `<script id="page-meta">`의 `"license"`, `"url"` 값을 채운다.

## 로컬에서 보기

`index.html`을 더블클릭하면 된다. 인터넷이 끊겨 있으면 글꼴만 시스템 글꼴로 바뀌고 나머지는 그대로 동작한다.

## 새 해설 페이지 추가하기

1. 새 페이지 HTML(예: `1-2-1_normal.html`)과 썸네일(`assets/thumb_1_2_1.png`, 600×400)을 올린다.
2. `index.html`의 `<a class="card" …>` 블록 하나를 복사해 주소·썸네일·번호·제목·설명·태그를 고친다. 준비 중 카드(`card soon`)는 공개하면 지운다.
3. 위 "해설 페이지" 표에 한 줄 더한다.
4. 새 페이지가 만든 개념·문헌 ID를 `production/KG_00_registry.json`에 합친다(같은 개념은 같은 ID).
5. 새 페이지 푸터의 "← 목차로" 링크는 `index.html`을 가리키므로 같은 폴더에 두면 그대로 동작한다.

## 페이지 안에 든 것

- 개념 사다리 5칸과 칸마다 직접 만지는 시뮬레이션(시드 고정 설명용 모형)
- 초파리 연구원 vs Money-Robo 대결 — 결과는 페이지 안 계산으로 정해짐
- 확인 퀴즈, 용어 말풍선(노란 점선 밑줄), 읽은 곳·퀴즈 진행 도우미
- 지식 색인(검색·관계 그래프)과 온톨로지·서지 꾸러미(JSON-LD, Turtle, CSV, CSL-JSON, BibTeX, RIS를 ZIP으로 내려받기)
- 외부 스크립트·브라우저 저장소를 쓰지 않음. 외부 요청은 Google Fonts 글꼴 하나

## 출처와 크레딧

- 글·구성: 안상선
- 캐릭터 그림: [adminmrobo/fruitfly-lab-expressions](https://github.com/adminmrobo/fruitfly-lab-expressions) (커밋 `ea5da3f`)
- 각 페이지의 참고 자료는 페이지 맨 아래 출처 표와 꾸러미의 `references.*` 파일에 있다.

## 라이선스

(정해지면 적는다. 글·코드와 캐릭터 그림의 라이선스를 따로 적는 것을 권한다.)
