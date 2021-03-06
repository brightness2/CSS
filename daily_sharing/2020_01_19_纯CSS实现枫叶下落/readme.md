# 纯CSS实现枫叶下落
==教程地址==：[原文地址（YouTube）](https://www.bilibili.com/video/av84160469)

==B站教程==：[原文转载（bilibili）](https://youtu.be/fD_AuhsheuU)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
<section>
    <h2>Autumn leaves</h2>
    <div class="set"> <!-- 中 -->
        <div><img src="img/f1.png"></div>
        <div><img src="img/f2.png"></div>
        <div><img src="img/f3.png"></div>
        <div><img src="img/f4.png"></div>
        <div><img src="img/f1.png"></div>
        <div><img src="img/f2.png"></div>
        <div><img src="img/f3.png"></div>
        <div><img src="img/f4.png"></div>
    </div>
    <div class="set set2"> <!-- 前 -->
        <div><img src="img/f1.png"></div>
        <div><img src="img/f2.png"></div>
        <div><img src="img/f3.png"></div>
        <div><img src="img/f4.png"></div>
        <div><img src="img/f1.png"></div>
        <div><img src="img/f2.png"></div>
        <div><img src="img/f3.png"></div>
        <div><img src="img/f4.png"></div>
    </div>
    <div class="set set3"> <!-- 后 -->
        <div><img src="img/f1.png"></div>
        <div><img src="img/f2.png"></div>
        <div><img src="img/f3.png"></div>
        <div><img src="img/f4.png"></div>
        <div><img src="img/f1.png"></div>
        <div><img src="img/f2.png"></div>
        <div><img src="img/f3.png"></div>
        <div><img src="img/f4.png"></div>
    </div>
</section>
```
### CSS
```css
body{
  margin: 0; /*外边距*/
  padding: 0; /*内边距*/
  overflow: hidden; /*溢出隐藏*/
  height: 100vh; /*高度*/
}
section{
  position: relative; /*相对定位*/
  width: 100%;
  height: 100%;
  background:radial-gradient(#333,#000); /*径向渐变*/
}
.set{
  position: absolute; /*绝对定位*/
  width: 100%;
  height: 100%;
  top: 0; /*距上部*/
  left: 0; /*距左部*/
}
img{
  width: 100px;
  user-select: none; /*不可选取*/
}
.set div{
  position: absolute;
  display: block; /*块元素*/
}
.set div:nth-child(1){ /*第一个子元素*/
  left: 20%;
  animation: animate 15s linear infinite; /*动画：name time 线性执行 重复*/
  animation-delay: -7s; /*等待时间*/
}
.set div:nth-child(2){
  left: 50%;
  animation: animate 15s linear infinite;
  animation-delay: -5s;
}
.set div:nth-child(3){
  left: 70%;
  animation: animate 20s linear infinite;
}
.set div:nth-child(4){
  left: 0%;
  animation: animate 15s linear infinite;
  animation-delay: -5s;
}
.set div:nth-child(5){
  left: 85%;
  animation: animate 18s linear infinite;
  animation-delay: -10s;
}
.set div:nth-child(6){
  left: 0%;
  animation: animate 12s linear infinite;
}
.set div:nth-child(7){
  left: 15%;
  animation: animate 14s linear infinite;
}
.set div:nth-child(8){
  left: 60%;
  animation: animate 15s linear infinite;
}
@keyframes animate{ /*动画*/
  0%{
    top:-10%;
    opacity: 0; /*透明度*/
    transform: translateX(20px) rotate(0deg); /*动作 X轴移动 旋转*/
  }
  10%{
    opacity: 1;
  }
  20%{
    transform: translateX(-20px) rotate(45deg);
  }
  40%{
    transform: translateX(-20px) rotate(90deg);
  }
  60%{
    transform: translateX(20px) rotate(130deg);
  }
  80%{
    transform: translateX(-20px) rotate(180deg);
  }
  100%{
    top:110%;
    transform: translateX(-20px) rotate(225deg);
  }
}
.set2{
  transform: scale(2) rotateY(180deg);
  filter: blur(2px); /*模糊*/
  z-index: 3;
}
.set3{
  transform: scale(0.8) rotateX(180deg);
  filter: blur(4px);
  z-index: 2;
}
h2{
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  width: 100%;
  text-align: center; /*居中*/
  margin: 0;
  color: #fff; /*字体颜色*/
  padding: 0;
  font-size: 8em; /*字体大小*/
  font-family: sans-serif; /*字体*/
  z-index: 1; /*Z轴顺序*/
  user-select: none;
}
```
### JS
```javascript

```
==教程地址==：[原文地址（YouTube）](https://youtu.be/fD_AuhsheuU)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av84160469)