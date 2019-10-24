# 商品文案區塊

商品文案說明介紹，背景是影片

```markup
 <!-- 商品文案 -->
    <section>
        <div class="container">
            <div class="row">
                <div class="creative_text">
                    <h3>日常的家常</h3>
                    <p>每天上午 第一顆太陽蛋</br>
                        下班回家 來一鍋蔬菜湯</br>
                        料理食材簡單</br>
                        下廚卻如此複雜…
                    </p>
                    <h3>定義廚藝新時尚</h3>
                    <p>可拆式把手設計</br>
                        鍋具餐具二合一</br>
                        圓弧流線造型</br>
                        好收納好清潔
                    </p>
                    <h1>halla malmo</h1>
                    <p>生活的設計感 設計的生活感</br>
                        給您兼顧機能與風格用品
                    </p>
                </div>
            </div>
        </div>

        <!-- 背景影片 -->
        <div class="container">
            <video autoplay muted loop id="myVideo">
                <source src="video/egg.mp4" type="video/mp4">
            </video>
        </div>
    </section>

```

![](.gitbook/assets/image%20%2829%29.png)

```css
/* 商品文案 */

.article_text h3 {
    color: #ffffff;
    margin: 10px 0;
    letter-spacing: .5rem;
}

.article_text h1 {
    color: #6fafb4;
    margin: 10px 0;
}

.article_text p {
    color: #dbdddd;
    line-height: 2rem;
    letter-spacing: 0.2rem;
    margin-bottom: 50px;
}


/* ------ 背景影片 ------ */

#myVideo {
    position: fixed;
    right: 0;
    bottom: 0;
    /* max-width 會讓影隨著螢幕大小改變，
    min-width就只會維持影片原尺寸! */
    min-width: 100%;
    min-height: 100%;
    z-index: -1;
    opacity: .5;
}
```

