# 수학 펫 배틀 이미지 에셋 목록

## 제작 기준

- 전체 스타일: 밝은 픽셀아트, 조련사-펫 배틀 RPG, 저학년 대상
- 기본 언어: 한글
- 기본 배경 제거 방식: 생성 이미지는 원본 보존 후 워크스페이스에 정리
- 파일명 규칙: 영문 소문자와 하이픈 사용
- 우선순위: MVP 전투 루프에 필요한 에셋부터 제작

## 1차 제작 에셋

| 파일 | 이름 | 분류 | 용도 | 상태 |
| --- | --- | --- | --- | --- |
| `characters/trainer-arin.png` | 조련사 아린 | 캐릭터 | 후방 지시자, 기본 플레이어 | 제작 완료 |
| `pets/pet-momo.png` | 모모 | 펫 | 공격형, 정답 시 2회 공격 | 제작 완료 |
| `pets/pet-lulu.png` | 루루 | 펫 | 방어형, 오답 보호막 | 제작 완료 |
| `pets/pet-tori.png` | 토리 | 펫 | 속공형, 연속 정답 보너스 | 제작 완료 |
| `pets/pet-popo.png` | 포포 | 펫 | 회복형, 정답 시 회복 | 제작 완료 |
| `enemies/enemy-number-jelly.png` | 숫자젤리 | 적 | 초반 기본 적 | 제작 완료 |
| `enemies/enemy-plus-acorn.png` | 덧셈도토리 | 적 | 초반 보상 적 | 제작 완료 |
| `enemies/enemy-minus-crab.png` | 뺄셈게 | 적 | 해변 스테이지 적 | 제작 완료 |
| `items/item-star-collar.png` | 별목걸이 | 장비 | 공격형 특성 강화 | 제작 완료 |
| `items/item-shield-badge.png` | 방패배지 | 장비 | 오답 피해 감소 | 제작 완료 |
| `items/item-focus-cookie.png` | 집중쿠키 | 소비 | 선택지 하나 제거 | 제작 완료 |
| `items/item-hint-compass.png` | 힌트나침반 | 소비 | 정답 후보 강조 | 제작 완료 |
| `currency/currency-star-coin.png` | 별코인 | 재화 | 상점 구매 | 제작 완료 |
| `currency/currency-answer-gem.png` | 정답보석 | 재화 | 펫 해금/특성 강화 | 제작 완료 |
| `backgrounds/bg-forest-academy.png` | 숲속 학원길 | 배경 | 1장 전투 배경 | 제작 완료 |
| `ui/ui-korean-battle-icons.png` | 전투 UI 아이콘 | UI | 정답, 오답, 특성, 장비 아이콘 | 제작 완료 |
| `preview-contact-sheet.png` | 에셋 프리뷰 | 확인용 | 1차 에셋 전체 미리보기 | 제작 완료 |

## 2차 확장 에셋

| 이름 | 분류 | 용도 |
| --- | --- | --- |
| 비비 | 펫 | 보상형 펫 |
| 코코 | 펫 | 안정형 펫 |
| 시계버섯 | 적 | 시간 제한 문제 적 |
| 상자미믹 | 적 | 보너스 상자 적 |
| 반짝간식 | 성장 아이템 | 펫 경험치 증가 |
| 회복젤리 | 소비 아이템 | 펫 HP 회복 |
| 행운주머니 | 장비 | 별코인 획득량 증가 |
| 연습연필 | 소비 아이템 | 오답 1회 무효 |
| 해변길 배경 | 배경 | 2장 전투 배경 |
| 상점 배경 | 배경 | 상점 화면 |

## 2차 제작 완료 에셋

월드맵 기본 진입, 선명한 전투 배경, 전투 피드백 이펙트, 지역 이동형 상점 구조를 위한 에셋이다.

