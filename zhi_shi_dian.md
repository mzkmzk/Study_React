# 知识点

## 1. React生命周期

1. Mounting: 已插入真实DOM
2. Updating: 正在被重新渲染
3. Unmounting: 已移出真实DOM

周期前后触发的函数

1. componentWillMount()
2. componentDidMount()
3. componentWillUpdate(object nextProps,object nextState)
4. componentDidUpdate(object preProps,object preState)
5. componentWillUnmount()

