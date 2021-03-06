# CSS HTML简约日历
==教程地址==：[原文地址（YouTube）](https://youtu.be/yKc7wkyFXfU)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av81913401/)


## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
<div class="calendar">
    <div class="date">
        <h3>January</h3>
        <div class="days">
            <div class="day">S</div>
            <div class="day">M</div>
            <div class="day">T</div>
            <div class="day">W</div>
            <div class="day">T</div>
            <div class="day">F</div>
            <div class="day">S</div>
            <div class="number"></div>
            <div class="number"></div>
            <div class="number">1</div>
            <div class="number">2</div>
            <div class="number  active">3</div>
            <div class="number">4</div>
            <div class="number">5</div>
            <div class="number">6</div>
            <div class="number">7</div>
            <div class="number">8</div>
            <div class="number">9</div>
            <div class="number">10</div>
            <div class="number">11</div>
            <div class="number">12</div>
            <div class="number">13</div>
            <div class="number">14</div>
            <div class="number">15</div>
            <div class="number">16</div>
            <div class="number">17</div>
            <div class="number">18</div>
            <div class="number">19</div>
            <div class="number">20</div>
            <div class="number">21</div>
            <div class="number">22</div>
            <div class="number">23</div>
            <div class="number">24</div>
            <div class="number">25</div>
            <div class="number">26</div>
            <div class="number">27</div>
            <div class="number">28</div>
            <div class="number">29</div>
            <div class="number">30</div>
            <div class="number">31</div>
        </div>
    </div>
    <div class="img">
        <img src="img/bg.jpg" alt="Error">
    </div>
</div>
```
### CSS
```css
body{
    margin: 0; /*外边距*/
    padding: 0; /*内边距*/
    display: flex; /*盒模型*/
    justify-content: center; /*主轴居中*/
    align-items: center; /*项目居中*/
    height: 100vh; /*高度*/
    background-color: #352b48; /*背景颜色*/
    font-family: sans-serif; /*字体*/
}
.calendar{
    position: relative;
    background-color: #fff;
    width: 800px;
    height: 450px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border: 15px solid #fff; /*边框*/
    box-shadow: 0 15px 35px rgba(0,0,0,0.5);
}
.calendar .date{
    width: 400px;
    padding: 30px;
    box-sizing: border-box; /*盒子大小规则*/
}
.calendar .date h3{
    margin: 0 0 20px; 
    padding: 0;
    font-size: 24px; /*字体大小*/
    font-weight: 500; /*字体维度*/
    text-align: center; /*字体居中*/
    user-select: none; /*不可选中*/
    text-transform: capitalize; /*首字母大写*/
}
.calendar .date .days{
    display: flex;
    flex-wrap: wrap; /*可换行*/
}
.calendar .date .days .number.active{
    background-color: #362b48;
    color: #fff;
    cursor: pointer; /*鼠标样式*/
    border-radius: 50%; /*边框圆角*/
}
.calendar .date .days .day,
.calendar .date .days .number{
    width: 48px;
    height: 48px;
    display: flex;
    justify-content: center;
    align-items: center;
    user-select: none;
}
.calendar .date .days .day:first-child,
.calendar .date .days .number:nth-child(7n+1){ /*7个为一组，每组第一个*/
    color: #f44336;
    font-weight: 600;
}
.calendar .img{
    position: relative; /*定位*/
    top:0;
    right: 0;
    width: 400px;
    height: 100%;
    background-color: #000;
    user-select: none;
}
.calendar .img img{
    position: relative;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover; /*元素内容如何适应屏幕*/
}
```
### JS
```javascript
 //无
```
==教程地址==：[原文地址（YouTube）](https://youtu.be/yKc7wkyFXfU)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av81913401/)