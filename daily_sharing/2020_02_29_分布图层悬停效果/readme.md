# 分布图层悬停效果
==教程地址==：[原文地址（YouTube）](https://youtu.be/knlYOJDI6Lk)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av92694735)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
  <div class="container">
		<div class="imgBx">
			<img src="img/bg.jpg">
			<img src="img/bg.jpg">
			<img src="img/bg.jpg">
		</div>
		<h2><!--自行添加--></h2>
		<div class="skew">
			<p>
        <!-- 自行添加英语 -->
      </p>
      <a href="#">Read Me</a>
		</div>
	</div>
```
### CSS
```css
* {
  margin: 0; /* 外边距 */
  padding: 0; /* 内边距 */
  font-family: sans-serif; /* 字体样式 */
}
body {
  display: flex; /* 弹性盒模型 */
  justify-content: center; /* 主轴对齐方式 */
  align-items: center; /* 交叉轴对齐方式 */
  background: #111; /* 背景颜色 */
  flex-direction: column; /* 排列方式：竖向 */
}
.container {
  position: relative; /* 相对定位 */
  margin-top: 250px;
  max-width: 800px; /* 最大宽度 */
  transform: skewY(-20deg) translate3d(0, 0, 0); /* 倾斜，开启3D加速 */
}
.container .imgBx{
  position: relative;
  width: 100%;
  height: 180px;
  transform-origin: bottom; /* 动画从哪边执行 */
  transform: skewX(45deg);
  /* overflow: hidden; */
}
.container .imgBx img {
  position: absolute;
  top: 0;
  left: 0;
  filter: grayscale(1); /* 灰阶调整 */
  width: 100%;
  height: 100%;
  transition: 0.5s; /* 过渡时间 */
}
/* 层叠效果实现 */
.container .imgBx:hover img{ /* 添加色彩 */
  filter: grayscale(0);
}
.container .imgBx:hover img:nth-child(3) {
  /* 移动实现层叠效果 */
  transform: translate(100px, -100px);
}
.container .imgBx:hover img:nth-child(2) {
  transform: translate(50px, -50px);
  opacity: 0.5; /* 透明度 */
}
.container .imgBx:hover img:nth-child(1) {
  transform: translate(0px, 0px);
  opacity: 0.1;
}
/* 下部文字 */ 
.container h2 {
  position: relative;
  color: #fff;
  font-size: 4em;
  transform:translate3d(0, 0, 0); /* 开启3D加速，防止抖动 */
}
.container .skew {
  transform-origin: top;
  transform: skewX(45deg) translate3d(0, 0, 0);
}
.container .skew p {
  color: #fff;
  font-size: 1.2em;
}
/* 按钮 */
.container .skew a {
  position: relative;
  padding: 10px 30px;
  display: inline-block; /* 行内盒模型 */
  background: transparent; /* 背景透明 */
  color: #fff;
  transform-origin: top;
  margin-top: 20px;
  border: 2px solid #fff; /* 边框 */
  transform: skewX(-45deg);
  letter-spacing: 2px; /* 字符间距 */
  text-decoration: none; /* 清除字符装饰 */
  font-size: 20px;
  transition: 0.5s;
}
.container .skew a:hover {
  background: #fff;
  color: #000;
}
```
### JS
```javascript

```
==教程地址==：[原文地址（YouTube）](https://youtu.be/knlYOJDI6Lk)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av92694735)