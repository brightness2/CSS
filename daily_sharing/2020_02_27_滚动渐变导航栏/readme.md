# 滚动渐变导航栏
==教程地址==：[原文地址（YouTube）](https://youtu.be/6HFpw5fcaD8)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av92158773/)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
<header>
  <!-- logo -->
  <a href="#" class="logo">Logo</a> 
  <!-- 导航栏 -->
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">Aboout</a></li>
    <li><a href="#">Services</a></li>
    <li><a href="#">Portfolio</a></li>
    <li><a href="#">Team</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</header>
<!-- 内容 -->
<section class="banner"></section>
```
### CSS
```css
* {
  margin: 0; /* 外边距 */
  padding: 0; /* 内边距 */
  box-sizing: border-box; /* 盒子大小规则 */
  font-family: sans-serif; /* 字体样式 */
}

body {
  background: #000; /* 背景颜色 */
  min-height: 200vh; /* 最小高度 */
}

header {
  position: fixed; /* 根据浏览器进行定位 */
  top: 0;
  left: 0;
  width: 100%; /* 宽 */
  display: flex; /* 弹性盒模型 */
  justify-content: space-between; /* 主轴对齐方式 */
  align-items: center; /* 交叉轴对齐方式 */
  transition: 0.6s; /* 过渡时间 */
  padding: 40px 100px;
  z-index: 1000; /* 层叠顺序 */
}
header .logo {
  position: relative;
  font-weight: 700;
  color: #fff;
  text-decoration: none; /* 文字装饰 */
  font-size: 2em; /* 字体大小 */
  text-transform: uppercase; /* 字体大写 */
  letter-spacing: 2px; /* 字符间距 */
  transition: 0.6s;
}
header ul {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center; 
}

header ul li {
  position: relative;
  list-style: none;
}

header ul li a {
  position: relative;
  margin: 0 15px;
  text-decoration: none;
  color: #fff;
  letter-spacing: 2px;
  font-weight: 500px;
  transition: 0.6s;
}

.banner {
  position: relative;
  width: 100%;
  height: 100vh;
  background: url(../img/bg.jpg);
  background-size: cover; /* 背景大小：裁切 */
}

/* 修改后 */

header.sticky .logo,
header.sticky ul li a {
  color: #000;
}

header.sticky {
  padding: 5px 100px;
  background: #fff;
}
```
### JS
```javascript
// 添加滚动事件
window.addEventListener('scroll', function() {
  //获取元素
  var header = document.querySelector("header");
  // 添加类
  header.classList.toggle("sticky", window.scrollY > 0 )
});
```
==教程地址==：[原文地址（YouTube）](https://youtu.be/6HFpw5fcaD8)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av92158773/)