---
title: Markdown快速入门
date: 2017-2-18 17:00:52
tags: 
 - 笔记
categories: 
 - 笔记
---
Markdown是一种可以使用普通文本编辑器编写的标记语言，通过简单的标记语法，它可以使普通文本内容具有一定的格式。
## 1、为什么要用Markdown，它有哪些优点
- Markdown的语法简洁明了、学习容易，而且功能比纯文本更强，因此有很多人用它写博客。世界上最流行的博客平台WordPress和大型CMS如Joomla、Drupal都能很好的支持Markdown。完全采用Markdown编辑器的博客平台有Ghost和Typecho。
- 写作中添加简单符号即完成排版，所见即所得。让你专注于文字而不是排版
- 格式转换方便，Markdown 的文本你可以轻松转换为 html、pdf等。
- 可以保存称纯文本，程序员做笔记很方便
## 2、常用的Markdown 编辑器
- VScode 跨平台，既能写代码，也能做笔记
- Atom Github出品
- 有道云笔记 普通用户有3G空间，可以PC端，移动端自动同步
## 3、Markdonw 常用语法

### 1 标题
标题是每篇文章必备而且最常用的格式。

在Markdown中，如果想将一段文字定义为标题，只需要在这段文字前面加上 #，再在 # 后加一个空格即可。还可增加二、三、四、五、六级标题，总共六级，只需要增加 # ，增加一个 # ，标题字号相应降低一级。
```
# 一级标题 h1
## 二级标题 h2
### 三级标题 h3
#### 四级标题 h4
##### 五级标题 h5
###### 六级标题 h6
```

效果:

# 一级标题 h1
## 二级标题 h2
### 三级标题 h3
#### 四级标题 h4
##### 五级标题 h5
###### 六级标题 h6

### 2 列表
列表格式也很常用，它可以让你的文稿变得井井有条。

在 Markdown 中，你只需要在文字前面加上 - 就可以了；如果你希望是有序列表，在文字前面加上 1. 2. 3. 即可。
<img src="https://raw.githubusercontent.com/fengchunsgit/note/master/imgs/2-1-%E5%88%97%E8%A1%A8.png" >

### 3 引用
如果你需要在文稿中引用一段别处的句子，那么就要用到「引用」格式。

在引用文字前加上 > 并与文字保留一个字符的空格，即可。
<img src="https://raw.githubusercontent.com/fengchunsgit/note/master/imgs/2-2%E5%BC%95%E7%94%A8.png" >
### 4 粗体和斜体
Markdown 的粗体和斜体也非常简单：

用两个 * 包含一段文本就是粗体的语法；

用一个 * 包含一段文本就是斜体的语法。
<img src="https://raw.githubusercontent.com/fengchunsgit/note/master/imgs/2-3-%E7%B2%97%E4%BD%93%E6%96%9C%E4%BD%93.png" >

### 5 链接与图片
链接：在 Markdown 中，插入链接只需要使用 `[显示文本](链接地址)`即可。

图片：在 Markdown 中，插入图片只需要使用 `![显示文本](图片链接地址)`即可。

也可以使用 `src` 标签,并设置 `width` , `height` 等属性调整图片大小
```html
<img src="https://raw.githubusercontent.com/fengchunsgit/note/master/imgs
/2-4%E9%93%BE%E6%8E%A5%E4%B8%8E%E5%9B%BE%E7%89%87.png" width="600px">
```

<img src="https://raw.githubusercontent.com/fengchunsgit/note/master/imgs/2-4%E9%93%BE%E6%8E%A5%E4%B8%8E%E5%9B%BE%E7%89%87.png" >

### 6 分割线
分割线的语法只需要另起一行，连续输入三个星号 *** 即可分割两段文字内容。

如图：

<img src="https://raw.githubusercontent.com/fengchunsgit/note/master/imgs/2-5-%E5%88%86%E5%89%B2%E7%BA%BF.png" >

### 7 表格
当你需要在Markdown文稿中键入表格，代码如下：

<img src="https://raw.githubusercontent.com/fengchunsgit/note/master/imgs/2-6%E8%A1%A8%E6%A0%BC.png" >

### 8 待办和清单
待办事项和清单在日常工作、生活中经常被使用。

在Markdown中，你只需要在待办的事项文本或者清单文本前加上- [ ]、- [x]即可。

- [ ] 表示未完成，- [x] 表示已完成。

注：键入字符与字符之间都要保留一个字符的空格。

具体呈现如下：

<img src="https://raw.githubusercontent.com/fengchunsgit/note/master/imgs/1-2%E5%BE%85%E5%8A%9E%E4%BA%8B%E9%A1%B91.png" >


### 9 流程图
在Markdown中，一段流程图语法以 “` 开头，以 “` 结尾。

在 “` 后另起一行，书写graph XX，用以确定将要绘制的流程图及其类型（XX表示流程图类型）。

流程图分为竖向和横向两大类，竖向包括自上而下和自下而上两种顺序，横向包括从右到左和从左到右两种顺序。

其对应语法分别为：graph TB/graph BT/graph RL/graph LR。

TB - top bottom（自上而下）
BT - bottom top（自下而上）
RL - right left（从右到左）
LR - left right（从左到右）
简单示例如图：

<img src="https://raw.githubusercontent.com/fengchunsgit/note/master/imgs/%E6%B5%81%E7%A8%8B%E5%9B%BE1.png" >


### 10 甘特图
我们在工作中用甘特图作计划进度表、项目进度表再合适不过了。

以如下甘特图为例说明，



与流程图一样，Markdown中，甘特图的语法也是以 “` 开头，以 “` 结尾。

在 “` 后另起一行，书写 gantt ，用以确定将要绘制的是甘特图。

标题的书写语法如下：


<img src="https://raw.githubusercontent.com/fengchunsgit/note/master/imgs/%E7%94%981.png" >

<img src="https://raw.githubusercontent.com/fengchunsgit/note/master/imgs/%E7%94%982.png" >



dateFormat YYYY-MM-DD规定了时间轴，title （标题文本）表示甘特图标题。

如需按项目进行划分，需键入section，空一个字符，再输入项目名称的文本（一个section和另一个section之间要空行）。

每个大项目将拆解为若干个小任务，只需在section之后另起一行，直接输入小项目名称即可。

更详细的甘特图语法，参见：http://knsv.github.io/mermaid/#styling39

### 11 代码
单行代码使用反单引号 `,即tab键上面的那个键（反单引号也称重音符，是西文字符，主要用于计算机相关领域。位置在键盘中数字键“1”的左边，其上档符号是“~ ”，使用Shift键可以换挡输入。由于计算机显示的原因，反单引号非常容易和单引号 ‘ 混淆。）

多行代码使用两组，每组3个`，进行包裹，后面加语言名称，进行高亮显示
<img src="https://raw.githubusercontent.com/fengchunsgit/note/master/imgs/1-1%E4%BB%A3%E7%A0%81%E9%AB%98%E4%BA%AE.png" >
```javascript
console.log('markdonw')
```

语法主要参考有道笔记:

[【简明版】有道云笔记Markdown指南](http://note.youdao.com/iyoudao/?p=2411)

[【进阶版】有道云笔记Markdown指南](http://note.youdao.com/iyoudao/?p=2445)