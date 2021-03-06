# 社交媒体复选框
==教程地址==：[原文地址（YouTube）](https://youtu.be/WRGPvCJmy7Q)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av87248801)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
<div class='wrapper'>
  <div class="container">
    <div class="social_media_wrap">
      <!-- 开启子项 -->
      <div class="item facebook">
        <!-- 左侧标题 -->
        <div class="item_left">
          <div class="media_box">
            <i class="fab fa-facebook-f"></i>
          </div>
          <div class="media_text">
            Facebook
          </div>
        </div>
        <!-- 按钮 -->
        <div class="item_right">
          <input type="checkbox" class="checkbox">
        </div>
      </div>
      <!-- 第二项 -->
      <div class="item twitter">
        <div class="item_left">
          <div class="media_box">
            <i class="fab fa-twitter"></i>
          </div>
          <div class="media_text">
            twitter
          </div>
        </div>
        <div class="item_right">
          <input type="checkbox" class="checkbox">
        </div>
      </div>
    </div>
  </div>
</div>
```
### CSS
```css
@import url("https://fonts.googleapis.com/css?family=Montserrat&display=swap");

* {
  margin: 0; /* 外边距 */
  padding: 0; /* 内边距 */
  box-sizing: border-box; /* 盒子大小规则 */
  font-family: "Montserrat", sans-serif; /* 字体样式 */
}

body {
  background: #fb9a39; /* 背景颜色 */
  height: 100vh; /* 高度 */
}
/* 最外围 */
.wrapper {
  position: absolute; /* 绝对定位 */
  top: 50%; /* 距上部 */
  left: 50%;
  transform: translate(-50%, -50%); /* 移动X,Y,相对于自身高度 */
  background: #fbb04d;
  width: 350px;
  border-radius: 20px; /* 边框圆角 */
  padding: 25px;
}

/* 行框内 */
.wrapper .container .social_media_wrap {
  background: #fff;
  border-radius: 20px;
  padding: 25px;
  box-shadow: 0 0 2px rgba(0, 0, 0, 0.125); /* 阴影 */
}
/* 子项 */
.social_media_wrap .item {
  display: flex; /* 弹性盒模型 */
  justify-content: space-between; /* 主轴对齐方式 */
  align-items: center; /* 交叉轴对齐方式 */
  margin-bottom: 20px;
}
/*应用于最后一项*/
.social_media_wrap .item:last-child {
  margin-bottom: 0;
}
/* 左侧 */
.social_media_wrap .item .item_left {
  display: flex;
  align-items: center;
}
/* 左侧图标布局 */
.item .item_left .media_box {
  width: 50px;
  height: 50px;
  border-radius: 10px;
  border: 1px solid #d5d6d8;
  color: #d5d6d8;
  position: relative;
  margin-right: 10px;
}
/* 左侧图标 */
.item .item_left .media_box .fab {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
/* 左侧文字 */
.item .item_left .media_text {
  color: #d5d6d8;
}
/* 右侧选框 */
.item .item_right .checkbox {
  width: 65px;
  height: 35px;
  position: relative;
  appearance: none; /* 不显示选中状态 */
  -webkit-appearance: none;
  background: #f0f0f0;
  border-radius: 25px;
  outline: none; /* 轮廓无 */
  cursor: pointer; /* 鼠标状态 */
}
/* 选中状态小球 */
.item .item_right .checkbox:before {
  content: ""; /* 内容 */
  position: absolute;
  top: 4px;
  left: 5px;
  width: 28px;
  height: 28px;
  background: #f0f0f0;
  border-radius: 50%;
  box-shadow: 0 0 2px rgba(0,0,0,0.35);
  transition: all 0.2s ease; /* 过渡时间 */
}
/* 选中状态时 */
.item .item_right .checkbox:checked:before{
  left: 32px;
  background: #fb9a39;
}

/* 以下为子项的活动状态时应用 */
.item.facebook.active .media_box{
  background: #3b5999;
  border-color: #3b5999;
  color: #fff;
}

.item.facebook.active .media_text{
  color: #3b5999;
}

.item.twitter.active .media_box{
  background: #55acee;
  border-color: #55acee;
  color: #fff;
}

.item.twitter.active .media_text{
  color: #55acee;
}

.item.instagram.active .media_box{
  background: #e4405f;
  border-color: #e4405f;
  color: #fff;
}

.item.instagram.active .media_text{
  color: #e4405f;
}

.item.linkedin.active .media_box{
  background: #0077B5;
  border-color: #0077B5;
  color: #fff;
}

.item.linkedin.active .media_text{
  color: #0077B5;
}
```
### JS
```javascript

```
==教程地址==：[原文地址（YouTube）](https://youtu.be/WRGPvCJmy7Q)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av87248801)