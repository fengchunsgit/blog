---
title: 打包工具gulp
date: 2017-11-4 21:40:33
tags: 
- 打包工具
categories: 
- 打包工具
---
# 代码打包工具

-  Grunt 自动化构建工具
-  [glup](gulpjs.com) 自动化构建工具 [gulp中文网](www.gulpjs.com.cn)
-  Webpack 静态资源打包

# gulp使用
```
//初始化项目 npm init

// 安装gulp 
npm i gulp --save-dev

//查看gulp版本
gulp -v

//安装gulp插件
npm i gulp-rev gulp-rev-replace gulp-useref gulp-filter gulp-uglify gulp-csso --save-dev

```
# gulp配置文件 gulpfile.js
>项目根目录下创建任务文件gulpfile.js，并创建任务
修改gulpfile  default 可以直接运行，其他需要写任务名
```
var gulp = require('gulp')
var csso = require("gulp-csso")
var filter = require("gulp-filter")
var rev = require("gulp-rev") //计算文件hash码
var revReplace= require("gulp-rev-replace") //index里面的引用改成新的
var uglify = require("gulp-uglify")
var useref = require("gulp-useref") //通过注释，写一些设置
//gulp-watch 文件变化自动打包
//gulp-postcss 自动给css添加浏览器前缀
//gulp-concat 将多个文件合并成一个文件
//gulp-responsive 自动生成相应式图片
//gulp- 再npm中寻找其他的插件

gulp.task('default', function () {
    var jsFilter=filter('**/*.js',{restore:true})
    var cssFilter=filter('**/*.css',{restore:true})
    var indexHtmlFilter=filter(['**/*','!**/index.html'],{restore:true})

    return gulp.src('src/index.html')
    .pipe(useref())
    .pipe(jsFilter)
    .pipe(uglify())
    .pipe(jsFilter.restore)
    .pipe(cssFilter)
    .pipe(csso())
    .pipe(cssFilter.restore)
    .pipe(indexHtmlFilter)
    .pipe(rev())
    .pipe(indexHtmlFilter.restore)
    .pipe(revReplace())
    .pipe(gulp.dest('dist'))
})

```

# 总结
gulp配置完成后一般不用再修改，而且可以提升工作效率，因此使用熟练gulp是非常值得的