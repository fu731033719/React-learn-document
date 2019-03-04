简单的理解组件的Props它相当于一个外部传值，因为每个组件皆可具象为一个函数，而Props则是外部控制组件展示的一个手段

```javascript
 class OneComponent extends Component{
     render() {
         return <h1>Hello, {this.props.name}</h1>
     }
 }

 const useComponent = <OneComponent name="user"/>
```
组件的Props的存在给与React项目的构建给予了极大的灵活性，但是值得注意React官方提倡Props的只读性，修改不直接在Props上进行。


对比Props,State是一个组件的局部状态，类似于一个内部传值
```javascript
class OneComponent extends Component{
    constructor () {
        super()
        this.state = { isActive: false }
    }
     render() {
         return(
        <h1>
            Hello, You are {this.state.isActive ? '激活' : '未激活'}
        </h1>
        ) 
     }
 }
```
React.js 的 state 就是用来存储这种可变化的状态的。
每个组件都需要尽量以stateless为核心思想去构建，这样的组件才能在业务复杂的场景下保持高维护及高可读性。