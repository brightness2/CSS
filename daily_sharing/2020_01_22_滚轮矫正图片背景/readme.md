# 实现滚动条矫正图片
==教程地址==：[原文地址（YouTube）](https://youtu.be/7exL28RKb5w)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av84562889/)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
    <section>
        <span class="skewed"></span>
    </section>
```
### CSS
```css
* {
  margin: 0; /*外边距*/
  padding: 0; /*内边距*/
}
body{
  height: 200vh; /*高*/
  background: #fff; /*背景颜色*/
}
section{
  position: absolute; /*绝对定位*/
  width: 100%; /*宽*/
  height: 100vh; /*高*/
  background: url('../img/bg.jpg'),linear-gradient(230deg, #f533d4, #2461bb); /*背景图片,渐变颜色*/
  background-blend-mode: luminosity; /*背景图片和背景色的融合模式*/
  background-size: cover; /*背景图片大小*/
}
section .skewed{
  position: absolute;
  bottom: -100%; /*距底部*/
  left: 0;
  width: 100%;
  height: 100%;
  background-color: #fff; 
  transform: skewY(-10deg); /*扭曲Y轴-10deg*/
  transform-origin:top left ; /*变化开始位置*/
}
```
### JS
```javascript
<script>
	// 获取根据CSS选择器获取元素
let skewed = document.querySelector('.skewed')
// 再窗口中添加scroll事件进行监听
window.addEventListener('scroll', function () {
		// -30为元素css设置的值 + 窗口滚动的Y轴值/10
		let value = -30 + window.scrollY/10
		// 修改skewY值
    skewed.style.transform = 'skewY(' + value + 'deg)' 
})
</script>
```
==教程地址==：[原文地址（YouTube）](https://youtu.be/7exL28RKb5w)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av84562889)