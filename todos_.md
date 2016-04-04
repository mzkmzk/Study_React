# Todos

![todo](QQ20160403-0.png)

# 1. 功能解析

1. 添加todo
2. 点击todo,切换active|completed状态
3. 分类显示

# 2. 功能点解析

## 2.1 添加todo

添加todo的思路就是

点点击`Add Todo`时,当文本框分空,即提交todo

就是执行

1. `dispatch(addTodo(input.value))`;
2. `AddTodo = connect()(AddTodo)`: 将`AddTodo`组件里的dispath和Redux连接起来

`connect()(AppTodo)`的作用就是将AddTodo组件中的dispath交给Redux处理.

View层就就是发送这个通知,后面的事情就不得而知了.

这个文本框和提交按钮的任务就完成了,只负责提交内容,store里的变化与它无关

OK,但是这个addTodo(input.value)究竟咋执行啊

`addTodo`的实现方法放在action中.

```javascript
export const addTodo = (text) => {
  return {
    type: 'ADD_TODO',
    id: nextTodoId++,
    text
  }
}
```

啊..action就是定义了这些东西..action指定了动作的类型,和传输的数据.

恩.通过这里我知道增加一个todo,他的id是`nextTodoId++`,内容为text

