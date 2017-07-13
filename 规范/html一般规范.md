### HTMLһ���Թ淶

#### ���廯
ʹ�÷�������ı�ǩ��д HTML �ĵ�, ѡ��ǡ����Ԫ�ر������ĺ���

#### ������
�������ʹ��div��span�ȱ�ǩ��

#### ��ǩ����
Ԫ�صı�ǩ������������Сд, ����ֵ�����˫����
���Խ���˳��
- class
- id, name
- data-*
- src, for, type, href, value
- title, alt
- role, aria-*

#### Ԫ�رպ�
��ȷʹ���Ապ�Ԫ�غͷ��Ապ�Ԫ�ء����Ապ�Ԫ��һ�����ϱպϱ�ǩ��

#### �����Խ�������
��html��ǩ�ϵ����Խ��������Ա�֤����Ŀɶ��ԡ��������ҵĳ���˳����һ�����Լ����塣
class / id, name / data-* / src, for, type, href / title, alt / aria-*, role

#### ����
ʹ��utf-8����
```
<meta charset="utf-8">
```

#### img
- �����������ʹ��img��ǩչʾͼƬ�������������ʹ��css����չ��ͼƬ��
- ��������imgͼƬ����title���ԣ�����alt���ԡ�
- ��Ҫ��img��src����Ϊ�գ���Ϊ��Щʱ���������������μ��ء�
- �������width��heightʵ�У�����ҳ��������

#### ע��
ʹ��TODO����Ǵ�������
```
<!-- TODO(john.doe): revisit centering -->
```

#### �Զ�������
ͨ����Ԫ�������Զ�������������� JavaScript ����������, ��������ʽΪ data-xx

#### ����
- ���ڱ�ǩǶ��ʱʹ���������ڲ�ͬģ������ʹ�ú���հ׻��ǿ��У��Լ��ʵ�ע�͡�
- һ��ʹ��tab����������������ʹ�ÿո�������
- ����ÿ�в�����120�ַ���

#### Э��ͷ
����ͼƬ���ⲿ��ʽ���ã��ⲿ�ű����ã������ⲿý���ļ�������ʡ��http��https��Э��ͷ���֡�
�����飺
```
<script src="http://jquery/2.1.3/jquery.min.js"></script>
<link rel="stylesheet" href="http://assets/css/style.css"/>
<style>
  .example {
    background: #fff url(http://www.doraemoney.com/assets/img/example-background.png) no-repeat center;
  }
</style>
``` 
���飺
```
<script src="//jquery/2.1.3/jquery.min.js"></script>
<link rel="stylesheet" href="//assets/css/style.css"/>
<style>
  .example {
    background: #fff url(//www.doraemoney.com/assets/img/example-background.png) no-repeat center;
  }
</style>
```

#### �ո�
һ���ǩ�ڲ����ո�����Ҫ���ӿո�ʹ��`&nbsp;`��

#### favicon
��֤favicon�ɷ��ʡ�
һ����������Զ����ʸ�Ŀ¼�µ�`favicon.ico`;
Ҳ����ʹ��link��ǩ�ƶ�:
```
<link rel="shortcut icon" href="path/to/favicon.ico">
```


#### ��ǩ��ʹ�ù���

- ��Ԫ�ص� name �����趨Ϊ action, enctype, method, novalidate, target, submit �ᵼ�±��ύ���ҡ�
- p ��ʾ����. ֻ�ܰ�������Ԫ��, ���ܰ����鼶Ԫ��
- ��Ҫʹ������Ԫ��Ƕ�׿鼶Ԫ��
- a��ǩ��ʾ���ӻ���ê�㣬��Ҫ��a��ǩ��Ƕ�׽������ǩ����button��
- ��ĳЩ�պϵ� `</div>` ��ǩ�Ա߼���һ��htmlע�ͣ�˵������պϵ���ʲôԪ�ء������д���Ƕ�׺�����������»�����á�
- ��Ҫ�ѱ������ҳ�沼�֡�
- ��ÿ��������ֶμ��� `<label> `��ǩ�����е� for ���Ա���Ͷ�Ӧ�������ֶζ�Ӧ�������û��Ϳ��Ե����ǩ��ͬ������ǩ���� cursor:pointer; ��ʽҲ�����ǵ�����
- ��Ҫʹ��������ʽ
- ʡ����ʽ���ű������е�`type`���ԡ�
- ͬһҳ�������ͬ��name��id���ԡ�
- �������͵����ԣ����鲻�������ֵ��
- Ϊ���е�button������Ӧ��type���ԣ�buttonĬ��Ϊ`type="submit"`,��Ҫ����ť���name���ԡ�


