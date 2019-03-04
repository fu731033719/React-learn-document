React中一切皆组件，而一个组件类必须要实现一个render方法。
``` javascript
import React { Component } from 'react';

class OneComponent extends Component {
    render () {
        return (
            <div>I`m a component</div>
        )
    }
}

export default OneComponent;
```
render必须返回一个JSX元素，并列返回多个JSX对象是不合法的，
``` javascript
···
return (
    <div>I`m a fir jsx</div>
    <div>I`m a sec jsx</div>
)
···
```
render函数内可以包裹表达式，这样我们可以更加灵活的对组件的展示进行灵活控制
``` javascript
···
render () {
    const component_name = 'some name'
    return (
        <div>I`m a `${component_name}`</div>
    )
}
···
```

单一jsx返回有时候会对我们的页面布局造成影响，当我们想隐藏jsx最外层的div包裹时，可以使用Fragment标签进行包裹
``` javascript
import React { Component, Fragment } from 'react';

class OneComponent extends Component {
    render () {
        return (
            <Fragment>
                <div>I`m a component</div>
                <div>I`m a sec jsx</div>
            </Fragment>
        )
    }
}
export default OneComponent;
```