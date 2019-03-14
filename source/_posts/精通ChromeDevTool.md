---
title: 精通ChromeDevTool
date: 2018-08-06 19:39:16
tags:
---

## 查看和编辑CSS

### 基础用法

选中元素，修改element.style，添加属性

向元素添加类

向元素添加伪类

通过修改box修改元素的盒模型


### 高级用法

#### 如何选中一个元素的四种方法

1. 在视口选中元素，右键检查
2. 使用箭头选择
3. 直接在dom tree选择
4. In DevTools, run a query like document.querySelector('p') in the Console, right-click the result, and then select Reveal in Elements panel. 


#### 如何跳转到定义样式的外部文件

1. css文件未被压缩
2. css文件已被压缩：开启css的 source-map， 或者使用 devTool 的format（{}）

#### 选择一个元素实际应用的样式：

> style tab呈现的是一个元素所有被指定的样式，包括被覆盖和重写的样式，computed tab呈现的是一个元素实际应用的样式

1. 查看所有继承属性 show all
2. 使用filter来过滤



## 查看和编辑js   替换掉console.log的调试方法吧

### 基本调试流程

### 适用于各种调试场景的断点类型

### 断点调试

> 如何单步调试代码: https://developers.google.com/web/tools/chrome-devtools/javascript/step-code

#### 单行执行调试
#### 跳过函数内部实现调试
#### 跳出函数调试
#### 执行到断点处调试
#### continue to here调试 ： 只在同一个函数中生效？
#### restart frame调试
#### 强制脚本执行到底B
#### change thread context: 场景：使用web worker或者 service work
#### 使用和编辑本地的，闭包的，全局的属性和变量
#### 查看和使用当前函数使用栈，包括同步和异步: 最上面的是最后调用的函数
#### blackBox script：调试和查看代码调用栈的高级解决方案  Editor pane  & Call Stack pane & BlackBox a script from Settings
#### 通过自定义的debug snippet来调适
#### 通过 watch 正确的js表达式来观察值
#### format 压缩过之后的js代码
#### 直接在 chrome 修改js文件，之后保存，不要刷新，一刷新就没了。然后就能在浏览开启上使用修改过后的js文件内容


## 查看和编辑 ui

### source panel：css修改立即生效，不需要保存；js修改需要保存，但不需要刷新

> DevTools erases your CSS and JavaScript changes when you reload the page. See Set up a Workspace to learn how to save the changes to your file system.

> The top-level, such as top in Figure 1, represents an HTML frame. You'll find top on every page that you visit. top represents the main document frame

#### 使用snippets可以为自己的代码调试赋能

比如零时引入jquery

#### 使用workspace来进行本地持久化开发和保存，这样就使得 chrome基本变成了一个 code editor


## 网页性能调优

> 网页性能调优：https://developers.google.com/web/tools/chrome-devtools/speed/get-started