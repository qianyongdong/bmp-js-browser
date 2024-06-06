# bmp-js-browser

在浏览器环境中解码并预览 bmp 图片

#npm link<br/>
https://www.npmjs.com/package/bmp-js-browser

#install <br/>
npm install bmp-js-browser --save

#usage

import BmpJs from 'bmp-js-browser'<br/>

const src = "你的 bmp 图片地址"

fetch(src).then(async(res)=>{
const arrayBuffer = await res.arrayBuffer();
const canvas = document.createElement('canvas');
const imageData = decode(arrayBuffer);
canvas.value.width = imageData.width;
canvas.value.height = imageData.height;
const ctx = canvas.getContext('2d');
ctx.putImageData(imageData, 0, 0);
document.body.appendChild(canvas);
})
