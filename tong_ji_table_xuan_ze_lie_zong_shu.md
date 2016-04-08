# 统计table选择列总数

先看一下重构师给出的页面效果

![示例图](QQ20160408-1.png)

## Redux+React的调用机制

先来看看Redux的架构图

![Redux的架构图](TB1SsWQLFXXXXXMXVXXXXXXXXXX-1170-514.jpg_600x600.jpg)

Views通过用户的交互而触发了`Action Creators`

`Action Creators`的作用就是return一个`Action`

`Action`一般为一个数据对象,该数据对象的作用是给reducer作为参考,如何改变Store


