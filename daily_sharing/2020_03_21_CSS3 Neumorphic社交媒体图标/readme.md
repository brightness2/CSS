# CSS3 Neumorphic社交媒体图标
==教程地址==：[原文地址（YouTube）](https://youtu.be/85tDF_h1Ci4)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av98594673)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
<div class="center">
  <div class="icons first">
    <li><a href="#"><span class="fab fa-facebook-f"></span></a></li>
    <li><a href="#"><span class="fab fa-twitter"></span></a></li>
    <li><a href="#"><span class="fab fa-instagram"></span></a></li>
    <li><a href="#"><span class="fab fa-linkedin-in"></span></a></li>
    <li><a href="#"><span class="fab fa-github"></span></a></li>
  </div>
  <div class="icons second">
    <li><a href="#"><span class="fab fa-facebook-f"></span></a></li>
    <li><a href="#"><span class="fab fa-twitter"></span></a></li>
    <li><a href="#"><span class="fab fa-instagram"></span></a></li>
    <li><a href="#"><span class="fab fa-linkedin-in"></span></a></li>
    <li><a href="#"><span class="fab fa-github"></span></a></li>
  </div>
</div>
```
### CSS
```css
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body{
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  text-align: center;
  background: #dde1e7;
  width: 100%;
}
.icons{
  display: flex;
  margin: 40px 0;
}
li{
  position: relative;
  list-style: none;
  height: 70px;
  width: 70px;
  margin: 0 10px;
  border-radius: 50%;
  background: #dde1e7;
  cursor: pointer;
  box-shadow: -3px -3px 7px #ffffff73,
              3px 3px 5px rgba(94,104,121,0.288);
}
li a{
  line-height: 70px;
  font-size: 27px;
  color: #b6bbc5;
}
.first li.shadow-1{
  box-shadow: inset -3px -3px 7px #ffffff73,
              inset 3px 3px 5px rgba(94,104,121,0.288);
}
.first li.shadow-1 a{
  font-size: 25px;
}
.second li.shadow-2 a{
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  height: 55px;
  width: 55px;
  line-height: 55px;
  border-radius: 50%;
  background: #dde1e7;
  font-size: 24px;
  box-shadow: inset -3px -3px 7px #ffffff73,
              inset 3px 3px 5px rgba(94,104,121,0.288);
}
li:nth-child(1).fill-color a{
  color: #4267B2;
}
li:nth-child(2).fill-color a{
  color: #1DA1F2;
}
li:nth-child(3).fill-color a{
  color: #E1306C;
}
li:nth-child(4).fill-color a{
  color: #2867B2;
}
li:nth-child(5).fill-color a{
  color: #333;
}

```
### JS
```javascript
$('.first li').click(function(){
  $(this).toggleClass("shadow-1").siblings();
  $(this).toggleClass("fill-color").siblings();
});
$('.second li').click(function(){
  $(this).toggleClass("shadow-2").siblings();
  $(this).toggleClass("fill-color").siblings();
});
```
==教程地址==：[原文地址（YouTube）](https://youtu.be/85tDF_h1Ci4)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av98594673)