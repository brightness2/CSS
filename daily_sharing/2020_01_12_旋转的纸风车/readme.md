# 标题
==教程地址==：[原文地址（YouTube）](https://youtu.be/bqL4FqihRQg)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av82999319)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
<div class="box">
    <div>
        <span></span>
        <span></span>
        <span></span>
        <span></span>
    </div>
</div>
```
### CSS
```css
body{
    margin: 0; /*外边距*/
    padding: 0; /*内边距*/
    background-color: #607d8b; /*背景颜色*/
}
.box{
    position:absolute; /*绝对定位*/
    top: calc(50% - 150px); /*距上部*/
    left: calc(50% - 100px); /*距左部*/
    transform: perspective(1000px) rotateY(-45deg); /*动画 视距 Y轴旋转*/
    width: 200px; /*宽度*/
    height: 300px; /*高度*/
    transform-style: preserve-3d; /*保留3D效果*/
}
.box::before{ /*之后添加*/
    content: ""; /*内容*/
    position: absolute;
    bottom: -100px;
    left: 0;
    width: 100%;
    height: 50px;
    background-color: #000;
    filter: blur(40px); /**/
    opacity: 0.5; /*透明度*/
    transform: rotateX(90deg);
}
.box div{
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    transform-style: preserve-3d;
    animation: cc 5s linear infinite; /*动画名称 5S 时间 重复循环*/
}
.box div span{
    position: absolute;
    top: 0;
    left: 0;
    display: block;
    width: 100%;
    height: 100%;
    background: linear-gradient(0deg, #f1f1f1,#bbb,#f1f1f1); /*渐变*/
    border-radius: 20px; /*圆角*/
}
.box div span:nth-child(1){ /*第一个*/
    transform: rotateX(0deg);
}
.box div span:nth-child(2){
    transform: rotateX(45deg);
}
.box div span:nth-child(3){
    transform: rotateX(-45deg);
}

.box div span:nth-child(4){
    transform: rotateX(90deg);
}
@keyframes cc{ /*动画*/
    0%{
        transform: perspective(1000px) rotateX(0deg);
    }
    100%{
        transform: perspective(1000px) rotateX(359deg);
    }
}
```
### JS
```javascript

```
==教程地址==：[原文地址（YouTube）](https://youtu.be/bqL4FqihRQg)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av82999319)