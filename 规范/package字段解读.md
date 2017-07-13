# package.json�����ֶν��

package.json��npm����CommonJS�淶�Ķ԰������ļ��Ķ��壬����һЩϸ�ڸı��npm�������ļ���

���£���`*`���ǿ�ѡ�ֶΣ����������ֶΡ�

### name ����

��Сд��ĸ�����ֺ�.-_��ɣ���������ֿո񡣰���������Ψһ�ģ��ҽ��鲻���js��node�ֶ�����ʶ��jsģ�顣

### description * ��������

��ʹ��npm search����ʱ����������ֶΡ�

### version �汾��

���廯�İ汾�ţ�ͨ��Ϊ���汾��.�ΰ汾��.�޶��Ÿ�ʽ��
- ���汾�ţ������˲����ݵ�API�޸�
- �ΰ汾�ţ����������¼��ݵĹ���������
- �޶��ţ����������¼��ݵ�����������

���а汾�ż��汾������Ϣ���Լӵ��汾�ź��棬��Ϊ���졣��1.2.3-release��

### keywords * �ؼ���

�ؼ�����Ϊ������ڣ�����NPM�з�������������׼ȷ�Ĺؼ����趨���������û������ҵ���İ�����ʹ��npm search����ʱ����������ֶΡ�

### maintainers * ��ά�����б�

ÿ��ά������name��email��web����������ɣ��磺

```
"maintainers": [{
    "name": "Zhouboyu",
    "email": "zhouboyu@qq.com",
    "web": "tinper.org"
    }]
```
NPMͨ�������Խ���Ȩ����֤��

### author * ����
������һ���ˡ�

### contributions * �������б�

��Դ��Ŀ�У��������˲���ȱȽϸߣ��Ե�ǰ�����״���Ŀ�����ӽ�����б�һ���һ�������ߣ������ʽ��ά�����б�һ����

### bugs * һ�����Է���bug�ĵ�ַ���ʼ���ַ��

npm bugs�õ��ϡ�

### licenses * ���֤�б�

### repositories * �йܴ����λ���б�

### config * ���ö���

Config�����е�ֵ��Scripts�����������нԿ��ã�ר�����ڸ�Scripts�ṩ���ò�����

### homepage * ��վ��ַ

û��http://�ȴ�Э��ǰ׺��URL��

### engine * ֧�ֵ�Javascript�����б�

### engineStrick *
����ֵ�������϶���ĳ���ֻ�����ƶ���engine�����У�����Ϊtrue��

### Os *
��ָ��ģ�������ʲô����ϵͳ�����У�

"os" : [ "darwin","Linux" ]

"os" : [ "!win32" ]

### CPU *
ָ��CPU�ͺš�

"cpu" : [ "x64","ia32" ]

"cpu" : [ "!arm","!mips" ]

### directories * Ŀ¼˵��

### bin * �������

���ָ�����ǰ���������ģ������������й���ִ�С���ȫ�ְ�װʱ������ȫ�ֵ�����������ذ�װ�������ڱ��ص������

```
"bin": {
"aa": "./bin/aa"
}
```

### mian * ��ڵ�ַ

���û�ʹ��require����ģ��ʱ����������ʹ������ֶΣ���û��û����ֶ�ʱ������Ұ���Ŀ¼�µ�index��.js/.node/.json���ļ���

### scripts * �ű�˵������

npm scripts ��д��package.json��scripts�ֶζ���Ľű����

ʹ��npm run script��ִ�нű���
�ŵ㣺
- ��Ŀ����ؽű������з��ù���
- ��ͬ�Ľű����ֻҪ������ͬ�Ϳ��趨ͬһ����ӿ�
- ��������npm�ĺܶศ�����ܡ�
#### ԭ��
ÿ��ִ��npm run,�ͻᴴ��һ��Shell����Shell��ִ��ָ���Ľű�������ֻҪ��Shell��ִ�е�����Ϳ���д��npm�С�
 ������Shellʱ���Ὣnode_modules/.bin��Ŀ¼����PATH�У�ִ�����ٻָ�PATH������scripts�еĽű��������Ҫ���·��������ֱ��д���
 
```
	 //no
	{
		 "scripts": {
					"test": "./node_modules/.bin/mocha"
		}
    }
	//yes
	 {
		 "scripts": {
					"test": "mocha"
		}
    }
```

