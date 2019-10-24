# 網頁影片區塊

```markup
  <section class="container">
    <iframe width="640" height="360" src="https://www.youtube.com/embed/mNBxwGghQAY" frameborder="0"
      allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </section>

```

![](.gitbook/assets/image%20%289%29.png)

我要'讓影片背景變成黑色，並且與上方輪播圖拉開距離，所以我下了一個class，來設定它，為了要讓黑色撐開背景，所以把**`containe`**改成**`container-fluid`**

```css
/* ------ 影片 ------ */

.video-area {
  padding: 5% 20%;
  background-color: #272727;
}
```

![](.gitbook/assets/image%20%2840%29.png)

目前影片還無法自動縮放，瀏覽器縮小，影片會被遮住

![](.gitbook/assets/image%20%2831%29.png)

```css
.video-container {
  position: relative;
  padding: 30%;
  overflow: hidden;
}

.video-container iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

```

加上以上CSS，影片就會符合螢幕大小自動縮放

![](.gitbook/assets/image%20%2830%29.png)