#### У��

ʹ��У�鹤����������html���롣
- w3c������У�鹤�� http://validator.w3.org/
- firefox��У���� http://www.w3.org/TR/html4/

#### ����ͷ��ǩ
- ���ñ���
```
<meta charset="utf-8">
```
- ����IE������汾
```
<meta http-equiv="X-UA-Compatible" content="IE=Edge">
```
- �������ԣ�������վ�Ŀɷ�����
```
<html lang="zh-CN">
```
- ���ñ���
```
<meta charset="utf-8">
```
- ��������
```
<meta http-equiv="Content-Language" Content="zh-CN" /> 
```
- �����ض���
```
<meta http-equiv="Refresh" Content="15; Url=http://www.baidu.com" />
```
- ���û���ʱ��
```
 <meta http-equiv="Expires" Content="Web, 26 Jun 2015 18:21:57 GMT" /> 
```
- ��ʹ�û���
```
 <meta http-equiv="Pragma" Content="No-cach" />
```
- ���ùؼ���
```
 <meta name="Keywords" Content="key1,key2,..." /> 
```
- ����������Ϣ
```
<meta name="Description" Content="description abc" />
```
- ���ö���������ץȡ
```
 <meta name="Robots" Content="All|None|Index|Noindex|Follow|Nofollow" /> 
```
- ���ÿ�������
```
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=0" />
```
- ���������ʹ��
```
<!-- ����������ں�ѡ�� --> <meta name="renderer" content="webkit|ie-comp|ie-stand">

 <!-- ʹ�����°��ie�����������chrome--> <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1"/> 
<!-- ����ֳ��豸�Ż�����Ҫ�����һЩ�ϵĲ�ʶ��viewport��������������ݮ -->

 <meta name="HandheldFriendly" content="true">

 <!-- ΢�����ʽ����� --> <meta name="MobileOptimized" content="320"> 

<!-- ucǿ������ --> <meta name="screen-orientation" content="portrait"> 

<!-- QQǿ������ --> <meta name="x5-orientation" content="portrait">

 <!-- UCǿ��ȫ�� --> <meta name="full-screen" content="yes"> 

<!-- QQǿ��ȫ�� --> <meta name="x5-fullscreen" content="true"> 

<!-- UCӦ��ģʽ --> <meta name="browsermode" content="application">

 <!-- QQӦ��ģʽ --> <meta name="x5-page-mode" content="app"> 

<!-- windows phone ����޸߹� --> <meta name="msapplication-tap-highlight" content="no">

 <!-- ��ֹת�� --> <meta http-equiv="Cache-Control" content="no-siteapp" /> 
```
- ���ô˶�Ӧͷ������ie��������
```
 <meta http-equiv="pragma" content="no-cache" > 
 <meta http-equiv="cache-control" content="no-cache" > 
 <meta http-equiv="expires" content="-1" > 
```

#### һЩ�����õ�
- ǿ����ҳ������ʾ,��ֹ������iframe����
```
<meta http-equiv="windows-Target" content="_top">
```
-����ie������
```
<meta http-equiv="Pics-label" content="">
```
- ���������ˢ��
```
<meta http-equiv="refresh" content="1" url="xxx.com">
```

-  �������
-  http://www.w3school.com.cn/tags/tag_meta.asp