npm�ű����˳��룬����Shell�ű���������˳��벻��0��npm����Ϊִ������ű�ʱ����

#### ͨ���
npm����ʹ��Shellͨ������磺
```
"test": "mocha test/*.test.js"
```
�������Ҫ��ԭʼ����ʹ��ͨ�����Ҫʹ��`\`ת�塣

#### ����
npm�ű����Σ�ʹ��`--`��ʶ��
Ҳ�����ٶȷ�װ���
```
"test": "mocha",
"test:lint": "jshint *.js"
```
#### ִ��˳��
`&`����ִ��`&&`˳��ִ�У�������ʹ��script-runner��npm-run-all��redrun���������ģ�顣

#### Ĭ��ֵ
npm�ṩ����Ĭ�Ͻű�
```
"start": "node server.js",
"install": "node-gyp rebuild"
```
��һ����Ҫ��ǰĿ¼����server.js�ļ����ڶ�����Ҫ��ǰĿ¼����binding.gyp�ļ���

#### ����
npm�ű���pre��post�������ӡ�
```
"pretest": "before",
"test": "mocha",
"posttest": "after"
```
ִ��`npm run test`�ᰴ�����ִ��
```
npm run pretest && npm run test && npm run posttest
```
���Կ���ʹ�ù���ִ��һЩ׼�������ϲ�����
Ĭ���ṩ�Ĺ��ӣ�
- publish
- install
- uninstall
- version
- test
- stop
- start
- restart
�Զ��������Ҳ�������pre��post���ӣ�����˫�ص�prepre��postpost��Ч
npm���ṩһ��npm_lifecycle_event���������ص�ǰִ�нű������ƣ����Կ������������������һ���ű��ļ��ڣ�Ϊ��ͬ��scripts�����д���롣��
```javascript
const TARGET = process.env.npm_lifecycle_event;
if (TARGET === "test") {
	console.log('run test');
}

if (TARGET === "pretest") {
	console.log('run pretest');
}

if (TARGET === "posttest") {
	console.log('run posttest');
}
```

#### ��д��ʽ
- npm start
- npm test
- npm start
- npm restart ����ִ���������� npm run stop && npm run restart && npm run start ��
ִ��˳��Ϊ
prerestart > prestop > stop > poststop > restart > prestart > start > poststart > postrestart 

#### ����
npm�ű���һ���ǳ�ǿ��ù��ܣ�����ʹ��npm�ڲ�����

���ȣ�ͨ��npm_packageǰ׺���Ի�ȡ��package.json������ֶΡ�
```
//js�ű���
var name = process.env.npm_package_name;

//shell�ű�
$npm_package_name
```
ʹ��npm_config�����õ�npm�����ñ�������npm_config_tag�õ�������ǩ��package.json��config�ı����ᱻ�����������ǡ�
```
"name": "foo",
"config": {"port": "8080"}
```
�ᱻ
```
npm config set foo:port 80
```
evn������г����л�������
```
"env": "env"
```

### dependencies * �����б�

��ǰ��ʹ�����������б�ʹ��npm install --save ����Ӱ���������б�

#### �汾��ʽ

- version ��ȫƥ��
- `>version` ��������汾
- `>=version`���ڻ��������汾
- <version
- <=version
- ~version �ǳ��ӽ�����汾
- ^version �뵱ǰ�汾����
- 1.2.x X�����������֣����1.2.1, 1.2.3�ȶ�����
- http://... Unixϵͳ��ʹ�õ�tarball��URL��
- `*` �κΰ汾������
- ""�κΰ汾������
- version1 - version2  �ȼ��� >=version1 <=version2.
- range1 || range2 ��������һ������
- git... Git��ַ
- user/repo

### devDependencies * ���������б�

�ڿ�����ʱ�����İ��б�ʹ��npm install --save-dev ����Ӱ���������б�

### peerDependencies *

�����������������İ��ǲ�����ʺ����ַ�ʽ��

### bundledDependencies *

��������ʱͬʱ���������������

### optionalDependencies *

���������ĳЩ������ʹû���ҵ�������װʧ�ܵ�����£�npm������ִ�С���ô��Щ�����ʺϷ������

#### �ο�
[http://semver.org](http://semver.org)