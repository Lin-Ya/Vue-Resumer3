---
title: 408_Vue.js简历编辑器第二版
tags: Vue.js,项目
grammar_cjkRuby: true
---
[预览地址](https://lin-ya.github.io/Vue-Resumer3/dist/)

# 简介
[第一版简历编辑器](https://lin-ya.github.io/Vue-Resumer2/dist/)是我入门学习vue.js的练手项目。初步掌握了vue.js的基本使用，于是决定在改进功能和设计的前提下，再重做一次（~~第一版样式太难看了~~）。

功能上：
- 去除了登录注册模块
- 列表标题自定义
- 所有图标均可自定义
- 增加技能数值槽（不存在100%的技能熟练度滴~）
- 大区块下的各个子项均可增删改
- 增加使用提示

样式上：
- 主题色调一致
- 布局趋同于正式建立
- 提示灯泡有不同的状态

在设计组件上比上一版更加注重组件的复用，所有的区块组件都是由更小的组件组合而成，包括img选择器，数值插槽等等。

![范例](http://p8qvw09e6.bkt.clouddn.com/storyWriter/chrome_2018-08-08_15-38-03.png)

![保存的图片范例](http://p8qvw09e6.bkt.clouddn.com/storyWriter/Resume-test.png "Resume-test")

# Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

Done
