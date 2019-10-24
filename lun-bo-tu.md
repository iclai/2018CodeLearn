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

![](.gitbook/assets/image%20%2822%29.png)

### 圖片置入

**`carousel-item`** 表示圖片的項目，**`active`**，告訴瀏覽器從這一張開始撥放

![](.gitbook/assets/image%20%283%29.png)

複製 圖片1寫好的程式區塊，往下貼上，並修改圖片路徑的名稱

![](.gitbook/assets/image%20%287%29.png)



