# 弹动加载动画

==教程地址==：[原文地址（YouTube）](https://youtu.be/536IMcLjsmw)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av96547333)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
<div class="loading-screen">
  <div class="loading-animation">
    <img src="logo.png" alt="" class="logo">
    <div class="loading-bar"></div>
  </div>
</div>
```
### CSS
```css
*{
  margin: 0;
  padding: 0;
}

.loading-screen{
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  background: #f5f5f5;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.logo{
  width: 48px;
  height: 48px;
}

.loading-bar{
  width: 130px;
  height: 2px;
  background: #cfcfcf;
  margin-top: 22px;
  position: relative;
  overflow: hidden;
}

.loading-bar::before{
  content: "";
  width: 68px;
  height: 2px;
  background: #0073b1;
  position: absolute;
  left: -34px;
  animation: bluebar 1.5s infinite ease;
}

@keyframes bluebar {
  50%{
    left: 96px;
  }
}

```
### JS
```javascript

```
==教程地址==：[原文地址（YouTube）](https://youtu.be/536IMcLjsmw)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av96547333)
