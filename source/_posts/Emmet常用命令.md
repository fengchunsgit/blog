---
title: Emmet常用命令
date: 2017-3-3 20:07:14
tags: 
- HTML
categories: 
- 笔记
---
>使用Emmet插件能够大幅度提升编写HTML和CSS的效率，许多IDE也内置了Emmet，[官方网站 emmet.io](https://emmet.io/)
## html和css缩写
```
html:5 html5结构
hdr header
ftr footer
bdrs10  border-radius: 10px;
```
## Emmet基本用法
- 子元素 > 
- 同级元素 + 
- 爬升 ^ 
- 重复 * 
- 调整组合顺序 () 

>div>ul>li*3

```
<div>
    <ul>
        <li></li>
        <li></li>
        <li></li>
    </ul>
</div>
```
    
>div+div+p

```
<div></div>
<div></div>
<p></p>
```
>div>div^p

```
<div>
    <div></div>
</div>
<p></p>
```

>(header>div>ul>li*4)+footer

```
<header>
    <div>
        <ul>
            <li></li>
            <li></li>
            <li></li>
            <li></li>
        </ul>
    </div>
  </header>
  <footer></footer> 
```
## Emmet属性
- id # 
- class . 
- 自定义属性 [] 
- 变量 $
- 文字 {}
- 无意义文字 lorem

>div#container.container[data-value]

```
<div id="container" class="container" data-value=""></div>
```

>ul>li.item$*5

```
<ul>
    <li class="item1"></li>
    <li class="item2"></li>
    <li class="item3"></li>
    <li class="item4"></li>
    <li class="item5"></li>
</ul>
```

>ul>li.item-$*5

```
<ul>
    <li class="item-1"></li>
    <li class="item-2"></li>
    <li class="item-3"></li>
    <li class="item-4"></li>
    <li class="item-5"></li>
</ul>
```

>a{click me}

```
<a href="">click me</a>
```

>lorem10 创造10个无意义文字

```
Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum, laborum.
```


## 注意事项
- tab键进行展开，跳转
- 光标一定要在最后
- 中间一定不能有空格