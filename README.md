# 포시즌키친 미디어

홈페이지(아임웹)에 쓰는 영상·이미지 파일. 아임웹은 mp4를 올릴 수 없어서
여기 올려두고 코드 위젯의 `<video src="...">`에서 주소로 불러온다.

작업 원본과 생성 스크립트는 `포시즌키친-홈페이지/영상/`에 있다.

## 파일

| 파일 | 용도 | 규격 |
|---|---|---|
| `hero/hero-desktop.mp4` | 메인 히어로 (PC) | 1920x1080 · 24fps · 3.6초 루프 |
| `hero/hero-mobile.mp4` | 메인 히어로 (모바일) | 1080x1920, 16:9 띠 900x506 |
| `hero/hero-*-poster.jpg` | 로딩 중 표시용 첫 프레임 | |

## 쓰는 법

```html
<video autoplay muted loop playsinline
       poster="https://ron789-glitch.github.io/fsk-media/hero/hero-desktop-poster.jpg">
  <source src="https://ron789-glitch.github.io/fsk-media/hero/hero-desktop.mp4" type="video/mp4">
</video>
```

## 파일을 바꿀 때

**같은 이름으로 덮어쓰면 방문자 브라우저와 CDN에 옛 파일이 남는다.**
내용을 바꿀 때는 파일명 뒤에 번호를 붙일 것 (`hero-desktop-2.mp4`).
