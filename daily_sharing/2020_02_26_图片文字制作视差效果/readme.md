# 图片文字制作视差效果
==教程地址==：[原文地址（YouTube）](https://youtu.be/vmQXnkkjG9U)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av91834459/)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
  <section>
		<p>
      <!-- 请自行添加文章 -->
		</p>
		<div id='bg'></div>
	</section>
```
### CSS
```css
@import url('https://fonts.googleapis.com/css?family=Poppins&display=swap');
* {
  margin: 0; /* 外边距 */
  padding: 0; /* 内边距 */
  font-family: 'Poppins', sans-serif; /* 字体样式 */
}
section {
  background-color: #000; /* 背景颜色 */
  height: 100vh; /* 高度 */
  overflow: hidden; /* 超出隐藏 */
}

section p {
  position: fixed; /* 定位：相对于浏览器 */
  top: 0;
  left: 0;
  font-size: 24px; /* 字体大小 */
  letter-spacing: -1px; /* 字符间距 */
  line-height: 0.8em; /* 行高 */
  background: url(../img/bg.jpg);
  -webkit-background-clip: text; /* 背景裁剪：文字 */
  text-align: justify; /* 两端对齐 */
  color: transparent; /* 透明文字 */
  filter: contrast(2); /* 对比度 */
  user-select: none; /* 无法选中 */
}

#bg {
  position: absolute;
  top: 0;
  right: 0;
  width: 100%;
  height: 100%;
  background: url(../img/bg.jpg);
  background-attachment: fixed; /* 背景不滚动 */
}
```
### JS
```javascript
		var bg = document.getElementById('bg');
		window.onmousemove = function(e) {
      // 修改宽度，根据鼠标
			bg.style.width = e.clientX + 'px';
		}
```
==教程地址==：[原文地址（YouTube）](https://youtu.be/vmQXnkkjG9U)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av91834459/)