| 파일 | 이름 | 분류 | 용도 | 상태 |
| --- | --- | --- | --- | --- |
| `world/world-map-hub.png` | 수학 월드맵 | 배경 | 수학모드 기본 진입 화면 | 제작 완료 |
| `backgrounds/bg-forest-academy-vivid.png` | 선명한 숲속 학원길 | 배경 | 흰 레이어 없는 전투 배경 | 제작 완료 |
| `locations/location-landmarks-sheet.png` | 지역 랜드마크 시트 | 오브젝트 | 전투 숲길, 펫 목장, 장비 상점, 아이템샵, 연습장 등 지도 아이콘 | 제작 완료 |
| `effects/effect-battle-feedback-sheet.png` | 전투 피드백 이펙트 시트 | 이펙트 | 정답, 오답, 두번공격, 보호막, 회복, 보상 연출 | 제작 완료 |
| `backgrounds/bg-equipment-shop.png` | 장비 상점 배경 | 배경 | 장비 구매/장착 화면 | 제작 완료 |
| `backgrounds/bg-item-shop.png` | 아이템샵 배경 | 배경 | 소비 아이템 구매 화면 | 제작 완료 |
| `backgrounds/bg-pet-ranch.png` | 펫 목장 배경 | 배경 | 펫 선택/성장/관리 화면 | 제작 완료 |
| `preview-contact-sheet-v2.png` | 2차 에셋 프리뷰 | 확인용 | 2차 에셋 전체 미리보기 | 제작 완료 |

## 개별 제작 완료 에셋

좌표값으로 시트를 자르는 과정에서 생기는 오차를 줄이기 위해, 월드맵 오브젝트와 전투 이펙트, 공통 UI 아이콘을 각각 단일 투명 PNG로 분리 제작했다. 실제 게임 구현에서는 아래 `single` 폴더의 파일을 우선 사용한다.

### 월드맵 랜드마크

- 경로: `assets/math-pet-battle/locations/single/`
- 수량: 16개
- 파일: `battle-forest-gate.png`, `pet-ranch.png`, `equipment-shop.png`, `item-shop.png`, `practice-yard.png`, `reward-chest.png`, `locked-beach-gate.png`, `stage-node-pedestal.png`, `boss-gate.png`, `home-academy.png`, `coin-bank.png`, `answer-gem-shrine.png`, `healing-fountain.png`, `bridge-checkpoint.png`, `signpost.png`, `market-wagon.png`

### 전투 피드백 이펙트

- 경로: `assets/math-pet-battle/effects/single/`
- 수량: 16개
- 파일: `correct-burst.png`, `wrong-puff.png`, `double-hit-water-star.png`, `leaf-shield-barrier.png`, `healing-sparkle.png`, `speed-lightning.png`, `enemy-impact-star.png`, `damage-pop-burst.png`, `combo-flame.png`, `reward-coin-sparkle.png`, `answer-gem-sparkle.png`, `next-stage-portal.png`, `success-confetti.png`, `counterattack-swipe.png`, `pet-command-glow.png`, `cooldown-clock-shimmer.png`

### 공통 UI 아이콘

- 경로: `assets/math-pet-battle/ui/single/`
- 수량: 16개
- 파일: `correct-check.png`, `wrong-x.png`, `trait-sparkle.png`, `shield.png`, `attack-burst.png`, `heal-heart.png`, `speed-lightning.png`, `bag.png`, `shop.png`, `gear.png`, `pet-paw.png`, `stage-flag.png`, `hint-compass.png`, `cooldown-clock.png`, `home.png`, `back-arrow.png`

### 검수용 프리뷰

- `assets/math-pet-battle/preview-contact-sheet-single-assets.png`
- 개별 제작분 48개를 한 화면에서 확인하기 위한 프리뷰 시트

## 생성 프롬프트 공통 조건

- 귀엽고 독창적인 픽셀아트
- 포켓몬, 디지몬 등 기존 IP와 직접 닮지 않게 제작
- 작은 화면에서도 형태가 읽히는 강한 실루엣
- 한글 텍스트가 필요한 UI 에셋은 글자 수를 짧게 유지
- 캐릭터/펫/아이템은 게임 내 배치가 쉬운 단일 피사체 중심
