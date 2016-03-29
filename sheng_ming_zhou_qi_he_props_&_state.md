# 声明周期和props & state

问题是这样的.

我在`componentDidMount`中添加一个ajax请求,但是有一个刷新按钮,通过prpos传递给React一个id,React根据此id执行url刷新组件.

先看看一看React的生命周期图

![React声明周期图](3-3-component-lifecycle.jpg)

在第一次加载React组件时,我通过componentDidMount里执行ajax来更新state,这里没有问题

关键是我点击了刷新,通过props传递给react一个id,然后根据id执行ajax刷新state.这时就出现当前props不是新传递进来的props引起的问题

先看看点击刷新后执行的传递id代码

```javascript
 console.log("new params" + index);
React_DOM.render(
    <Dialog
        params={{
            "id" : index,
        }}
        />,
    document.getElementById("example")
);
```

