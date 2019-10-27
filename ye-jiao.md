# 頁腳

```markup
<!-- 頁腳 -->
    <footer class="footer">
        <div class="container">
            <div class="row">
                <div class="col-md-8 col-sm-12 footer_logo">
                    <img src="images/logo_blue.png">
                </div>
                <div class="col-md-4 col-sm-12 footer_address">
                    <ul>
                        <li>專 線：04-33556688</li>
                        <li>服務時間：週一至週五 9:00 ~ 18:00</li>
                        <li>服務信箱：service@gmail.com</li>
                    </ul>
                </div>
            </div>
            <div class="row footer_copyright justify-content-center">
                <p>COPYRIGHT © 2019 halla malmo .ALL RIGHTS RESERVED.</p>
            </div>
        </div>
    </footer>
```

Bootstrap有許多內建針對網頁網格管理排版的對其方式，可以自行閱讀bootstrap網頁使用說明。

**\`\`**[**`justify-content-cente`**](https://bootstrap.hexschool.com/docs/4.0/utilities/flex/)**我要讓頁腳文字區塊置中，當然你可以不只有文字，也可以置入圖片**

**\`\`**

```css
/* 頁腳 */

.footer {
    background-color: #e6e6e6;
    padding: 15px 0;
}

.footer_logo img {
    max-width: 100px;
}

.footer_address ul {
    list-style-type: none;
    font-size: 14px;
    line-height: 1.2rem;
    color: #5e5e5e;
}

.footer_copyright {
    font-size: 10px;
}
```

![](.gitbook/assets/image%20%2834%29.png)

