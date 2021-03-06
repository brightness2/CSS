# css制作悬停效果按钮
==教程地址==：[原文地址（YouTube）](https://youtu.be/MLfAW55_4cY)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av91021280)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
<div class="container">
  <button class="btn btn1">Hover Me</button>
  <button class="btn btn2">Hover Me</button>
  <button class="btn btn3">Hover Me</button>
  <button class="btn btn4">Hover Me</button>
</div>
```
### CSS
```css
body{
  margin: 0; /* 外边距 */
  padding: 0; /* 内边距 */
}
.container{
  text-align: center; /* 字体水平居中 */
  margin-top: 360px;
}
.btn{
  border: 1px solid #3498db; /* 边框 */
  background: none; /* 背景无 */
  padding: 10px 20px;
  font-size: 20px; /* 字体大小 */
  font-family: "montserrat"; /* 字体样式 */
  cursor: pointer; /* 鼠标样式 */
  margin: 10px;
  transition: 0.8s; /* 等待时间 */
  position: relative; /* 相对定位 */
  overflow: hidden; /* 溢出隐藏 */
}
.btn1,.btn2{
  color: #3498db; /* 颜色 */
}
.btn3,.btn4{
  color: #fff;
}
.btn1:hover,.btn2:hover{ /* 悬停时更改颜色 */
  color: #fff;
}
.btn3:hover,.btn4:hover{
  color: #3498db;
}
.btn::before{ /* 之前添加 */
  content: ""; /* 内容 */
  position: absolute; /* 绝对定位 */
  left: 0;
  width: 100%;
  height: 0%;
  background: #3498db;
  z-index: -1; /* 图层显示顺序 */
  transition: 0.8s;
}
.btn1::before,.btn3::before{
  top: 0;
  border-radius: 0 0 50% 50%; 
}
.btn2::before,.btn4::before{
  bottom: 0;
  border-radius: 50% 50% 0 0;
}
.btn3::before,.btn4::before{
  height: 180%; /* 通过修改高度实现显示 */
}
.btn1:hover::before,.btn2:hover::before{
  height: 180%;
}
.btn3:hover::before,.btn4:hover::before{
  height: 0%;
}

```
### JS
```javascript

```
==教程地址==：[原文地址（YouTube）](https://youtu.be/MLfAW55_4cY)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av91021280)