# 基础API

1. 遇到`<`开头,用HTML解析,遇到`{`用JS解析
2. `React库`用于生成一个组件
    
    1. createClass用于生成组件(组件名首字母必须大写 & 组件只能有一个顶级标签)
    2. render用于输出组件
3. `this.props.属性` 获取调用本组件时候定义的属性
4. 定义`class`属性时,要写成`className`,定义`for`属性时,要写成`htmlFor`
5. `this.props.children`: 表示组件的所有子节点,可用`React.Children.map`遍历所有子节点
6. 


## 参考资源

基础API <http://www.ruanyifeng.com/blog/2015/03/react.html>

