# Redux+React使用Ajax

## 1.在store中配置中间件

```javascript
define(function(require,exports) {
    const {createStore , applyMiddleware} = require('redux');
    const {order} = require('../reducers/index');
    const  {thunkMiddleware} = require('redux-thunk');
    
    exports.configureStore = function(initialState){
        const store = createStore(order,initialState,applyMiddleware(thunkMiddleware));

        return store;
    }
});
```

就是吧`redux-thunk`引入到store前

##2. action使用

```javascript
    function getUser(users){
        return {
            type: "LOAD_USERS",
            users: users
        }
    }

  exports.loadUsers = function(){
      const param = {
          activity_id: 4583,
          application_status: 1,
          pay_status: 2,
      }
        return (dispatch, getState) => {
            return $.getJSON(url,param,function(result){
                dispatch(getUser(result));
            });
        }
    }
```


