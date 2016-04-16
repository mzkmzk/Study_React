# redux-thunk引入

## 1. 问题

因为我是通过自己项目配置的`requirejs`,所以无法引用npm安装`redux-thunk`

所以只能愚蠢的拷贝`redux-thunk`中lib的代码

但是会出现`redux.js middleware is not a function`的问题

## 2. 过程

先来看看`redux-thunk的代码`

```javascript
'use strict';

function thunkMiddleware(_ref) {
  var dispatch = _ref.dispatch;
  var getState = _ref.getState;

  return function (next) {
    return function (action) {
      return typeof action === 'function' ? action(dispatch, getState) : next(action);
    };
  };
}

module.exports = thunkMiddleware;
```

代码的具体作用可以参考<https://github.com/react-guide/redux-tutorial-cn/blob/master/09_middleware.js>

为了我们自己项目的`requirejs`就改成了

```javascript
'use strict';

define(function (require, exports) {
    function thunkMiddleware(_ref) {
        var dispatch = _ref.dispatch;
        var getState = _ref.getState;

        return function (next) {
            return function (action) {
                return typeof action === 'function' ? action(dispatch, getState) : next(action);
            };
        };
    }
    exports.thunkMiddleware = thunkMiddleware;
});
```

然后 浏览器就开始报错了.


