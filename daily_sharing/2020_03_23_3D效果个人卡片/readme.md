# 带有3D效果的个性名片
==教程地址==：[原文地址（YouTube）](https://youtu.be/5ZEqwRepZao)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/BV1V7411m72L)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
<div class="card">
      <div class="content">
        <div class="user"><span class="fas fa-user"></span></div>
        <header>CodingNepal</header>
        <div class="follow-us">Follow us on</div>
        <div class="icons">
          <a href="#"><span class="fab fa-facebook-f"></span></a>
          <a href="#"><span class="fab fa-twitter"></span></a>
          <a href="#"><span class="fab fa-instagram"></span></a>
          <a href="#"><span class="fab fa-github"></span></a>
        </div>
      </div>
    </div>
```
### CSS
```css
@import url('https://fonts.googleapis.com/css?family=Poppins:400,500,600,700&display=swap');
*{
  margin: 0;
  padding: 0;
  user-select: none;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}
body{
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  background: #a7ffeb;
  perspective: 1000px;
  transform-style: preserve-3d;
  overflow: hidden;
}
.card{
  background: white;
  height: 380px;
  width: 300px;
  margin: auto;
  border-radius: 5px;
  padding: 20px 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  transform-style: preserve-3d;
}
.card .content{
  color: #202020;
  text-align: center;
  transform-style: preserve-3d;
}
.content .user{
  height: 100px;
  width: 100px;
  background: #33ffcf;
  border: 1px solid #1affc9;
  border-radius: 50%;
  margin: 10px auto;
  transform: translateZ(50px);
}
.user .fa-user{
  color: white;
  font-size: 40px;
  line-height: 100px;
}
.content header{
  margin: 20px 0;
  font-size: 32px;
  font-weight: 600;
  transform: translateZ(50px);
}
.content .follow-us{
  font-size: 23px;
  font-weight: 600;
  transform: translateZ(50px);
}
.content .icons{
  margin: 20px 0 10px 0;
  transform: translateZ(50px);
}
.icons a{
  margin: 0 2px;
}
.icons a span{
  height: 45px;
  width: 45px;
  background: #33ffcf;
  border: 1px solid #1affc9;
  line-height: 44px;
  border-radius: 50%;
  color: white;
  font-size: 20px;
}
tate{
  transform: rotate(-180deg);
}
input{
  display: none;
}

```
### JS
```javascript
$('body').mousemove(function(p){
        let rotateX = -($(window).innerWidth()/2-p.pageX)/20;
        let rotateY = -($(window).innerHeight()/2-p.pageY)/10;
        $('.card').css("transform","rotateX("+rotateX+"deg) rotateY("+rotateY+"deg)");
      });
      $(document).mouseout(function(){
        $('.card').css("transform","");
      });
```
==教程地址==：[原文地址（YouTube）](https://youtu.be/5ZEqwRepZao)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/BV1V7411m72L)