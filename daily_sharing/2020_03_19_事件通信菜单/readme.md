# 事件通信菜单
==教程地址==：[原文地址（YouTube）](https://youtu.be/I7M3V5sBMQc)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av97307629/)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
<!-- https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.11.2/css/all.css -->
<div class="newsletter">
  <h1>
    Monthly
    <span>Newsletter</span>
  </h1>

  <p>Lorem ipsum dolor sit amet, natus sequi maxime assumenda.</p>

  <div class="txtb">
    <input type="text" placeholder="Enter Your Email Address">
    <button type="button"><i class="fas fa-arrow-right"></i></button>

  </div>
</div>
```
### CSS
```css
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Open Sans",sans-serif;
}

body{
  background: #786fa6;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

.newsletter{
  background: linear-gradient(125deg,#778beb,#f8a5c2);
  width: 500px;
  padding: 60px;
  text-align: center;
  box-shadow: 0 0 20px #00000060;
}

.newsletter h1{
  text-transform: uppercase;
  color: #fff;
  font-size: 48px;
  line-height: 40px;
}

.newsletter h1 span{
  display: block;
  font-size: 38px;
}

.newsletter p{
  color: #fff;
  font-size: 14px;
  margin: 10px 0;
}

.txtb{
  width: 100%;
  height: 70px;
  background: #f1f1f199;
  border-radius: 40px;
  position: relative;
  margin-top: 40px;
}

.txtb input{
  width: 100%;
  height: 70px;
  border-radius: 40px;
  border: 0;
  background: none;
  padding: 0 30px;
  outline: none;
  font-size: 15px;
  padding-right: 80px;
}

.txtb button{
  background: #574b90;
  border: 0;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  position: absolute;
  right: 10px;
  top: 10px;
  outline: none;
  cursor: pointer;
  color: #fff;
  transition: 0.3s linear;
}

.txtb button:hover{
  opacity: .5;
}

```
### JS
```javascript

```
==教程地址==：[原文地址（YouTube）](https://youtu.be/I7M3V5sBMQc)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av97307629/)