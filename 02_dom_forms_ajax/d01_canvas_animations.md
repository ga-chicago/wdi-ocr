## Animations in Canvas

* Redraw the canvas every 15 ms
* Take a canvas drawing of a square, and redraw it every 20 ms with a slightly different position.

```javascript
var canvas = document.getElementById('myCanvas');
var ctx = canvas.getContext('2d');

var x = 0;
var draw = function() {
  //THIRD
  //clear background
  ctx.fillStyle = "gray";
  ctx.fillRect(0,0, canvas.width, canvas.height);

  //SECOND
  //move the square to the right
  x += 1;
  //FOURTH
  //make sure it doesn't go off the screen though
  if (x > canvas.width) {
    x %= canvas.width;
    x = 0;
  }
  // FIRST
  //draw square in new position
  ctx.fillStyle = "red";
  ctx.fillRect (x, 300, 100, 50);
}

setInterval(draw, 15);
```
