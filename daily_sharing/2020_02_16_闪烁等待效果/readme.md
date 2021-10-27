# 过渡等待动画
==教程地址==：[原文地址（YouTube）](https://youtu.be/bOcXNaUN20M)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av89332359/)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
<h2>
  <span>L</span>
  <span>o</span>
  <span>a</span>
  <span>d</span>
  <span>i</span>
  <span>n</span>
  <span>g</span>
  <span>...</span>
</h2>
```
### CSS
```css
* {
  margin: 0; /* 外边距 */
  padding: 0; /* 内边距 */
  font-family: consolas; /* 字体 */
}
body {
  display: flex; /* 弹性盒模型 */
  justify-content: center; /* 主轴对齐方式 */
  align-items: center; /* 交叉轴对齐方式 */
  min-height: 100vh; /* 最小高度 */
  background-color: #000; /* 背景颜色 */
}
h2 {
  color: #000; /* 颜色 */
  font-size: 6em; /* 字体大小 */
  display: flex;
}
h2 span{
  animation: animate 4s linear infinite; /* 动画：名称，时间，速率 重复 */
}
@keyframes animate {
  0%,100% {
    color: #fff;
    filter: blur(2px); /* 模糊 */
    text-shadow: /* 阴影 */
    0 0 10px #00b3ff,
    0 0 20px #00b3ff,
    0 0 40px #00b3ff,
    0 0 80px #00b3ff,
    0 0 120px #00b3ff,
    0 0 200px #00b3ff,
    0 0 300px #00b3ff,
    0 0 400px #00b3ff;
  }
  25%,75% {
    color: #000;
    filter: blur(0px);
    text-shadow:none;
  }
}
```
### JS
```javascript
// 获取数组
const spans = document.getElementsByTagName('span')
let t = 0
// 循环赋值
for(i of spans) {
  i.style.animationDelay = t + 's'
  t = t + 0.1
}
```
==教程地址==：[原文地址（YouTube）](https://youtu.be/bOcXNaUN20M)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av89332359/)