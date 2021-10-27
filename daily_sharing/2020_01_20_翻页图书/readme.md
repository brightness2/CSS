# 翻页图书
==教程地址==：[原文地址（YouTube）](https://youtu.be/zBR9qBBM9KA)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av84306584)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
<div class='card'>
    <div class="imgBox">
        <img src="img/bg.jpg">
    </div>
    <div class='details'>
        <h2>环保</h2>
        <p>全称环境保护，是指人类为解决现实的或潜在的环境问题，协调人类与环境的关系，保障经济、社会的持续发展而采取的各种行动的总称。其方法和手段有工程技术的、行政管理的、创新研发的，也有法律的、经济的、宣传教育的等。</p>
    </div>
</div>
```
### CSS
```css
body{
  margin: 0; /* 外边距 */
  padding: 0; /* 内边距 */
  background: #708d00; /* 背景颜色 */
}
img{
  width: 100%; /* 宽 */
}
.card{
  position: absolute; /* 绝对定位 */
  top: 50%; /* 距上部 */
  left: 50%; /* 距左部 */
  width: 300px;
  height: 400px;
  background: #fff;
  transform-style: preserve-3d; /* 开启3D空间 */
  transform: translate(-50%,-50%) perspective(2000px); /* 移动X,Y */
  box-shadow: inset 300px 0 50px rgba(0, 0, 0, 0.5), 0 20px 100px rgba(0, 0, 0, 0.5); /*阴影*/
  transition: 1s;
}
.card:hover{
  transform: translate(-50%,-50%) perspective(2000px) rotate(-10deg);
  box-shadow: inset 20px 0 50px rgba(0, 0, 0, 0.5), 0 10px 100px rgba(0, 0, 0, 0.5);
}
.card::before{ /*上边框*/ 
  content: '';
  position: absolute;
  top:-5px;
  left: 0;
  width: 100%;
  height: 5px;
  z-index: 10;
  background: #475b02;
  transform: skewX(-45deg); /*X轴扭曲*/
}
.card::after{ /*右边框*/
  content: '';
  position: absolute;
  top: 0;
  right: -5px;
  width: 5px;
  height: 100%;
  background-color: #7ea301;
}
.card .imgBox{ /*图片*/
  user-select: none; /*不可选取*/
  width: 100%;
  height: 100%;
  position: relative;
  transform-origin: left; /*更改元素变形位置*/
  transition: 1s cubic-bezier(.15,1.7,.84,.58);

}
.card:hover .imgBox{
  transform: rotateY(-155deg); /*Y轴转动*/
}
.card .details{ /*文本效果*/
  position: absolute;
  top:0;
  left: 0;
  box-sizing: border-box;
  padding: 20px;
  z-index: -1;
}
```
### JS
```javascript

```
==教程地址==：[原文地址（YouTube）](https://youtu.be/zBR9qBBM9KA)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av84306584)