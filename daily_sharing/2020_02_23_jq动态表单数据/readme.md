# 标题
==教程地址==：[原文地址（YouTube）](https://youtu.be/h7gZY3_3Dqs)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av91020879)

**两个视频的内容相同，第二个为转载**

## 效果图
>![演示图片](演示.gif)

## 代码区

### html
```html
<div class="container">
  <!-- 输入框 -->
  <input type="text" class="txtb" placeholder="Add a task">
  <!-- 未完成 -->
  <div class="notcomp">
    <h3>Not Completed</h3>
  </div>
  <!-- 已完成 -->
  <div class="comp">
    <h3>Completed</h3>
  </div>
</div>
```
### CSS
```css
* {
  margin: 0; /* 外边距 */
  padding: 0; /* 内边距 */
  font-family: "montserrat",sans-serif; /* 字体 */
  box-sizing: border-box; /* 盒子大小规则 */
}

body {
  background-image: linear-gradient(120deg,#487eb0,#fbc531); /* 背景渐变 */
  min-height: 100vh; /* 最小高度 */
}


.container {
  max-width: 800px; /* 最大宽度 */
  margin: auto;
  padding: 10px;
}

.txtb {
  width: 100%;
  border: none; /* 边框无 */
  border-bottom: 2px solid #000; /* 下边框 */
  background: none;
  padding: 10px;
  outline: none; /* 轮廓无 */
  font-size: 18px; /* 字体大小 */
}

h3 {
  margin: 10px 0;
}

.task {
  width: 100%;
  background: rgba(255,255,255,0.5);
  padding: 18px;
  margin: 6px 0;
  overflow: hidden; /* 超出隐藏 */
}

.task i {
  float: right; /* 右浮动 */
  margin-left: 20px;
  cursor: pointer; /* 鼠标样式 */
}

.comp .task {
  background: rgba(0,0,0,.5);
  color: #fff; /* 颜色 */
}

```
### JS
```javascript
// 添加事件
$(".txtb").on("keyup",function(e){
  //13  对应的是enter按钮
  if(e.keyCode == 13 && $(".txtb").val() != "")
  {
    // 添加一个元素内容(添加的内容主框体)
    var task = $("<div class='task'></div>").text($(".txtb").val());
    // 删除按钮
    var del = $("<i class='fas fa-trash-alt'></i>").click(function(){
      // 获取父元素
      var p = $(this).parent();
      // jq淡出效果隐藏
      p.fadeOut(function(){
        //删除元素
        p.remove();
      });
    });
    // 同上
    var check = $("<i class='fas fa-check'></i>").click(function(){
      var p = $(this).parent();
      p.fadeOut(function(){
        $(".comp").append(p);
        // 淡入
        p.fadeIn();
      });
      $(this).remove();
    });

    task.append(del,check);
    $(".notcomp").append(task);
      //清除输入
    $(".txtb").val("");
  }
});
```
==教程地址==：[原文地址（YouTube）](https://youtu.be/h7gZY3_3Dqs)

==B站教程==：[原文转载（bilibili）](https://www.bilibili.com/video/av91020879)