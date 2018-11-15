---
title: canvas入门
date: 2017-3-15 23:37:18
tags: 
 - canvas
categories:
 - canvas
---
# 创建canvas
- HTML
```
<canvas id='canvas'></canvas>
```
- JavaScript
```
    window.onload=function(){
      var canvas=document.getElementById('canvas')
      var context=canvas.getContext('2d');
    }

```

# 绘制直线，多边形和七巧板
```
  <canvas id="canvas">
    <!-- 支持浏览器，不会显示canvas中的文字，可以用来兼容比较老的浏览器，提醒用户升级 -->
    您的浏览器不支持，请升级您的浏览器
  </canvas>

  <script>
    window.onload = function () {
      var canvas = document.getElementById('canvas')

      canvas.width = 1024
      canvas.height = 768
      var context = canvas.getContext('2d');

      context.beginPath()
      // draw a line
      context.moveTo(100, 100) //state
      context.lineTo(700, 700) //state
      context.lineTo(100, 700)
      context.lineTo(100, 100)
      context.closePath()
      context.lineWidth = 5
      context.strokeStyle = "red"

      // context.fillStyle="rgb(2,100,100)"
      // context.fill()

      context.stroke() //draw

      context.beginPath()
      context.moveTo(200, 100)
      context.lineTo(700, 600)
      context.closePath()

      context.strokeStyle = "black" //reset color canvas是基于状态的，因此会覆盖第一次绘制的红色三角形
      context.stroke()

    }

```

>可以使用直线画一个七巧板



# 绘制弧和圆
```
context.arc(
centerx,centery,radius,
startingAngle,endingAngle,
anticlockwise=false
)
```

![](https://img4.mukewang.com/5af94a1e00016cb512800720.jpg)

# 电子钟绘制
- 数字点阵绘制
![](https://img3.mukewang.com/5bed43540001ef5812800720.jpg)

- 小圆圆心计算方法
 
![](https://img2.mukewang.com/5bed46ec0001ead612800720.jpg)

# 动画 Animation
```
//最简单的动画实现
//执行时间并不准确，不精确
setInterval(
function(){
    render();
    update();
},50)

```

# canvas小球滚动
```
<!DOCTYPE html>
<html>
<style>
  #canvas {
    border: 1px solid #000;
  }

</style>


<head>
  <meta charset="utf-8" />
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <title>canvasBall</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">

</head>

<body>
  <canvas id="canvas"></canvas>
  <script>
    var ball = {
      x: 512,
      y: 100,
      r: 20,
      g: 5,
      vx: 10,
      vy: -0,
      color: '#005588'
    }

    window.onload = () => {
      var canvas = document.getElementById('canvas')

      canvas.width = 1024
      canvas.height = 768

      var context = canvas.getContext('2d')

      setInterval(() => {
        render(context)
        update()
      }, 50);
    }

    function update() {
      ball.x += ball.vx
      ball.y += ball.vy
      ball.vy += ball.g

      //碰到边界
      if (ball.y >= 768 - ball.r) {
        ball.y = 768 - ball.r
        ball.vy = -ball.vy * 0.5 //损耗
      }
      if (ball.x >= 1024 - ball.r) {
        ball.x = 1024 - ball.r;
        ball.vx = -ball.vx;
      }
      if(ball.x<ball.r){
        ball.x=ball.r;
        ball.vx=-ball.vx;
      }
    }

    function render(cxt) {
      cxt.clearRect(0, 0, canvas.width, canvas.height)

      cxt.fillStyle = ball.color
      cxt.beginPath()
      cxt.arc(ball.x, ball.y, ball.r, 0, 2 * Math.PI)
      cxt.closePath()

      cxt.fill()
    }

  </script>

</body>

</html>
```