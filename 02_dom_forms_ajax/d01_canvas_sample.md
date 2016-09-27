## Canvas Walkthrough

#### 1. Define Canvas

```html
<html>
<body>
  <canvas id="myCanvas" width="400" height="400"></canvas>
  <script type="text/javascript">
    var canvas = document.getElementById('myCanvas');
    var ctx = canvas.getContext('2d');

    ctx.fillStyle = "rgb(100, 200, 160)";
    ctx.fillRect (0, 350, 100, 50);
	</script>
<body>
</html>
```

#### 2. Draw a square in each corner

Change the javascript in the boiler plate so there is a 50x50 square in each corner of the canvas.

```javascript
ctx.fillStyle = "red";
ctx.fillRect (0, 0, 50, 50);

ctx.fillStyle = "blue";
ctx.fillRect (350, 0, 50, 50);

ctx.fillStyle = "red";
ctx.fillRect (350, 350, 50, 50);

ctx.fillStyle = "blue";
ctx.fillRect (0, 350, 50, 50);
```
