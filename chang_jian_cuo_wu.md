# 常见错误

## 1. 循环生成相同元素时,建议使用key,例如循环生成li

这并不会引起编译错误,但会引起一个warning

```xml
Warning: Each child in an array or iterator should have a unique "key" prop.
```

我原先的代码是这样的


```javascript
this.props.fields.map(function(){
    return (
        <li>
            ...
        </li>
    )
});
```

