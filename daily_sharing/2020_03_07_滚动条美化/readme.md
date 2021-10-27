# 自定义滚动条
==教程地址==：[原文地址（YouTube）](https://youtu.be/mijLmCD3W9s)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av94211888)
**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
    <section>
      <h2>百年孤独</h2>
      <p>
<!-- 请增加到足够滚动的字体 -->
      </p>
    </section>
```
### CSS
```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: consolas;
}
body {
  background: #000;
}
section {
  width: 100%;
  min-height: 100vh;
  padding: 100px;
}
section h2 {
  color: #666;
}
section p {
  color: #666;
  font-size: 1.2em;
}
/* 滚动条设置 */
::-webkit-scrollbar {  /* 滚动条 */
  width: 12px;
}
::-webkit-scrollbar-thumb {  /* 滚动条上的滚动滑块. */
  background: linear-gradient(transparent, #30ff00); /* 背景颜色 */
  border-radius: 6px;
}
::-webkit-scrollbar-thumb:hover {
  background: linear-gradient(transparent, #00c6ff);
}
```
### JS
```javascript

```
==教程地址==：[原文地址（YouTube）](https://youtu.be/mijLmCD3W9s)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av94211888)