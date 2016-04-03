# API

1. `bindActionCreators`: 能自动将多个action创建函数绑定到dispatch()方法中
2. `createStore(reducer, [initialState])`: 

    1. 参数: 
      1. renducer(function): 接受两个参数,分别是当前的state树和要处理的action,返回新的state树
      2. initialState: 初始时的state
    2. 返回值: 新的state树
3. `Store`: 支持方法: 
  
    1. getState: 返回当前的state树,与最后一个reducer返回值相同.
    2. dispath(action): 分发action,触发state变化的唯一路径.