# Bootstrap 安裝

![](.gitbook/assets/bootstrap4.jpg)

我們要使用 Bootstrap 4來建立網頁，所以要將Bootstrap 框架引入網頁中 ，請先開啟[_Bootstrap 首頁_](https://bootstrap.hexschool.com/)。

> 安裝 Bootstrap 有 2 種方式

1. 使用外部連結到網頁中。
2. 直接將bootstrap 檔案下載至網頁資料夾中，使用內部連結。

**外部連結** ， 點擊首頁的 **Get started** ，將CSS 樣式路徑複製貼進網頁_&lt;head&gt;_與_&lt;/head&gt;_之間。

```markup
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.2.1/css/bootstrap.min.css" integrity="sha384-GJzZqFGwb1QTTN6wy59ffF1BuGJpLSa9DkKMp0DgiMDm4iYMj70gZWKYbI706tWS" crossorigin="anonymous">
```

接著將將JavaScrapt 組件複製貼進網頁的_&lt;/body&gt;_結尾之前。

```markup
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.6/umd/popper.min.js" integrity="sha384-wHAiFfRlMFy6i5SRaxvfOCifBUQy1xHdJ/yoi7FRNXMRBu5WHdZYu1hA6ZOblgut" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.2.1/js/bootstrap.min.js" integrity="sha384-B0UglyR+jN6CkvvICOB2joaf5I4l3gm9GU6Hc1og6Ls7i6U/mkkaduKaBhlAXv9k" crossorigin="anonymous"></script>
```

![](.gitbook/assets/image%20%2823%29.png)

> 引入 _jquery-3.3.1.slim.min.js、bootstrap.min.js、bootstrap.min.js_ 這三個JS組件，主要會運用在以下功能

* Alerts for dismissing \(解除警報\)
* Buttons for toggling states and checkbox/radio functionality \(按鈕切換功能和選項按鈕功能\)
* Carousel for all slide behaviors, controls, and indicators\(幻燈片撥放控制和輪播功能\)
* Collapse for toggling visibility of content\(摺疊切換，如手機版漢堡選單\)
* Dropdowns for displaying and positioning \(顯示和定位，下拉選單，也需要[Popper.js](https://popper.js.org/)\)
* Modals for displaying, positioning, and scroll behavior \(顯示和定位和捲動行為組態\)
* Navbar for extending our Collapse plugin to implement responsive behavior\(導航列的擴和折疊插件，用來實現響應式行為\)
* Tooltips and popovers for displaying and positioning \(提示和彈出框工具的顯示與定位，也需要 [Popper.js](https://popper.js.org/)\)
* Scrollspy for scroll behavior and navigation updates\(滾動監聽行為，自動更新導航外掛，會根據滾動條的位置自動更新對應的導航目標。\)

