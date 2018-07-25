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
