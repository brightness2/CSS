# 响应式联系信息
==教程地址==：[原文地址（YouTube）](https://youtu.be/7uEqQx4S50E)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av97306912/)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
<div class="contact-info">
  <div class="card">
    <i class="card-icon far fa-envelope"></i>
    <p>email@domain.com</p>
  </div>

  <div class="card">
    <i class="card-icon fas fa-phone"></i>
    <p>+000000000000</p>
  </div>

  <div class="card">
    <i class="card-icon fas fa-map-marker-alt"></i>
    <p>New York, USA</p>
  </div>
</div>
```
### CSS
```css
*{
  margin: 0;
  padding: 0;
  font-family: "montserrat",sans-serif;
  box-sizing: border-box;
}
body{
  background: #f1f1f1;
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}
.contact-info{
  display: flex;
  width: 100%;
  max-width: 1200px;
  align-items: center;
  justify-content: center;
  padding: 0 20px;
}


.card{
  background: #2f3542;
  padding: 0 20px;
  margin: 0 10px;
  width: calc(33% - 20px);
  height: 200px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  color: #fff;
  cursor: pointer;
}

.card-icon{
  font-size: 28px;
  background: #ff6348;
  width: 60px;
  height: 60px;
  text-align: center;
  line-height: 60px !important;
  border-radius: 50%;
  transition: 0.3s linear;
}

.card:hover .card-icon{
  background: none;
  color: #ff6348;
  transform: scale(1.6);
}

.card p{
  margin-top: 20px;
  font-weight: 300;
  letter-spacing: 2px;
  max-height: 0;
  opacity: 0;
  transition: 0.3s linear;
}

.card:hover p{
  max-height: 40px;
  opacity: 1;
}


@media screen and (max-width:800px) {
  .contact-info{
    flex-direction: column;
  }
  .card{
    width: 100%;
    max-width: 300px;
    margin: 10px 0;
  }
}

```
### JS
```javascript

```
==教程地址==：[原文地址（YouTube）](https://youtu.be/7uEqQx4S50E)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av97306912/)