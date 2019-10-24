# 產品介紹區塊

一樣先寫**`<section></section>`**，再建立一個**`container`**，讓區塊有彈性，可以塞產品資料。



![](.gitbook/assets/image%20%2819%29.png)

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

![](.gitbook/assets/image%20%2829%29.png)

