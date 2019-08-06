### 建立選單導航列navigation\(含 LOGO和選單\)

開始製作網頁選單Nav這個部分，由於Nav是包在Header裡面，所以要先寫`<Header></header>`，並把`<nav></nav>`包在面，&lt;nav&gt;要設定class，來設定風格，`navbar`為Bootstrap的內建選單，Bootstrap已經將CSS語法都寫在裡面了，所以我們就輸入名稱，把選單的風格呼叫進來，`navbar-dark`為深色選單，`bg-dark`為黑色背景，如下圖。

![](/assets/A01.jpg)

> 建立LOGO，將準備好的LOGO圖片置入HTML中

```html
 <a href="#" class="navbar-brand">
   <img src="images/logo.png" alt="logo" />
 </a>
```

> 利用ul、li 建立選單

```html
<div>
  <ul>
    <li><a href="#">產品</a></li>
    <li><a href="#">功能</a></li>
    <li><a href="#">創意</a></li>
    <li><a href="#">活動</a></li>
    <li><a href="#">規格</a></li>
  </ul>
</div>
```



