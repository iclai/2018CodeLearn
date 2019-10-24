---
description: Bootstrap 為現今網頁開發中，被運用最廣泛的 CSS 框架，也是運用了網格系統
---

# Bootstrap 4 Grid System

Bootstrap提供的格線系統，也是一樣的概念，將版面區分成 `column` 和 `row`，並平均分割成12等分。

![](../.gitbook/assets/image%20%286%29.png)

### [版面縮小](https://getbootstrap.com/docs/3.4/css/)

![](../.gitbook/assets/image%20%2811%29.png)

### container容器

container是Bootstrap網格系統佈局使用的容器，也是最根本的排版元素，非常重要，使用時會因應每個響應式斷點來更改寬度。

![](../.gitbook/assets/image%20%2820%29.png)

```markup
 <!-- col -->
    <div class="container">
        <div class="row col12">
            <div class="col">
                XS (576px) class: col-*
            </div>
        </div>
        <div class="row">
            <div class="col col4">
                3格
            </div>
            <div class="col col4">
                3格
            </div>
            <div class="col col4">
                3格
            </div>
        </div>
    </div>
    <!-- col sm -->
    <div class="container">
        <div class="row colsm">
            <div class="col-sm">
                sm (≥576px) class: col-sm-*
            </div>
        </div>
        <div class="row">
            <div class="col-sm-3 sm3">
                3格
            </div>
            <div class="col-sm-6 sm3">
                6格
            </div>
            <div class="col-sm-3 sm3">
                3格
            </div>
        </div>
    </div>
    <!-- col md -->
    <div class="container">
        <div class="row colmd">
            <div class="col-md">
                md (≥768px) class: col-md-*
            </div>
        </div>
        <div class="row">
            <div class="col-md-1 md3">
                第1格
            </div>
            <div class="col-md-1 md3">
                第2格
            </div>
            <div class="col-md-1 md3">
                第3格
            </div>
            <div class="col-md-1 md3">
                第4格
            </div>
            <div class="col-md-1 md3">
                第5格
            </div>
            <div class="col-md-1 md3">
                第6格
            </div>
            <div class="col-md-1 md3">
                第7格
            </div>
            <div class="col-md-1 md3">
                第8格
            </div>
            <div class="col-md-1 md3">
                第9格
            </div>
            <div class="col-md-1 md3">
                第10格
            </div>
            <div class="col-md-1 md3">
                第11格
            </div>
            <div class="col-md-1 md3">
                第12格
            </div>
        </div>
    </div>

    <!-- col lg -->
    <div class="container">
        <div class="row collg">
            <div class="col-lg">
                lg (≥992px) class: col-lg-*
            </div>
        </div>
        <div class="row">
            <div class="col-lg-2 lg2">
                2格
            </div>
            <div class="col-lg-2 lg2">
                2格
            </div>
            <div class="col-lg-2 lg2">
                2格
            </div>
            <div class="col-lg-2 lg2">
                2格
            </div>
            <div class="col-lg-2 lg2">
                2格
            </div>
            <div class="col-lg-2 lg2">
                2格
            </div>
        </div>
    </div>
    <!-- col xl -->
    <div class="container">
        <div class="row colxl">
            <div class="col-xl">
                xl (≥1200px) class: col-xl-*
            </div>
        </div>
        <div class="row">
            <div class="col-xl-9 xl6">
                9格
            </div>
            <div class="col-xl-3 xl6">
                3格
            </div>
        </div>
```

### Media Queries 的分段點 <a id="media-queries-&#x7684;&#x5206;&#x6BB5;&#x9EDE;"></a>

* @media\(min-width:576px\){ 當裝置畫面寬度為576px或是576px以上就執行這個樣式 }
* @media\(min-width:768px\){ 當裝置畫面寬度為768px或是768px以上就執行這個樣式 }
* @media\(min-width:992px\){ 當裝置畫面寬度為992px或是992px以上就執行這個樣式 }
* @media\(min-width:1200px\){ 當裝置畫面寬度為1200x或是1200px以上就執行這個樣式 }

container設定有分2種，一種是**`container`**，另一種是**`container-fluid`**。

container，無論瀏覽器有多大多小，兩側會有留白\(Grid padding\)

container-fluid則會將原本兩側的留白，全部100%填滿

![](../.gitbook/assets/image%20%287%29.png)

