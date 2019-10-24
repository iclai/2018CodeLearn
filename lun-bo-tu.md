# 輪播圖

建立輪播圖要的section區域，class設定 carousel， 告訴Bootstrap要引用它的輪播功能。 

![](.gitbook/assets/image%20%288%29.png)

數據加載方式也是carousel，所以後面要加入**`data-ride="carousel"`**

```markup
 <div class="carousel" data-ride="carousel">
```

創建好輪播圖區域後，就要加入輪播圖片，要在內部輪播的圖片

```markup
 <div class="carousel-inner">
```

![](.gitbook/assets/image%20%2848%29.png)

### 圖片置入

**`carousel-item`** 表示圖片的項目，**`active`**，告訴瀏覽器從這一張開始撥放

![](.gitbook/assets/image%20%285%29.png)

複製 圖片1寫好的程式區塊，往下貼上，並修改圖片路徑的名稱，可以看到圖片是很大的而且已經會自己輪播。

![](.gitbook/assets/image%20%2811%29.png)

我們希望相片輪播的方式可以用滑動的，而不是用跳動的，所以要在輪播圖最外框的div加上一個 **`slide`** , 這樣圖片就換傳變成滑動

相片加入 **`class="w-100"`** 讓圖片可以自適設備螢幕的大小

![](.gitbook/assets/image%20%2843%29.png)

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

![](.gitbook/assets/image%20%2822%29.png)

按鈕串聯圖片的ID名稱 carousel-controller

```markup
<a href="#carousel-controller" data-slide="prev" class="carousel-control-prev"></a>
```

![](.gitbook/assets/image%20%2835%29.png)

左邊已經出現按鈕區域

```markup
<span class="carousel-control-prev-icon"></span>
```

&lt;span&gt; 引入Bootstrap的 ICON，輪播圖上，就會出現上一頁的icon按鈕

![](.gitbook/assets/image%20%282%29.png)

下一頁的按鈕，就複製上一頁寫好的語法，往下貼上，並將prev，全都修改成next，下一頁的按鈕就出現了

![](.gitbook/assets/image%20%2847%29.png)

### 輪播點點按鈕

```markup
 <ol class="carousel-indicators">
     <li data-target="#carousel-controller"></li>
  </ol>
```

**`carousel-indicators`** 輪播指向哪張圖，**`data-target="#carousel-controller"`** 目標是圖片的ID名稱

![](.gitbook/assets/image%20%2849%29.png)

data-slide-to="0" ，資料要連結到哪一張圖片，class="active"，圖片開啟連結關聯性。

data-slide-to，數字如同陣列一樣，從0開始算圖片第1張，1則為圖片的第2張，2為圖片的第3張

![](.gitbook/assets/image%20%2855%29.png)

### 加入大標題

```markup
 <div class="carousel-caption">
```

在每張輪播圖中，加入標題，carousel-caption，加入字幕的意思

![](.gitbook/assets/image%20%2818%29.png)

```markup
 <!-- 可以輪播的Banner圖片 -->
  <section>
    <div id="carousel-controller" class="carousel slide" data-ride="carousel">
      <!-- 輪播圖片 -->
      <div class="carousel-inner">
        <!-- 圖片1 -->
        <div class="carousel-item active">
          <img class="w-100" src="images/Banner1.jpg" alt="">
          <div class="carousel-caption">
            <h1>檢驗合格</h1>
            <p>塗層光滑 不沾易洗</p>
          </div>
        </div>
        <!-- 圖片2 -->
        <div class="carousel-item">
          <img class="w-100" src="images/Banner2.jpg" alt="">
          <div class="carousel-caption">
            <h1>智慧把手</h1>
            <p>鍋具輕鬆轉換 美味直接盛盤</p>
          </div>
        </div>
        <!-- 圖片3 -->
        <div class="carousel-item">
          <img class="w-100" src="images/Banner3.jpg" alt="">
          <div class="carousel-caption">
            <h1>圓弧設計</h1>
            <p>堆疊收納 節省空間</p>
          </div>
        </div>
      </div>
      <!-- 圖片上一頁按鈕 -->
      <a href="#carousel-controller" data-slide="prev" class="carousel-control-prev">
        <span class="carousel-control-prev-icon"></span>
      </a>
      <!-- 圖片下一頁按鈕 -->
      <a href="#carousel-controller" data-slide="next" class=" carousel-control-next">
        <span class="carousel-control-next-icon"></span>
      </a>

      <!-- 下方點點 -->
      <ol class="carousel-indicators">
        <li data-target="#carousel-controller" data-slide-to="0" class="active"></li>
        <li data-target="#carousel-controller" data-slide-to="1"></li>
        <li data-target="#carousel-controller" data-slide-to="2"></li>
      </ol>
    </div>
  </section>
```

