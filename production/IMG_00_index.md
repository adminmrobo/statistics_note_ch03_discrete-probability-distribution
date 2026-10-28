# 시리즈 공용 이미지 명세서 — 우연의 과학통계학

| 항목 | 내용 |
|---|---|
| 시리즈 | 우연의 과학통계학, 페이지 1개 (1.1-2) — 이 명세서는 시리즈 첫 등록 페이지가 만듦 |
| 시즌 | 기본 |
| 공용 표정 | 캐릭터 팩 96장 (커밋 ea5da3f) · 그림 없음 역할 키 3개 (doc_scale, asst_ledger, asst_board) |

## 1. 공용 표정 현황
| 키 | 팩 키 | 상태 | 쓰는 페이지 | 프롬프트 (그림 없음만) |
|---|---|---|---|---|
| doc_think | doc_e09 | 팩 | 1.1-2 | — |
| doc_judge | doc_e10 | 팩 | 1.1-2 | — |
| doc_magic | doc_e16 | 팩 | 1.1-2 | — |
| fly_point / fly_arms | fly_e08 / fly_e16 | 팩 | 1.1-2 | — |
| robo_coin / robo_sigh | robo_e16 / robo_e20 | 팩 | 1.1-2 | — |
| doc_scale | (doc_e13로 대신) | 그림 없음 | 1.1-2 (무승부 대비) | E13_neutral `prompt_en`에서 몸짓만 *calm gentle smile, holding a perfectly level brass balance scale with both hands* |
| asst_ledger | (asst_e07로 대신) | 그림 없음 | — | E07 `prompt_en`에서 몸짓만 *serious eyes, holding an open ledger with blank striped pages and a pen* |
| asst_board | (asst_e16로 대신) | 그림 없음 | — | E16 `prompt_en`에서 몸짓만 *proud smile, holding up a blank three-column scoreboard* |

## 2. 목차·표지 그림
| 키 | 판 | 내용 | 우선 | 제작 |
|---|---|---|---|---|
| cover_series | J | 밤의 연구실 전경. 박사가 가운데에서 벽의 큰 개념 지도(동그라미와 선, 글자 없음)를 가리키고, 초파리와 Money-Robo가 양쪽에서 올려다보고, 하루가 점수판을 든다. 칠판 한쪽에 주사위와 종 곡선 그림(통계 시리즈 표식) | P1 | 외부 |
| bg_index | F | 연구실 복도, 문마다 다른 색 빛(각 페이지 = 방) | P1 | 외부 |
| lineup | G | 넷이 나란히 선 소개 컷, 이름표 자리는 비움 | P1 | 직접 (팩 그림 배치) |
| thumb_1_1_2 | I | 1.1-2 페이지 카드 | P2 | 직접 (만듦) |
| icon_fly, icon_robo, icon_draw, icon_dq | H | 점수판·지도용 아이콘 | P1 | 직접 (팩 머리 자르기) |
| og_index | K | 시리즈 표지 축소판 | P3 | 직접 |

**cover_series 프롬프트**
```
detailed 16-bit SNES-era pixel art, limited palette, crisp pixels, dithering shading, thick dark outlines, cheerful comedy mood, consistent with the reference images, cozy night laboratory mood, purple light, soft magenta and green fluorescent accents, 16:9 series cover, all four characters together, the Professor, a chibi male scientist with a big head, dark charcoal spiky hair with a white streak at the front, a small low ponytail at the back, very thick bold black eyebrows, teal-framed rectangular glasses, light peach skin, white lab coat over a black vest, black tie and black slacks, at the center pointing at a large wall concept map made only of circles and lines; the Fruit Fly, a tiny expressive cartoon fruit fly researcher with a dark charcoal-black segmented insect body, large glossy red compound eyes, a retro dark blue helmet with a yellow-white center stripe and small round side bolts, colorful dangling cables in magenta, purple and blue, a tiny white lab coat over a black vest, translucent veined wings, on the left looking up; MONEY-ROBO, a cute small floating chibi robot with a large glossy rounded-square white head and a small rounded white body with thick black outlines, a black pill-shaped screen face showing golden-yellow pixel eyes and mouth, a small round knob antenna, stubby fingerless arms, a cyan pill-shaped core light, hovering on the right looking up; Haru, a cute anime girl lab assistant with long straight pink hair with navy blue streaks, two round hair buns, big bright blue eyes, a lavender hoodie under an open white lab coat, holding a blank three-column scoreboard; a pair of dice and a bell curve drawn on a side chalkboard, no text, no letters, no numbers, no logos, no weapons, no cigarettes, no alcohol, no blood, no real brands
```

## 3. 페이지별 대표 그림 모음
| 페이지 | 앵커 | bg | hero | thumb | 상태 |
|---|---|---|---|---|---|
| 1.1-2 확률질량·밀도 함수 | B 측정대 | bg_1_1_2 | sc_1_1_2_hero | thumb_1_1_2 | bg·hero 의뢰, thumb 만듦 |

## 4. 아이콘
icon_fly(초파리 머리), icon_robo(로봇 머리), icon_draw(저울), icon_dq(빨간 X) — 32·16px, 팩 192px 그림의 머리를 잘라 직접 만든다. 목차 페이지를 만들 때 함께 넣는다.

## 5. 매니페스트
```json
{ "series": "우연의 과학통계학",
  "shared": [
    {"key":"cover_series","plate":"J","maker":"external","status":"requested","priority":"P1"},
    {"key":"bg_index","plate":"F","maker":"external","status":"requested","priority":"P1"},
    {"key":"lineup","plate":"G","maker":"claude","status":"todo","priority":"P1"},
    {"key":"doc_scale","pack":"doc_e13","status":"pack-substitute","priority":"P2"}],
  "pages": [{"number":"1.1-2","bg":"bg_1_1_2","hero":"sc_1_1_2_hero","thumb":"thumb_1_1_2","duel":"F"}] }
```
