``` javascript
const element = <h1 className="element-style">jsx style element</h1>
```

JSX是一种JavaScript的语法拓展，React官方也推荐使用这种写法来描述用户界面，React对于JSX有特殊的渲染机制，类似上述代码会被Babel转换为一个更加具象的样子

``` javascript
 const element = React.createElement(
     'h1',
     {className: 'element-style'},
     'jsx style element'
 )
```

React通过读取上述对象来构建DOM并保持数据内容一致