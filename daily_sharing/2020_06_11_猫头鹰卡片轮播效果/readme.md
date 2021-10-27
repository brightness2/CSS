# 猫头鹰卡片轮播效果
==教程地址==：[原文地址（YouTube）](https://youtu.be/EG-sXgY1md4)

==B站教程==：[原文转载（bilibili）](此处键入链接)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
  <div class="slider owl-carousel">
    <div class="card">
      <div class="img">
        <img src="img/one.jpg" alt=""></div>
      <div class="content">
        <div class="title">
          Briana Tozour</div>
        <div class="sub-title">
          Graphic Designer</div>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odit modi dolorem quis quae animi nihil minus sed
          unde voluptas cumque.</p>
        <div class="btn">
          <button>Read more</button>
        </div>
      </div>
    </div>
    <div class="card">
      <div class="img">
        <img src="img/one.jpg" alt=""></div>
      <div class="content">
        <div class="title">
          Pricilla Preez</div>
        <div class="sub-title">
          Web Developer</div>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odit modi dolorem quis quae animi nihil minus sed
          unde voluptas cumque.</p>
        <div class="btn">
          <button>Read more</button>
        </div>
      </div>
    </div>
    <div class="card">
      <div class="img">
        <img src="img/one.jpg" alt=""></div>
      <div class="content">
        <div class="title">
          Eliana Maia</div>
        <div class="sub-title">
          App Developer</div>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odit modi dolorem quis quae animi nihil minus sed
          unde voluptas cumque.</p>
        <div class="btn">
          <button>Read more</button>
        </div>
      </div>
    </div>
  </div>
```
### CSS
```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
html, body {
  display: grid;  /* 网格布局 */
  height: 100%;
  place-items: center;
  text-align: center;
  background: #f2f2f2;
}
.slider{
  max-width: 1150px;
  display: flex;
}
.slider .card{
  flex: 1;
  margin: 0 10px;
}
.slider .card .img {
  height: 200px;
  width: 100%;
}
.slider .card .img img{
  height: 100%;
  width: 100%;
  object-fit: cover; /* 对象对齐模式 */
}
.slider .card .content {
  padding: 10px 20px;

}
.slider .card .content .title{
  font-size: 25px;
  font-weight: 600;
}
.slider .card .content .sub-tltle{
  font-size: 20px;
  font-weight: 600;
  color: #e74c3c;
  line-height: 20px;
}
.card .content .p {
  text-align: justify;  /* 字体对齐方式 */
  margin: 10px 0px;
}
.card .content .btn {
  display: block;
  text-align: left;
  margin: 10px 0;
}
.card .content .btn button {
  background: #e74c3c;
  color: #fff;
  border:none;
  outline: none; /* 轮廓 */
  font-size: 17px;
  padding: 5px 8px;
  border-radius: 5px;
  cursor: pointer;  /* 光标样式 */
}
.card .content .btn button:hover {
  transform: scale(0.9);  /* 倍率 */
}
```
### JS
```javascript
    $(".slider").owlCarousel({
      loop: true,
      autoplay: true,
      autoplayTimeout: 2000, //2000ms = 2s;
      autoplayHoverPause: true,
    });
```
==教程地址==：[原文地址（YouTube）](https://youtu.be/EG-sXgY1md4)

==B站教程==：[原文转载（bilibili）]()