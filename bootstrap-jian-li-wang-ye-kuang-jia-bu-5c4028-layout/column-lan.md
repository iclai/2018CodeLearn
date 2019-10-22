# Column欄

在Bootstrap中，&lt;div&gt;區塊欄位，會按照父類別的寬度大小來做改變，套用col會平均分配欄寬。

```markup
<div class="container">
        <div class="row">
            <div class="col bg-primary">ROEW1</div>
            <div class="col bg-danger">ROEW2</div>
            <div class="col bg-warning">ROEW3</div>
        </div>
    </div>
```

![](../.gitbook/assets/image.png)

使用 「col-數字」會讓Bootstrap做的的網頁非常有彈性，為何要讓網頁有彈性呢??

因為一般使用者在電腦瀏覽器看網頁，文章或是圖片都很清楚，一旦網頁轉換到手機或是平版時，卻會看到網頁跑版，或是圖片模糊的情況，所以透過Bootstrap斷點，就能讓網頁自動適應裝置畫面的尺寸。



