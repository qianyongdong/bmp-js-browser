# bmp-js-browser

在浏览器环境中解码并预览 bmp 图片

**npm 链接**

[https://www.npmjs.com/package/bmp-js-browser](https://www.npmjs.com/package/bmp-js-browser)

**安装**

```npm
npm install bmp-js-browser --save
```

**使用**

```javascript
import BmpJs from 'bmp-js-browser';

const src = '你的 bmp 图片地址';

fetch(src).then(async (res) => {
  const arrayBuffer = await res.arrayBuffer();
  const canvas = document.createElement('canvas');
  const imageData = decode(arrayBuffer);
  canvas.width = imageData.width;
  canvas.height = imageData.height;
  const ctx = canvas.getContext('2d');
  ctx.putImageData(imageData, 0, 0);
  document.body.appendChild(canvas);
});
```
