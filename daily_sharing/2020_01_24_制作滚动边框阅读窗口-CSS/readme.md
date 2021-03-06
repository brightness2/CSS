# 纯CSS制作滚动边框阅读窗口
==教程地址==：[原文地址（YouTube）](https://youtu.be/t-9UIPEJxxQ)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av84798622/)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
<div class="box">
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <div class="content">
        <h1>What is scrolling</h1>
        <p>滚动（Rolling）是一种结合了转动（多半是针对轴对称物体）及相对特定表面平移的的运动。若在理想状况下，物体和表面会在没有滑动的情形下互相接触。</p>
    </div>
</div>
```
### CSS
```css
body{
  margin: 0; /*外边距*/
  padding: 0; /*内边距*/
  background: #073146; /*背景*/
  font-family: sans-serif; /*字体*/
}
.box{
  position: absolute; /*绝对定位*/
  top: 50%; /*距上部*/
  left: 50%; /*距左部*/
  transform: translate(-50%, -50%); /*移动X,Y轴*/
  height: 400px; /*高度*/
  width: 400px; /*宽度*/
  background-color: #001e2d; /*背景颜色*/
  box-sizing: border-box; /*大小规则*/
  overflow: hidden; /*超出隐藏*/
  box-shadow: 0 20px 20px rgba(0, 0, 0, 0.5); /*阴影*/
  border: 2px solid rgba(0, 0, 0, 0.5); /*边框*/
}
.box::before{ /*之前添加*/
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background-color: rgba(255, 255, 255, 0.1);
  transition: 0.5s; /*过渡时间*/
  pointer-events: none; /*允许鼠标点击穿透*/
}
.box:hover::before{
  left: -50%;
  transform: skewX(-5deg); /*斜切*/
}
.box .content{
  position: absolute;
  top: 15px;
  left: 15px;
  right: 15px;
  bottom: 15px;
  border: 2px solid #ffeb3b;
  padding: 30px;
  text-align: center; /*字体水平对齐*/
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.5);
}
.box .content h1{
  color: #fff;
  font-size: 30px; /*字体大小*/
  margin: 0 0 10px;
  padding: 0;
}
.box .content p{
  color: #fff;
}
.box span{
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%; /*高度*/
  display: block;
  box-sizing: border-box;
}
.box span:nth-child(1){ /*第一个span*/
  transform: rotate(0deg); /*旋转,上边框*/
}
.box span:nth-child(2){
  transform: rotate(90deg); /*旋转,右边框*/
}
.box span:nth-child(3){
  transform: rotate(180deg); /*旋转,下边框*/
}
.box span:nth-child(4){
  transform: rotate(270deg); /*旋转左边框*/
}
.box span:nth-child(2)::before{
  animation-delay: -2s; /*等待时间*/
}
.box span:nth-child(4)::before{
  animation-delay: -2s;
}
.box span::before{ /*此为动态边框*/
  content: '';
  position: absolute;
  width: 100%;
  height: 2px;
  background: #0093ff;
  animation: animate 4s linear infinite; /*动画*/
}
@keyframes animate{ /*动画*/
  0%{
    transform: scaleX(0); /*X轴放大*/
    transform-origin: left; /*动画从左开始*/
  }
  50%{
    transform: scaleX(1);
    transform-origin: left;
  }
  /*实现从左到右的转变*/
  50.1%{
    transform: scaleX(1);
    transform-origin: right;
  }
  100%{
    transform: scaleX(0);
    transform-origin: right;
  }
```
### JS
```javascript

```
==教程地址==：[原文地址（YouTube）](https://youtu.be/t-9UIPEJxxQ)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av84798622/)