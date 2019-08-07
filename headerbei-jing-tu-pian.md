---
description: 製作抬頭Banner，將其背景填滿
---

# header背景圖片

我們要製作Header裡面的Banner，因為我們的Banner是要填滿背景，上方要押抬頭標題，所以請先將背景圖片準備好。

```markup
<div class="bg-image"></div>
```

輸入div，並設定其class 名稱`bg-image(可自行定義)`和屬性，在CSS中把圖片叫進來。

```css
.bg-image {
  background-image: url(images/banner.jpg);  /*自己的電腦圖片資料夾位置*/
  position: absolute;  /*絕對位置*/
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  background-position: center;
  background-size: cover;
  z-index: -999; /*設定圖片層級*/
}
```



