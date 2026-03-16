# 5400-Assignment6

```
let cells = [];

function setup() {
  createCanvas(600, 600);
  cells = Array(width).fill(0);
  cells[floor(width/2)] = 1; 
}

function draw() {
  for (let x = 0; x < width; x++) {
    if (cells[x] == 1) point(x, frameCount);
  }

  let next = [];
  for (let i = 1; i < width-1; i++) {
    next[i] = cells[i-1] ^ cells[i+1]; 
  }

  cells = next;
  if (frameCount > height) noLoop();
}
```
