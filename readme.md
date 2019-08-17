# 原生微信小程序框架

**详细参考代码和官方文档**


## 项目结构（分包）

- pages 主包
- packageA 分包（应项目大小而定）
- 整个小程序所有分包大小不超过 8M
- 单个分包/主包大小不能超过 2M

## 页面组成

> 开发者工具创建 自动生成

- xxx.wxss 样式
- xxx.wxml 结构
- xxx.js 
- xxx.json 页面私有配置

## 页面生命周期

- 开发者工具创建 自动生成


## 自定义组件以及通信


## 模板（只做展示结构数据）
```

<template is="temp1" data="{{tempName,staffA}}" />

```
> 1. 一定要 data。
> 2. 存在作用域 只能访问 data 中的数据。

## 界面适配设计稿

- 按照 750 标准设计稿执行


## 动态样式以及类

```

	class="cla1,{{rule?'cla2':'cla3'}}"
	
	style="color:{{color}}"

```

## 公共函数的封装与引用


## wxs的使用

* 每一个 .wxs 文件和 <wxs> 标签都是一个单独的模块。
* 每个模块都有自己独立的作用域。即在一个模块里面定义的变量与函数，默认为私有的，对其他模块不可见。
* 一个模块要想对外暴露其内部的私有变量与函数，只能通过 module.exports 实现。
* 在.wxs模块中引用其他 wxs 文件模块，可以使用 require 函数。 绝对路径 单例 不引用不解析
* 按照官方文档 数据操作参照 es5

## 登录处理


## tips

- .json文件不可注释。
- 可用block块结合wx:if/wx:for来实现一块代码的操作，block不翻译，起包裹作用。
- .wxml 中的 {{}} 可进行 三目 运算 不能使用一些js对象操作，如Math.,JSON.。
