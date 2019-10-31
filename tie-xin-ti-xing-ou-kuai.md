# 貼心提醒區塊

其實HTML框架語法就是不斷的重複區塊拼湊起來，寫久了，你會發現，都是差不多。

```markup
  <!-- 貼心提醒 -->
    <section>
        <div class="container content">
            <div class="row remind">
                <h4>貼心提醒</h4>
                <div class="w-100"></div>
                <p>使用時請留意：</p>
                <ul>
                    <li>烹調時把手請勿直接接觸火源。</li>
                    <li>請將烹調熱源控制於鍋底範圍，以免把手損壞。</li>
                    <li>鍋具把手視為鍋具本體耗材的一部分，若是損壞則無法維修。</li>
                </ul>
            </div>
        </div>
    </section>
```

```css
/* 貼心提醒 */

.content {
    position: relative;
    bottom: 0;
    color: #f1f1f1;
    width: 100%;
    padding: 20px;
}

.remind {
    padding: 20px;
    background: rgba(0, 0, 0, 0.3);
    color: #FFFFFF;
}
```

![](.gitbook/assets/image%20%281%29.png)

