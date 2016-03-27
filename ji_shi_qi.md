# 计时器

```html
<!DOCTYPE html>
<html>
<body>
<div id="container"></div>

<script src="https://fb.me/react-0.14.7.js"></script>
<script src="https://fb.me/react-dom-0.14.7.js"></script>

<script>
    var ExampleApplication = React.createClass({
        render: function() {
            var elapsed = Math.round(this.props.elapsed  / 100);
            var seconds = elapsed / 10 + (elapsed % 10 ? '' : '.0' );
            var message =
                    'React has been successfully running for ' + seconds + ' seconds.';
            return React.DOM.p(null, message);
        }
    });

    var start = new Date().getTime();
    setInterval(function() {
        ReactDOM.render(
                React.createElement(ExampleApplication,{elapsed: new Date().getTime() - start}), 
                document.getElementById('container') 
        );
    }, 50);
</script>
</body>
</html>
```

程序中