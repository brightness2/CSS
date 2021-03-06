# 等待动画效果
==教程地址==：[原文地址（YouTube）](https://youtu.be/QLiZ5VrhA98)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av91021092)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
<div class="loading">
  <span>Loading...</span>
</div>
```
### CSS
```css
body{
  margin: 0; /* 外边距 */
  padding: 0; /* 内边距 */
  background: #34495e; /* 背景颜色 */
  height: 100vh; /* 高度 */
  display: flex; /* 弹性盒模型 */
  align-items: center; /* 交叉轴对齐方式 */
  justify-content: center; /* 主轴对齐方式 */
  font-family: "montserrat",sans-serif; /* 字体 */
}

.loading{
  width: 200px;
  height: 200px;
  box-sizing: border-box; /* 盒子大小规则 */
  border-radius: 50%;
  border-top: 10px solid #e74c3c;
  position: relative; /* 相对定位 */
  animation: a1 2s linear infinite; /* 动画：名称，时间，速率，重复 */
}
/* 边框 */
.loading::before,.loading::after{/* 之前，之后添加 */
  content: ''; /* 内容 */
  width: 200px;
  height: 200px;
  position: absolute; /* 绝对定位 */
  left: 0;
  top: -10px;
  box-sizing: border-box;
  border-radius: 50%;
}

.loading::before{
  border-top: 10px solid #e67e22; /* 上边框 */
  transform: rotate(120deg); /* 通过修改角度显示 */
}

.loading::after{
  border-top: 10px solid #3498db;
  transform: rotate(240deg);
}

.loading span{
  position: absolute;
  width: 200px;
  height: 200px;
  color: #fff;
  text-align: center;/* 字体水平居中 */
  line-height: 200px; /* 行高 */
  animation: a2 2s linear infinite;
}

@keyframes a1 {
  to{
    transform: rotate(360deg); /* 转动角度 */
  }
}

@keyframes a2 {
  to{
    transform: rotate(-360deg);
  }
}

```
### JS
```javascript

```
==教程地址==：[原文地址（YouTube）](https://youtu.be/QLiZ5VrhA98)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av91021092)