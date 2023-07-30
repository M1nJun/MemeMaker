# MemeMaker

```js
const colors = [
  "#1abc9c",
  "#2ecc71",
  "#3498db",
  "#9b59b6",
  "#34495e",
  "#f1c40f",
  "#e67e22",
  "#c0392b",
];

var x;
var y;
function onClick(event) {
  x = event.offsetX;
  y = event.offsetY;
}

function onMove(event) {
  ctx.beginPath();
  ctx.moveTo(x, y);
  const color = colors[Math.floor(Math.random() * colors.length)];
  ctx.strokeStyle = color;
  ctx.lineTo(event.offsetX, event.offsetY);
  ctx.stroke();
}

canvas.addEventListener("mousemove", onMove);
canvas.addEventListener("click", onClick);
```
