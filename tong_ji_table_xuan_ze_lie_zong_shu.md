# 统计table选择列总数

## 1.Redux+React的调用机制

先来看看Redux的架构图

![Redux的架构图](TB1SsWQLFXXXXXMXVXXXXXXXXXX-1170-514.jpg_600x600.jpg)

Views通过用户的交互而触发了`Action Creators`

`Action Creators`的作用就是return一个`Action`

`Action`一般为一个数据对象,该数据对象的作用是给reducer作为参考,如何改变Store

## 2. 功能分析

先看一下重构师给出的页面效果

![示例图](QQ20160408-1.png)


额其实功能很简单.

1. 左上角有统计总人数
2. 人数列可以勾选上
3. 左下角有统计勾选的人数

## 3. 分解View模块



