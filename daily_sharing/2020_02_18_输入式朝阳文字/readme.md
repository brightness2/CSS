# 输入式朝阳文字
==教程地址==：[原文地址（YouTube）](https://youtu.be/xrmdn1t5moA)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av89844748)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
<div id="text" contenteditable="true">Text</div>
```
### CSS
```css
* {
  margin: 0; /* 外边距 */
  padding: 0; /* 内边距 */
  font-family: sans-serif; /* 字体 */
}

body {
  display: flex; /* 弹性盒模型 */
  justify-content: center; /* 主轴对齐方式 */
  align-items: center; /* 交叉轴对齐方式 */
  background: #00fff3; /* 背景颜色 */
  height: 100vh; /* 高度 */
}
#text {
  position: relative; /* 相对定位 */
  outline: none; /* 去除边框 */
  color: #fff; /* 颜色 */
  font-weight: 700; /* 字体维度 */
  font-size: 10em; /* 字体大小 */
  width: 100%; /* 宽度 */
  text-align: center; /* 字体居中 */
}
```
### JS
```javascript
// 获取元素
var text = document.getElementById('text');
var shadow = '';
// 循环给阴影赋值
for(var i = 0; i< 30 ; i++) {
  shadow += (shadow ? ',': '') + i*1 +'px ' + i*1 +'px 0 #01ded3'
}
// 添加阴影
text.style.textShadow = shadow;
```
==教程地址==：[原文地址（YouTube）](https://youtu.be/xrmdn1t5moA)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av89844748)