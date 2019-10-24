# 產品介紹區塊

一樣先寫**`<section></section>`**，再建立一個**`container`**，讓區塊有彈性，可以塞產品資料。



![](.gitbook/assets/image%20%2823%29.png)

在Bootstrap中，有一個[**`card`**](https://bootstrap.hexschool.com/docs/4.2/components/card/)元件，可以運用，所以我們將照片套入

```markup
<!-- 產品介紹區塊(創意) -->
  <section id="creative">
    <div class="container">
      <h2 class="text-center">
        智慧把手
      </h2>
      <!-- 產品照片 -->
      <div class="row">
        <div class="col">
          <div class="card">
            <img alt="產品照片1" src="images/function01.jpg">
          </div>
        </div>
      </div>



    </div>
  </section>

```

![](.gitbook/assets/image%20%2836%29.png)

商品照片下方要加入文字介紹

![](.gitbook/assets/image%20%2852%29.png)

設定CSS，美化標題和照片

![](.gitbook/assets/image%20%2832%29.png)

設定產品文字說明區塊

![](.gitbook/assets/image%20%2837%29.png)

![](.gitbook/assets/image%20%283%29.png)

```css
/* ------產品介紹區塊 ------*/

.creative_area {
    padding: 50px 0 100px 0;
}

.creative_area h2 {
    color: #6fafb4;
    margin: 20px 0 60px 0;
}

.creative_area .card img {
    width: 100%;
}

.creative_area .card h4 {
    color: #fff;
}


/* 把標題區塊card-title-wrap設定好位置 */

.creative_area .card-title-wrap {
    padding: 15px 25px;
    position: relative;
    z-index: 9;
    background-color: #fff;
}


/* 設定產品說明文字標題 */

.creative_area .card-title-wrap .card-title {
    display: block;
    margin: 0;
    font-size: 24px;
    color: #333;
}

.creative_area .card-title-wrap .card-text {
    display: block;
    margin: 0;
    font-size: 18px;
    color: #335
}


/* 滑鼠滑過去  */

.creative_area .card:hover {
    visibility: visible;
    background-color: #6fafb4;
}

.creative_area .card:hover .card-title-wrap {
    background-color: #6fafb4;
}


/* 滑鼠滑過照片變透明 */

.creative_area .pic-hover {
    padding-top: 45px;
    position: absolute;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.8);
    top: 0;
    left: 0;
    text-align: center;
    opacity: 0;
    visibility: hidden;
    transition: all 0.3s ease;
}

.creative_area .card:hover .pic-hover {
    opacity: .8;
    visibility: visible;
    color: #FFFFFF;
}
```

製作好一組完整的相片區塊後，直接複製一組，往下貼上，就有三組產品照片了

![](.gitbook/assets/image%20%2822%29.png)

