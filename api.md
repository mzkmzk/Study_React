# API

1. `bindActionCreators`: 能自动将多个action创建函数绑定到dispatch()方法中
2. `createStore(reducer, [initialState])`: 

    1. renducer(function): 接受两个参数,分别是当前的state树和要处理的action,返回新的state树
    2. initialState: 初始时的state

