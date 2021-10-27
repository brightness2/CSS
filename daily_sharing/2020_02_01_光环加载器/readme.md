# css炫光加载器
==教程地址==：[原文地址（YouTube）](https://youtu.be/jThaNv8pKDQ?t=36)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av86041322)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
  <div class="loader">
		<span></span>
		<span></span>
		<span></span>
		<span></span>
	</div>
```
### CSS
```css
body{
  margin: 0; /* 外边距 */
  padding: 0; /* 内边距 */
  display: flex; /* 弹性盒模型 */
  justify-content: center; /* 主轴对齐方式 */
  align-items: center; /* 交叉轴对齐方式 */
  background: #240229; /* 背景颜色 */
  height: 100vh; /* 高度 */
}
.loader{
  position: relative; /* 相对定位，为了不让子元素定位到根而设置 */
  width: 100px;
  height: 100px;
  border-radius: 50%; /* 边框圆角 */
  background: linear-gradient(#14ffe9, #ffeb3b, #ff00e0); /* 背景渐变 */
  animation: animate 0.5s linear infinite; /* 动画：名称 时间 速率曲线 重复 */
}
@keyframes animate{
  0%{
    transform: rotate(0deg); /* 旋转 */
  }
  /* 利用修改旋转角度而实现环绕 */
  100%{
    transform: rotate(360deg);
  }
}
.loader span{
  position: absolute; /* 绝对定位 */
  width: 100px;
  height: 100px;
  border-radius: 50%;
  background: linear-gradient(#14ffe9, #ffeb3b, #ff00e0);
}
.loader span:nth-child(1){ /* 第一个span元素 */
  filter: blur(5px); /* 过滤：模糊 */
}
.loader span:nth-child(2){ /* 第二个span元素 */
  filter: blur(10px);
}
.loader span:nth-child(3){
  filter: blur(25px);
}
.loader span:nth-child(4){
  filter: blur(50px);
}
.loader::after{ /* 之后添加，为中心的黑色 */
  content: ''; /* 内容 */
  position: absolute;
  /* 当设置了2个对立的定位时，元素的大小为对立距离 如此处的高为
  100px - 10px - 10px = 80px
  (父元素 - top - left)
  */
  top: 10px; /* 距上部 */
  left: 10px;
  right: 10px;
  bottom: 10px;
  background: #240229;
  border-radius: 50%;
}
```
### JS
```javascript

```
==教程地址==：[原文地址（YouTube）](https://youtu.be/jThaNv8pKDQ?t=36)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av86041322)