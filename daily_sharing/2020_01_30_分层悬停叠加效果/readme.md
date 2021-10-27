# 标题
==教程地址==：[原文地址（YouTube）](https://youtu.be/WF68FcI21es)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av85779437/)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
  <div class="container">
		<img src="img/bg.jpg">
		<img src="img/bg.jpg">
		<img src="img/bg.jpg">
		<img src="img/bg.jpg">
	</div>
```
### CSS
```css
body {
  margin: 0; /* 外边距 */
  padding: 0; /* 内边距 */
  width: 100%; /* 宽 */
  height: 100vh; /* 高 */
  display: flex; /* 弹性盒模型 */
  align-items: center; /* 交叉轴居中 */
  justify-content: center; /* 主轴居中 */
  overflow: hidden; /* 超出隐藏,防止出现滚动条 */
}
.container {
  position: relative; /* 相对定位 */
  width: 360px;
  height: 640px;
  margin-top: 150px;
  background: rgba(0, 0, 0, 0.3); /* 背景 */
  transform: rotate(-30deg) skew(25deg) scale(0.8); /* 旋转 扭曲 放大 */
  transition: 0.5s; /* 过渡时间 */
}
.container:hover{
  transform: rotate(-30deg) skew(25deg) scale(1);
}
.container img {
  position: absolute; /* 绝对定位 */
  object-fit: cover; /* 保证宽高比进行裁剪 */
  height: 100%;
  width: 100%;
  transition: 0.5s;
}
.container:hover img:nth-child(4) { /* 第四个img */
  transform: translate(160px, -160px); /* 移动x,y */
  opacity: 1; /* 透明度 */
}
.container:hover img:nth-child(3) {
  transform: translate(120px, -120px);
  opacity: 0.8;
}
.container:hover img:nth-child(2) {
  transform: translate(80px, -80px);
  opacity: 0.6;
}
.container:hover img:nth-child(1) {
  transform: translate(40px, -40px);
  opacity: 0.4;
}
```
### JS
```javascript

```
==教程地址==：[原文地址（YouTube）](https://youtu.be/WF68FcI21es)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av85779437/)