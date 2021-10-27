# 使用范围滑块更改页面亮度
==教程地址==：[原文地址（YouTube）](https://youtu.be/zGfcKBLoJFc)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av96546284/)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
<div class="container">
  <div class="brightness-box">
    <i class="far fa-sun"></i>
    <input type="range" id="range" min="10" max="100" value="100">
    <i class="fas fa-sun"></i>
  </div>
</div>
```
### CSS
```css
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.container{
  background: url(bg.jpg) no-repeat center;
  min-height: 100vh;
  background-size: cover;
  display: flex;
  align-items: center;
  justify-content: center;
}

.brightness-box{
  width: 400px;
  height: 60px;
  background: #f9f9f9;
  border-radius: 8px;
  padding: 0 20px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.brightness-box i{
  margin: 0 10px;
}

#range{
  width: 100%;
  -webkit-appearance: none;
  background: #0a85ff;
  height: 3px;
  outline: none;
}

#range::-webkit-slider-thumb{
  -webkit-appearance: none;
  width: 22px;
  height: 22px;
  background: #333;
  border-radius: 50%;
  cursor: pointer;
}
```
### JS
```javascript
rangeInput = document.getElementById('range');
container = document.getElementsByClassName('container')[0];

rangeInput.addEventListener("change",function(){
  container.style.filter = "brightness(" + rangeInput.value + "%)";
});
```
==教程地址==：[原文地址（YouTube）](https://youtu.be/zGfcKBLoJFc)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av96546284/)