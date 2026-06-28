# 한자 메모리

한국어문회 공인한자능력시험 배정한자 기준의 한자 학습 웹 게임입니다.

## 현재 기능

- 8급, 7급II, 7급 선택
- 한자 카드와 뜻·음 카드 매칭
- 카드 수 선택
- 오늘의 미션, 보석, 스티커 보상
- 힌트, 섞기
- 틀린 단어 복습함
- 태블릿 대응 반응형 UI

## 실행

PC에서는 `index.html`을 브라우저로 열면 됩니다.

GitHub Pages에 올릴 경우 저장소 루트에 있는 `index.html`이 바로 실행됩니다.

## 파일 구조

```text
.
├── index.html
├── assets/
│   └── hanja-stickers-sprite.png
├── .nojekyll
└── README.md
```

## 배포 메모

GitHub Pages를 사용할 때는 상대 경로를 유지해야 합니다.

```css
url("assets/hanja-stickers-sprite.png")
```

처럼 작성되어 있어 저장소명 하위 경로에서도 동작합니다.
