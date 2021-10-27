#  CSS倾斜边框|创意框边框悬停效果
==教程地址==：[原文地址（YouTube）](https://youtu.be/-1U62fdmCk4)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av81272914)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
    <div class="container">
        <div class="box">
            <div class="content">
                <h2>01</h2>
                <h3>夜之城</h3>
                <p>
                    “惊魂”们的表现越来越狂暴：大街上充满了瘾君子们——他们为一种刚刚出现的娱乐项
                    目所沉迷：“脑舞”。脑舞十分廉价，却可以让人体验到其他人的生活和他们的情绪，
                    尤其是当其他人的生活比自己的更加丰富多彩时，这种刺激是无与伦比的。
                </p>
                <a href="#">Read More</a>
            </div>
        </div>
        <div class="box">
            <div class="content">
                <h2>02</h2>
                <h3>脑舞</h3>
                <p>
                    说白了，脑舞是一种个人经历所制作的电子专辑。观看者可以通过一种叫做“BD播放器（BD Player）”
                    的特殊大脑扩充器直接将这些电子专辑中的数据输入自己的神经系统，
                    脑舞让观看者可以同时感受记录者脑中的所有感受，包括情绪、肌肉动作、感知等等。
                </p>
                <a href="#">Read More</a>
            </div>
        </div>
        <div class="box">
            <div class="content">
                <h2>03</h2>
                <h3>游戏设定</h3>
                <p>
                    制作组承诺游戏将真实地忠于“赛博朋克”风格。
                    玩家将进入2077年的黑暗未来——那是一个先进技术既成为人类的救星、
                    也是加以人类身上的诅咒的世界。本作面向成人玩家打造，采用了多线程、
                    非线性式剧情，围绕着一个超级大都市“夜之城”（Night City）及其周边展开。
                </p>
                <a href="#">Read More</a>
            </div>
        </div>
        <div class="box">
            <div class="content">
                <h2>04</h2>
                <h3>游戏特色</h3>
                <p>
                    1. 第一人称RPG沙盘游戏;
                    2. 想去哪里都可以去;
                    3. 为成年玩家打造的野心RPG;
                    4. 发生在2077年的腐败和高科技世界;
                    5. 多线故事;
                    6. 细腻的夜之城景色;
                    7 高级RPG机制;
                    8 RPG机制基于“笔和纸系统”;
                    9. 大量武器、升级、植入物和高科技小装备;
                    10. 采用的新装备反映了人类50年的发展过程;
                </p>
                <a href="#">Read More</a>
            </div>
        </div>
    </div>
```
### CSS
```css
body{
    margin:0; /*外边距*/
    padding: 0; /*内边距*/
    display: flex; /*盒模型*/
    flex-wrap: wrap; /*允许换行*/
    justify-content: center; /*横轴*/
    align-items: center; /*纵轴*/
    min-height: 100vh; /*最小高度*/
    background: #060c21; /*背景颜色*/
    font-family: sans-serif; /*字体*/
}
.container{
    position: relative; /*相对定位*/
    width: 90%; /*宽度*/
    display: grid; /*样式：网格*/
    grid-template-rows: auto; /*网格块行数*/
    grid-template-columns: repeat(auto-fill,minmax(260px,1fr)); /*表格块列数（自动换行(所占大小，    minmax(最小值，最大值(区间))     )）*/
     /*相关连接   https://developer.mozilla.org/zh-CN/docs/Web/CSS/grid-template-columns*/
    grid-gap: 0 40px; /*间距:上下0 左右40*/
}
.container .box{ /*容器内 盒*/
    position:relative;
    height: 400px;
    background-color: #060c21;
    display: flex;
    justify-content: center;
    align-items: center;
    border: 1px solid #000;
}
.container .box::after{ /*之后添加*/
    content: ""; /*添加内容*/
    position: absolute; /*绝对定位*/
    top:0px;
    left: 50%;
    width: 50%;
    height: 100%;
    background: rgba(255, 255, 255, 0.05);
}
.container .box:before{ /*之前*/
    content: "";
    position: absolute;
    top:-2px;
    left: -2px;
    right: -2px;
    bottom: -2px;
    background:#fff;
    transform: skew(2deg,2deg); /*扭曲*/
    z-index: -1; /**/
}
.container .box:nth-child(2n+1)::before{ /*之后添加*/
    background: linear-gradient(315deg,#f1c40f,#e64a19); /*渐变*/
}
.container .box:nth-child(2n+2)::before{ /**/
    background: linear-gradient(315deg,#16a085,#3498db);
}
.content{ /*盒内-内容*/
    position:relative;
    margin: 20px;
}
.box .content h2{ /*背景标题(01,02,03,04)*/
    position: absolute; 
    top:-60px;
    right: 20px;
    margin: 0;
    padding: 0;
    font-size: 10em;
    color: rgba(255, 255, 255, 0.1);
    transition:0.5s;
    user-select: none; /*设置为不可选取*/
}
.box:hover .content h2{ /*悬停后，进行移动*/
    top:-140px;
}
.box .content h3{ /**/
    margin: 0 0 10px;
    padding: 0;
    font-size: 24px;
    font-weight: 500;
    color:#fff;
    opacity: 0.7; /*透明度*/
    transition: 0.5s;
}
.box:hover .content h3{ /*悬停后，进行透明度变化*/
    opacity: 1;
    font-size: 30px;
}
.box .content p{ /*盒内-内容主文字*/
    margin: 0;
    padding: 0;
    color: #fff;
    font-size: 16px;
    transition: 0.5s;
    opacity: 0.5;
}
.box:hover .content p{ /*修改悬停后P的透明度*/
    opacity: 1;
}
.box .content a{ /*按钮*/
    display: inline-block; /*行内块元素*/
    position: relative;
    margin: 20 0 0;
    padding: 10px 20px;
    text-decoration: none; /*清除字体样式*/
    border: 1px solid #fff;
    color: #fff;
    transition: 0.5s;
    transform: translateY(-40px); /*移动*/
    opacity: 0;
    visibility: hidden; /*隐藏*/
    font-size: 16px;
    user-select: none; /*不可选取*/
}
.box:hover .content a{ /*悬停后 按钮进行的变化*/
    transform: translateY(0px);
    opacity: 1;
    visibility: visible;
}
.content a:hover{ /*鼠标到指向按钮，按钮的变化*/
    background: #fff;
    color:#000;
}

```
### JS
```javascript

```
==教程地址==：[原文地址（YouTube）](https://youtu.be/-1U62fdmCk4)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av81272914)