### HTML一般性规范

#### 语义化
使用符合语义的标签书写 HTML 文档, 选择恰当的元素表达所需的含义

#### 轻量化
避免过度使用div和span等标签。

#### 标签属性
元素的标签和属性名必须小写, 属性值必须加双引号
属性建议顺序：
- class
- id, name
- data-*
- src, for, type, href, value
- title, alt
- role, aria-*

#### 元素闭合
正确使用自闭合元素和非自闭合元素。非自闭合元素一定加上闭合标签。

#### 对属性进行排序
对html标签上的属性进行排序，以保证代码的可读性。以下是我的常用顺序，你一可以自己定义。
class / id, name / data-* / src, for, type, href / title, alt / aria-*, role

#### 编码
使用utf-8编码
```
<meta charset="utf-8">
```

#### img
- 有下载需求的使用img标签展示图片，无下载需求的使用css背景展现图片。
- 尽量不给img图片增加title属性，增加alt属性。
- 不要让img的src属性为空，因为有些时候会引起浏览器二次加载。
- 建议添加width或height实行，避免页面跳动。

#### 注释
使用TODO来标记待办事项
```
<!-- TODO(john.doe): revisit centering -->
```

#### 自定义属性
通过给元素设置自定义属性来存放与 JavaScript 交互的数据, 属性名格式为 data-xx

#### 缩进
- 请在标签嵌套时使用缩进，在不同模块代码间使用合理空白或是空行，以及适当注释。
- 一般使用tab进行缩进，不建议使用空格缩进。
- 建议每行不超过120字符。

#### 协议头
对于图片，外部样式引用，外部脚本引用，其他外部媒体文件，建议省略http或https等协议头部分。
不建议：
```
<script src="http://jquery/2.1.3/jquery.min.js"></script>
<link rel="stylesheet" href="http://assets/css/style.css"/>
<style>
  .example {
    background: #fff url(http://www.doraemoney.com/assets/img/example-background.png) no-repeat center;
  }
</style>
``` 
建议：
```
<script src="//jquery/2.1.3/jquery.min.js"></script>
<link rel="stylesheet" href="//assets/css/style.css"/>
<style>
  .example {
    background: #fff url(//www.doraemoney.com/assets/img/example-background.png) no-repeat center;
  }
</style>
```

#### 空格
一般标签内不留空格，如需要增加空格，使用`&nbsp;`；

#### favicon
保证favicon可访问。
一般浏览器会自动访问跟目录下的`favicon.ico`;
也可以使用link标签制定:
```
<link rel="shortcut icon" href="path/to/favicon.ico">
```


#### 标签的使用规则

- 表单元素的 name 不能设定为 action, enctype, method, novalidate, target, submit 会导致表单提交混乱。
- p 表示段落. 只能包含内联元素, 不能包含块级元素
- 不要使用内联元素嵌套块级元素
- a标签表示链接或是锚点，不要在a标签内嵌套交互类标签，如button。
- 在某些闭合的 `</div>` 标签旁边加上一段html注释，说明这里闭合的是什么元素。这在有大量嵌套和缩进的情况下会很有用。
- 不要把表格用于页面布局。
- 给每个表单里的字段加上 `<label> `标签，其中的 for 属性必须和对应的输入字段对应，这样用户就可以点击标签。同理，给标签加上 cursor:pointer; 样式也是明智的做法
- 不要使用内联样式
- 省略样式及脚本引用中的`type`属性。
- 同一页面避免相同的name和id属性。
- 布尔类型的属性，建议不添加属性值。
- 为表单中的button声明对应的type属性，button默认为`type="submit"`,不要给按钮添加name属性。


#### 校验

使用校验工具来检查你的html代码。
- w3c的在线校验工具 http://validator.w3.org/
- firefox的校验插件 http://www.w3.org/TR/html4/

#### 常用头标签
- 设置编码
```
<meta charset="utf-8">
```
- 设置IE浏览器版本
```
<meta http-equiv="X-UA-Compatible" content="IE=Edge">
```
- 设置语言，增加网站的可访问性
```
<html lang="zh-CN">
```
- 设置编码
```
<meta charset="utf-8">
```
- 设置语言
```
<meta http-equiv="Content-Language" Content="zh-CN" /> 
```
- 设置重定向
```
<meta http-equiv="Refresh" Content="15; Url=http://www.baidu.com" />
```
- 设置缓存时间
```
 <meta http-equiv="Expires" Content="Web, 26 Jun 2015 18:21:57 GMT" /> 
```
- 不使用缓存
```
 <meta http-equiv="Pragma" Content="No-cach" />
```
- 设置关键字
```
 <meta name="Keywords" Content="key1,key2,..." /> 
```
- 设置描述信息
```
<meta name="Description" Content="description abc" />
```
- 设置对搜索引擎抓取
```
 <meta name="Robots" Content="All|None|Index|Noindex|Follow|Nofollow" /> 
```
- 设置可视区域
```
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=0" />
```
- 设置浏览器使用
```
<!-- 国产浏览器内核选择 --> <meta name="renderer" content="webkit|ie-comp|ie-stand">

 <!-- 使用最新版的ie浏览器，或者chrome--> <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1"/> 
<!-- 针对手持设备优化，主要是针对一些老的不识别viewport的浏览器，比如黑莓 -->

 <meta name="HandheldFriendly" content="true">

 <!-- 微软的老式浏览器 --> <meta name="MobileOptimized" content="320"> 

<!-- uc强制竖屏 --> <meta name="screen-orientation" content="portrait"> 

<!-- QQ强制竖屏 --> <meta name="x5-orientation" content="portrait">

 <!-- UC强制全屏 --> <meta name="full-screen" content="yes"> 

<!-- QQ强制全屏 --> <meta name="x5-fullscreen" content="true"> 

<!-- UC应用模式 --> <meta name="browsermode" content="application">

 <!-- QQ应用模式 --> <meta name="x5-page-mode" content="app"> 

<!-- windows phone 点击无高光 --> <meta name="msapplication-tap-highlight" content="no">

 <!-- 禁止转码 --> <meta http-equiv="Cache-Control" content="no-siteapp" /> 
```
- 设置此对应头可限制ie缓存问题
```
 <meta http-equiv="pragma" content="no-cache" > 
 <meta http-equiv="cache-control" content="no-cache" > 
 <meta http-equiv="expires" content="-1" > 
```

#### 一些不常用的
- 强制网页独立显示,防止被别人iframe调用
```
<meta http-equiv="windows-Target" content="_top">
```
-设置ie中评级
```
<meta http-equiv="Pics-label" content="">
```
- 设置浏览器刷新
```
<meta http-equiv="refresh" content="1" url="xxx.com">
```

-  相关文献
-  http://www.w3school.com.cn/tags/tag_meta.asp