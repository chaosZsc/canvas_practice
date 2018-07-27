# [canvas_practice](https://chaoszsc.github.io/canvas_practice/)
《Canvas: Draw on the web》——学习实践canvas

## 1. [从线条开始](./src/index1.html)
```javascript
// 获取画笔
const canvas = document.querySelector('#canvas'); // 假设有一张id为canvas的画布
const context = canvas.getContext('2d');
// 画布形成一张以左上角为原点，y轴正方向向下，x轴正方向向右的坐标轴

// 移动到起点坐标(100, 100)
context.moveTo(100, 100);
// 连线至坐标(600, 600)
context.lineTo(600, 600);
// 线条宽度
context.lineWidth = 5;
// 描边颜色
context.strokeStyle = '#000000';
// 描边
context.stroke();
```

## 2. [多线条组成图形](./src/index2.html)
```javascript
// 设定绘制起始处
context.beginPath();
```

## 3. [绘制矩形](./src/index3.html)
```javascript
// 闭合图形(最后一笔可以不画)
context.closePath();
// 按教程不闭合图形时，最后接缝处会有缺口，现在最新Chrome浏览器中没有出现，估计是优化了。。。

// 填充颜色
context.fillStyle = 'yellow'

// canvas 矩形api
context.rect(x, y, width, height);
```
>[**魔性方块**](./src/index3-1.html)

## 4. 线条的属性
1. [`lineCap`](./src/index4-1.html)  
定义线条两端的样式：
    * `butt`: 默认值，平直边缘。
    * `round`: 以线宽为直径的半圆。
    * `square`: 以线宽为长，以线宽一半为宽的矩形。
2. [`lineJoin`](./src/index4-2.html)  
定义两条线相交的拐角样式：
    * `miter`: 默认值，在连接处边缘延长相接。  
        > [`miterLimit`](./src/index4-3.html)（了解下）
    * `bevel`: 对角线斜角。
    * `round`: 圆。
3. `lineWidth`  
定义线的宽度。
4. `strokeStyle`
定义线边框颜色和样式。