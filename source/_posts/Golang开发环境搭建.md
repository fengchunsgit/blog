---
title: Golang开发环境搭建
date: 2017-6-16 11:58:40
tags: 
 - Golang
 - 笔记
categories: 
 - Golang
---
# go安装
## 下载
- 官网下载
- [studyGolang下载](https://studygolang.com/dl)


## 安装
- windos 默认安装在`C:/Go/`目录下，要将`path`添加上
- 配置`$GOROOT`

`GOROOT`指向Go开发包的安装目录。从Go 1.0开始，不必显示地设置`GOROOT`环境变量。Windows安装包将会自动设置`GOROOT`，默认装在`C:\Go`：
```bash
GOROOT=C:\Go\
```
而在`*nix`环境下，下载Go安装包并解压在`/usr/local/`目录下，然后把`/usr/local/go/bin`加入`PATH`环境变量即可：
```bash
export PATH=$PATH:/usr/local/go/bin
```
如果Go安装包没有安装在默认的目录下`（Windows为C:\Go，*nix为/usr/local/go）`，则需要手动设置`GOROOT`，举个例子`（*nix）`：
```bash
export GOROOT=$HOME/go

```

- 配置`$GOPATH`

`GOPATH`指定了Go工程目录，包含 `src` ，`pkg` 和 `bin` 三个子目录。这是开发 Go 程序时，唯一需要显示设置的环境变量。当使用go get目录下载Go第三方程序包时，也会安装在这个目录下。此外，为了方便，要记得把`$GOPATH/bin`也加到`PATH`环境变量：
```
export PATH=$PATH:$GOPATH/bin  
```

## hello,world
建立hello.go
```golang
package main

import (
	"fmt"
)

func main(){
	fmt.Println("hello");
}
```
```
go run hello.go

hello //输出

```

# go开发利器vscode

## 安装vscode插件go
>alt+左键点击，进行跳转
## Go开发相关配置
setting.json中进行相关设置
```
{
    
    "files.autoSave": "onFocusChange",
    "go.buildOnSave": true,
    "go.lintOnSave": true,
    "go.vetOnSave": true,
    "go.buildFlags": [],
    "go.lintFlags": [],
    "go.vetFlags": [],
    "go.useCodeSnippetsOnFunctionSuggest": false,
    "go.formatOnSave": true,
    "go.formatTool": "goreturns",
    "go.goroot": "C:\\go",
    "go.gopath": "D:\\go"
}
```
