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
    3. subscribe(listener): 每当dispath action 的时候会执行回调.返回值是一个可以解绑变化监听的函数
    4. replaceReducer(nextReducer): 替换store当前用来计算state的reducer
    