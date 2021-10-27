# 跟随鼠标移动的背景
==教程地址==：[原文地址（YouTube）](https://youtu.be/PbKOX2tkHlI)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av84716592)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
    <div id='container'>
        <div class='content'>
            <h2>404</h2>
            <h4>Opps! Page not found</h4>
            <p>
                2013年，404 Not Found成为中国大陆的网络热词。在中国，404被大部分网民普遍用作网站被防火长城屏蔽的代名词。而事实上，由于防火长城一般的封锁方法是向连接两端的计算机发送RST（Reset）数据包干扰两者间正常的TCP连接，被防火长城屏蔽的网站无法回复任何HTTP状态码，最常见的错误信息是“连接已被重置”。
            </p>
            <a href="#">
                Back To Home
            </a>
        </div>
    </div>
```
### CSS
```css
*{
  margin: 0; /*外边距*/
  padding: 0; /*内边距*/
  box-sizing: border-box; /*盒子大小规则*/
  font-family: sans-serif; /*字体:非衬线*/
}
body{
  background: linear-gradient(45deg, #8500ff, #5acaff); /*背景颜色渐变*/
  height: 100vh; /*高度：100视窗*/
}
#container{
  position: absolute; /*绝对定位*/
  top: 10%; /*距上部*/
  left: 10%;
  right: 10%;
  bottom: 10%;
  border-radius: 10px; /*圆角边框*/
  display: flex; /*弹性盒模型*/
  justify-content: center; /*主轴对齐方式*/
  align-items: center; /*交叉轴对齐方式*/
  background: url('../img/bg.png'), #151729; /*背景图片，颜色*/
  box-shadow: 0 15px 30px rgba(0, 0, 0, 0.5); /*背景阴影*/
}
#container .content{ 
  max-width: 600px; /*最大宽度*/
  text-align: center; /*字体行居中*/
}
#container .content h2{
  font-size: 18vw; /*字体大小*/
  color: #fff;
  line-height: 1em; /*行高*/
}
#container .content h4{
  position: relative;
  font-size: 1.5em;
  margin-bottom: 20px;
  color: #111;
  background: #fff;
  font-weight: 300;
  padding: 10px 20px;
  display: inline-block; /*行内盒模型*/
}
#container .content p{
  color: #fff;
  font-size: 1.2em;
}
#container .content a{
  position: relative;
  display: inline-block;
  padding: 10px 25px;
  background: #ff0562;
  color: #fff;
  text-decoration: none;
  margin-top: 25px;
  border-radius: 25px;
  border-bottom: 4px solid #d00d56; /*下边框*/
  user-select: none;
}
```
### JS
```javascript
        // 根据id获取元素
        const container = document.getElementById('container');
        // 窗口的鼠标移动事件,传入event对象
        window.onmousemove = function(e) {
            // 返回被触发时的鼠标X，Y位置
            let x = e.clientX / 5 
                y = e.clientY / 5;
            // 将容器的背景图片定位进行修改
            container.style.backgroundPositionX = x + 'px';
            container.style.backgroundPositionY = y + 'px';
        }
```
==教程地址==：[原文地址（YouTube）](https://youtu.be/PbKOX2tkHlI)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av84716592)