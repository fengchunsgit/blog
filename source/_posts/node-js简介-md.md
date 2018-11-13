---
title: Node.js简介
date: 2017-11-13 17:34:32
tags: 
 - 笔记
categories: 
 - node.js
---
>Node.js是一个基于Chrome V8 引擎的JavaScript运行环境，Node.js使用了一个事件驱动、非阻塞I/O模型，使其轻量又高效。node.js的包管理器npm，是全球最大的开源生态系统。

[官网 nodejs.org](https://nodejs.org/en/)

[中文 nodejs.cn](https://nodejs.cn)

```
var fs=require('fs')

//异步方法
fs.readFile('readme.txt','utf-8',function(err,data){
	if(err){
	console.log(err)
	}else{
	console.log(data)
	}
})

//同步方法
var data=fs.readFileSync('readme.txt','utf-8');
console.log(data);
```

## npm
[npm官网](https://www.npmjs.com/)
```
npm -v
npm install jquery  包名区分大小写

package.json 定义了 
可以使用npm init 创建新的package.json,
模块命名不能有大写，不能有空格等

dependencies 生成环境
devDependencies 开发环境
jQuery^1.7.4  大于1.7.4,且大版本要一致
jQuery~1.7.4  前两位要一致，最后一位1.7.x  ~1.7 1.x
jquery 1.7.4 精确匹配

npm i --production
npm i --dev
npm - -g
npm i --save  更新package.json
```

### 轻量级服务器
- http-server
- lite-server
