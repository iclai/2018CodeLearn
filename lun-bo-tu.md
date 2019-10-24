# 輪播圖

建立輪播圖要的section區域，class設定 carousel， 告訴Bootstrap要引用它的輪播功能。 

![](.gitbook/assets/image%20%285%29.png)

數據加載方式也是carousel，所以後面要加入**`data-ride="carousel"`**

```markup
 <div class="carousel" data-ride="carousel">
```

創建好輪播圖區域後，就要加入輪播圖片，要在內部輪播的圖片

```markup
 <div class="carousel-inner">
```

![](.gitbook/assets/image%20%2824%29.png)

### 圖片置入

**`carousel-item`** 表示圖片的項目，**`active`**，告訴瀏覽器從這一張開始撥放

![](.gitbook/assets/image%20%283%29.png)

複製 圖片1寫好的程式區塊，往下貼上，並修改圖片路徑的名稱，可以看到圖片是很大的而且已經會自己輪播。

![](.gitbook/assets/image%20%287%29.png)

我們希望相片輪播的方式可以用滑動的，而不是用跳動的，所以要在輪播圖最外框的div加上一個 **`slide`** , 這樣圖片就換傳變成滑動

相片加入 **`class="w-100"`** 讓圖片可以自適設備螢幕的大小

![](.gitbook/assets/image%20%2821%29.png)

```markup
  <!-- 可以輪播的Banner圖片 -->
  <section>
    <div class="carousel slide" data-ride="carousel">
      <!-- 輪播圖片 -->
      <div class="carousel-inner">
        <!-- 圖片1 -->
        <div class="carousel-item active">
          <img class="w-100" src="images/Banner1.jpg" alt="">
        </div>
        <!-- 圖片2 -->
        <div class="carousel-item">
          <img class="w-100" src="images/Banner2.jpg" alt="">
        </div>
        <!-- 圖片3 -->
        <div class="carousel-item">
          <img class="w-100" src="images/Banner3.jpg" alt="">
        </div>


      </div>
    </div>
  </section>

```

### 設定圖片上下頁按鈕

按鈕 要和 輪播圖有連結性，所以要在輪播圖的最外面的div 加上ID 名稱，這樣按鈕才知道要對應到哪一個名稱

```markup
 <div id="carousel-controller" class="carousel slide" data-ride="carousel">
```

![](.gitbook/assets/image%20%2811%29.png)

