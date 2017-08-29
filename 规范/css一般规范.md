# css编码规范

### 空格建议

- 选择器与`{`之间添加空格
- 多选择器`,`后添加空格，多属性`,`后添加空格
- 属性值`：`后添加空格

### 长度控制
除url外其它代码要控制长度不超过120字符，对多属性在空格处或`，`处合理换行

### 选择器

- 当一个rule包含多个selector时，每个选择器占4一行（`,`处换行）
- `>`、`+`、`~`；两边各留空格
- 属性选择器值用双引号

### 属性
- 属性书写，单起一行，且加分号

## 通用

### 选择器

- 不写空选择器
- 不要将`id`、`class`选择器与元素选择器混用
- 选择器嵌套尽量少于等于三级

### 属性
- 尽量使用属性缩写
- 属性书写顺序
```
.example{
	/*formatting modal*/
	content
	position
	top
	right
	bottom
	left
	float
	display
	overflow
	z-index
	/*box modal*/
	border
	margin
	padding
	width
	height
	/* typographic*/
	font
	line-height
	text-align
	word-wrap
	/*visual*/
	background
	color
	transition
	list-style
}
```
- 带前缀的属性，从长到短排列，以冒号对齐

### 清除浮动
- 触发BFC
	- float非none
	- position非static
	- overflow非visible
- clearfix 在伪类上添加

### ！important
- 尽量不使用`！important`

### z-index
- z-index最大值2147483647，只用于第三方环境防覆盖（添加`！important`）
- 一般最大设置为999999

### 数值
为0-1之间小数时，省略`0`

### url
- url中路径建议不加引号
- url中地址建议省去协议名

### 单位
长度为0时，省略单位

### 颜色
- 颜色建议不使用色值名
- 同一使用大写或小写
- 尽可能使用3个字符的16进制颜色

### 字体建议
- pc字体不小于12px
- `font-style` 只使用`normal`
- `font-weight`建议使用数字，700及以上为blod，以下为normal

### 注释
- 对hack代码添加注释
- 对代码段增加注释
- 对特殊代码增加注释

### class命名
- 只使用小写字符及`-`来命名class
- class名称尽可能简短明了
- 使用有意义的名称，不要使用表现形式（样式）的名称
- 一般，基于最近父元素的class为前缀扩展


### 样式内容
一般项目要对样式进行基本分块
- 重置样式
- 全局样式
- 工具样式
- 根据组件及模块进行代码分块及命名空间划分

### Margin Collapse

由于上下盒模型之间margin值会叠加，只会保留最大值，所以建议使用margin-bottom来撑开边距。

### 使用reset

因为浏览器特性实现并不一致，所以建议使用css reset.
- normalize.css
- minireset
- ress

### 一切使用border-box

设置所有块状元素
```
box-sizing: border-box;
```

### 图片尽量使用背景图

图片使用
```
background: url('./bg.png') center center cover;
```
可以很好的按比例缩放。但是也存在问题：
- 无法设置图片懒加载
- 图片无法被搜索引擎抓到
- object-fit可以解决部分问题(兼容问题)

### 避免重复代码

大部分css属性都是可以继承的，所以不需要复写的，就不要重复写。

### 使用transform添加CSS Animations

在使用动画改变元素的width/height/left/right/top/bottom时，可以优先使用transform来提供更平滑的变化。

[W3C-CSS校验地址](http://jigsaw.w3.org/css-validator/)
