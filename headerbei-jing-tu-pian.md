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

![&#x5982;&#x4E0A;&#x5716;&#xFF0C;&#x80CC;&#x666F;&#x5716;&#x7247;&#x5DF2;&#x7D93;&#x5728;&#x7DB2;&#x9801;&#x4E2D;](.gitbook/assets/i02.jpg)

為了測試背景效果，我們在下方`<section> </section>`中輸入一些假字，撐起網頁。

![](.gitbook/assets/i01.jpg)

![&#x7DB2;&#x9801;&#x9810;&#x89BD;&#x5F8C;&#xFF0C;&#x5047;&#x5B57;&#x5728;&#x5716;&#x7247;&#x4E0A;&#x65B9;&#x5B8C;&#x5168;&#x84CB;&#x4F4F;&#xFF0C;&#x8868;&#x793A;&#x5982;&#x679C;&#x662F;&#x5225;&#x7684;&#x7DB2;&#x9801;&#x5167;&#x5BB9;&#x4E5F;&#x6703;&#x5168;&#x90E8;&#x84CB;&#x4F4F;&#x80CC;&#x666F;&#x3002;](.gitbook/assets/i04.jpg)

當然，我們不希望下方網頁內容將背景全部蓋住，所以希望假字可以在背景之下。所以要給背景圖片一個高度，讓圖片撐起頁面，也將假字往下推。

並希望下方背景在滑鼠往下瀏覽頁面時，背景圖可以固定在原本的位置不動，所以接著，設定圖片符合螢幕高度100%。給圖片加入一個ID名稱`main-banner` ，並包住背景圖片div。

```markup
   <div class="bg-image bg-parallax"></div>
 </div>
```

```css
#main-banner {
  height: 100vh;  /*vh是view height，指螢幕可視範圍高度的百分比*/
}
.bg-parallax {
  background-attachment: fixed;
}
```

![&#x5716;&#x7247;&#x9AD8;&#x5EA6;&#x8A2D;&#x5B9A;&#x5F8C;&#xFF0C;&#x4E0B;&#x65B9;&#x5047;&#x5B57;&#x5167;&#x5BB9;&#x6703;&#x5F80;&#x4E0B;&#x6392;&#x5217;](.gitbook/assets/i03.jpg)

一頁式網頁，會一直往下瀏覽，但我們不希望導覽列選單會因為我們網頁往下滑，而必須回頭來找選單，所以記得選單要設定讓它在網頁往下滑時，固定在表頭，這樣就算滑到最下面也可以很容易在螢幕範圍內點擊選單到我們要的資訊頁面。

![](.gitbook/assets/i06.jpg)

```css
.navbar {
  position: fixed;
  right: 0;
  left: 0;
  top: 0;
  margin: auto;
  z-index: 999;
}
```

