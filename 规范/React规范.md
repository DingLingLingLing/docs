### React 编码规范

#### 基本规范
- 每个文件只包含一个React组件
   - 不限制无状态组件和Pure组件
- 使用JSX语法
- 不使用`React.createElement`语法
- 编写必要注释
- 使用基本的ES6语法

####  命名
- 扩展名： 扩展名使用js或jsx ？
- 文件名：文件名使用帕斯卡命名，即大驼峰命名，如：ReferenceComponent.js
- 引用命名：React组件名也使用帕斯卡命名，引用实例采用驼峰命名。
- 组件命名：组件名应该和文件名一致，如果是目录中的组件，要是有index.jsx作为文件名，并使用文件夹名称作为组件名。
- 组件仓库命名为小写和“-”连接，如bee-button、bee-button-group
- 带命名空间的组件，如果一个组件包含只有自身使用的子组件，以该组件为命名空间编写组件，例如Table，Table.Head

#### 声明
- 不要使用`displayName`来命名组件，应使用类的引用名称。
```
// bad
export default React.createClass({
  displayName: 'ReservationCard',
  // stuff goes here
});

// good
export default class ReservationCard extends React.Component {
}
```

#### 对齐
- JSX语法使用下列对齐方式
```
// bad
<Foo superLongParam="bar"
     anotherSuperLongParam="baz" />

// good
<Foo
  superLongParam="bar"
  anotherSuperLongParam="baz"
/>

// 如果组件的属性可以放在一行就保持在当前一行中
<Foo bar="bar" />

// 多行属性采用缩进
<Foo
  superLongParam="bar"
  anotherSuperLongParam="baz"
>
  <Quux />
</Foo>
```

#### 引号
- JSX属性使用双引号，其他js使用单引号

#### 空格
- 代码缩进使用`tab`键（4个空格）。
- 自闭和标签`/`前加一个空格。

#### 属性
- 属性名称使用驼峰命名。
- 在必要情况下，使用`...others`得到所有其他属性。
- 当属性为布尔类型时，属性值为true时，省略赋值。
```
// bad
<Foo
  hidden={true}
/>

// good
<Foo
  hidden
/>
```
#### 括号
- 使用括号包裹多行JSX标签。

#### 标签
- 当标签没有子元素时，始终自闭和标签。
- 组件有多行属性，关闭标签另起一行。

#### 方法
- render方法中回调函数，在构造函数中进行bind绑定。（箭头函数？）。
- 组件内部方法不使用下划线前缀。

####  ref
- 在非必须情况下，尽量不使用ref操作dom
- 使用ref的callback
```
// bad
<Foo
  ref="myRef"
/>

// good
<Foo
  ref={(ref) => { this.myRef = ref; }}
/>
```

#### 排序

1. constructor
2. getChildContext
3. componentWillMount
4. componentDidMount
5. componentWillReceiveProps
6. shouldComponentUpdate
7. componentWillUpdate
8. componentDidUpdate
9. componentWillUnmount
10. 自定义方法
11. render

#### propTypes和defaultProps
```
/定义prop检验
const propTypes = {
//每一个props都要写注释
}

//定义默认参数
const defaultProps = {

}
/**
 * 定义组件
 */
class Button extends React.Component {
	constructor (props) {
		super(props);
		//定义state
		this.state = {
    //每一个state要写注释
		}
		// 事先声明方法绑定
		this.MyEvent = this.MyEvent.bind(this);
	}

	//组件生命周期方法
    //自定义函数方法，及注释
      MyEvent () {

      }
    


	render () {
		return (
			// <div onClick={this.MyEvent}></div>
		)
	}
}

Button.propTypes = propTypes;
Button.defaultProps = defaultProps;
export default Button;
```

第一版    参考airbnb编码规范