# GitHub Blog

## 폰트 수정 방법

### 폰트 크기 변경
1. /_sass/minimal-mistakes/_reset.scss
    - 여기서 원하는 크기로 수정해주기
    - 반응형 웹이므로 화면 크기에 따른 폰트를 모두 설정해주어야함
    - 현재 모바일 14, 나머지는 16폰트로 수정

```css
html {
  /* apply a natural box layout model to all elements */
  box-sizing: border-box;
  background-color: $background-color;
  font-size: 14px;

  @include breakpoint($medium) {
    font-size: 16px;
  }

  @include breakpoint($large) {
    font-size: 16px;
  }

  @include breakpoint($x-large) {
    font-size: 16px;
  }

  -webkit-text-size-adjust: 100%;
  -ms-text-size-adjust: 100%;
}
```

### 폰트 수정

> [리디바탕체](https://noonnu.cc/font_page/324)

1. /assets/fonts에 폰트파일 추가

2. assets/css/main.scss에 코드 추가

```css
@font-face {
    font-family: 'RIDIBatang';
    src: url('/assets/fonts/RIDIBatang.woff') format('woff');
    font-weight: normal;
    font-style: normal;
}
```

3. minimal-mistakes/_variables.scss 부분 수정

```d
/* system typefaces */
$serif: Georgia, Times, serif !default;
$sans-serif: "RIDIBatang", -apple-system, BlinkMacSystemFont, "Roboto", "Segoe UI",
  "Helvetica Neue", "Lucida Grande", Arial, sans-serif !default;
$monospace: Monaco, Consolas, "Lucida Console", monospace !default;
```

---

minimal-mistakes 기준