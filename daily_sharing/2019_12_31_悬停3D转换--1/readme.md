# 标题
==教程地址==：[原文地址（codepen）](https://codepen.io/pirrera/pen/tKFhI)

==B站教程==：[原文转载（bilibili）](此处键入链接)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <div class="thumb">
        <a href="#">
              <span>the optimist lives on</span>
        </a>
  </div>
</body>
</html>
```
### CSS
```css
body,html {
    padding: 0;
    background: #ddd;
    background: linear-gradient(#ddd, #e8e8e8);
    font-family:sans-serif;
    height: 100%;
    margin:0;
}
.thumb {
    width: 400px;
    height: 400px;
    margin: 70px auto;
    perspective: 1000px; /*1000px*/
}
.thumb a span {
    color: white;
    text-transform: uppercase; /*大写*/
    position: absolute; /*相对定位*/
    top: 100%;
    left: 0;
    width: 100%;
    font: bold 12px/36px "Open Sans"; /*文字设置*/
    text-align: center; /*文字居中*/
    transform: rotateX(-89.99deg);
    transform-origin: top;
    z-index: 1;
}
.thumb a {
    display: block;
    width: 100%;
    height: 100%;
    border-top-left-radius: 25%; /*左上*/
    border-top-right-radius: 25%; /*右上*/
    background: linear-gradient(-45deg,rgb(255, 187, 0), rgba(255, 0, 0, 0.4)); /*背景*/
    transform-style: preserve-3d; /*子元素保留3D位置*/
    transition: 0.5s; /*过渡时间*/
}
.thumb:hover a {
    transform: rotateX(80deg);/*80度旋转*/
    transform-origin: bottom; /*设置观察者的角度*/
}
.thumb a:after { /*a之后添加，类似于a的背景*/
    content: '';
    position: absolute; /*绝对定位*/
    left: 0;
    bottom: 0;
    width: 100%;
    height: 36px;
    background: inherit; /*继承*/
    background-position: top;/*图像起始位置*/
    transform: rotateX(90deg); /*X轴旋转*/
    transform-origin: bottom;
}

.thumb a:before { /*a之前添加，下部阴影*/
    content: '';
    position: absolute; /*绝对定位*/
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
    box-shadow: 0 0 100px 50px rgba(0, 0, 0, 0.5);
    transition: all 0.5s;
    opacity: 0.3;
    transform: rotateX(95deg) translateZ(-80px) scale(0.75); /*X轴旋转95度，距Z轴-80，缩小到0.75倍*/
    transform-origin: bottom;
}

.thumb:hover a:before { /*悬停时阴影*/
    opacity: 1;
    box-shadow: 0 0 25px 25px rgba(0, 0, 0, 0.5);
    transform: rotateX(0) translateZ(-60px) scale(0.85);
}

/*有关3D转换的文章：https://www.zhangxinxu.com/wordpress/2012/09/css3-3d-transform-perspective-animate-transition/*/

```
### JS
```javascript
 //无
```
==教程地址==：[原文地址（codepen）](https://codepen.io/pirrera/pen/tKFhI)

==B站教程==：[原文转载（bilibili）]()