### React ����淶

#### �����淶
- ÿ���ļ�ֻ����һ��React���
   - ��������״̬�����Pure���
- ʹ��JSX�﷨
- ��ʹ��`React.createElement`�﷨
- ��д��Ҫע��
- ʹ�û�����ES6�﷨

####  ����
- ��չ���� ��չ��ʹ��js��jsx ��
- �ļ������ļ���ʹ����˹�������������շ��������磺ReferenceComponent.js
- ����������React�����Ҳʹ����˹������������ʵ�������շ�������
- ��������������Ӧ�ú��ļ���һ�£������Ŀ¼�е������Ҫ����index.jsx��Ϊ�ļ�������ʹ���ļ���������Ϊ�������
- ����ֿ�����ΪСд�͡�-�����ӣ���bee-button��bee-button-group
- �������ռ����������һ���������ֻ������ʹ�õ���������Ը����Ϊ�����ռ��д���������Table��Table.Head

#### ����
- ��Ҫʹ��`displayName`�����������Ӧʹ������������ơ�
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

#### ����
- JSX�﷨ʹ�����ж��뷽ʽ
```
// bad
<Foo superLongParam="bar"
     anotherSuperLongParam="baz" />

// good
<Foo
  superLongParam="bar"
  anotherSuperLongParam="baz"
/>

// �����������Կ��Է���һ�оͱ����ڵ�ǰһ����
<Foo bar="bar" />

// �������Բ�������
<Foo
  superLongParam="bar"
  anotherSuperLongParam="baz"
>
  <Quux />
</Foo>
```

#### ����
- JSX����ʹ��˫���ţ�����jsʹ�õ�����

#### �ո�
- ��������ʹ��`tab`����4���ո񣩡�
- �Ապͱ�ǩ`/`ǰ��һ���ո�

#### ����
- ��������ʹ���շ�������
- �ڱ�Ҫ����£�ʹ��`...others`�õ������������ԡ�
- ������Ϊ��������ʱ������ֵΪtrueʱ��ʡ�Ը�ֵ��
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
#### ����
- ʹ�����Ű�������JSX��ǩ��

#### ��ǩ
- ����ǩû����Ԫ��ʱ��ʼ���Ապͱ�ǩ��
- ����ж������ԣ��رձ�ǩ����һ�С�

#### ����
- render�����лص��������ڹ��캯���н���bind�󶨡�����ͷ����������
- ����ڲ�������ʹ���»���ǰ׺��

####  ref
- �ڷǱ�������£�������ʹ��ref����dom
- ʹ��ref��callback
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

#### ����

1. constructor
2. getChildContext
3. componentWillMount
4. componentDidMount
5. componentWillReceiveProps
6. shouldComponentUpdate
7. componentWillUpdate
8. componentDidUpdate
9. componentWillUnmount
10. �Զ��巽��
11. render

#### propTypes��defaultProps
```
/����prop����
const propTypes = {
//ÿһ��props��Ҫдע��
}

//����Ĭ�ϲ���
const defaultProps = {

}
/**
 * �������
 */
class Button extends React.Component {
	constructor (props) {
		super(props);
		//����state
		this.state = {
    //ÿһ��stateҪдע��
		}
		// ��������������
		this.MyEvent = this.MyEvent.bind(this);
	}

	//����������ڷ���
    //�Զ��庯����������ע��
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

��һ��    �ο�airbnb����淶