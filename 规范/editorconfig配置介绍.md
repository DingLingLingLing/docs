# 使用editorconfig配置你的编辑器
在日常开发中，经常会切换不同编辑器，总要设置一遍的配置。
团队开发，每个人使用不同的编辑器。要求一样的配置费尽口舌。
如果你在烦恼这些，.editorconfig将成为你的银弹。通过在项目根目录中添加.editorconfig文件并配置一定规则，就可以设置不同编辑器保持一致代码规范。

### 配置介绍

##### charset 文件编码

- 一般使用utf-8,可选（latin1, utf-16be,utf-16le）

##### indent_style 缩进类型
- space 空格
- tab 制表符

##### indent_size 缩进数量
- 整数，一般2或4
- tab

##### tab_width tab长度
- 整数

##### insert_final_newline 是否在文件最后插入一个空行
- true
- false

##### end_of_line 换行符格式
- lf (常用,*nux系统)
- crlf(windows)
- cr(<=MacOS9)

##### trim_trailing_whitespace 是否删除行尾空格
- true
- false

##### max_line_length 行最大字符数
超过自动换行，仅支持atom等少数编辑器
- 整数

其它更多属性查看[github/editorconfig/](https://github.com/editorconfig/editorconfig/wiki/EditorConfig-Properties)

### 示例

```
# editorconfig.org

root = true

[*]
charset = utf-8
indent_size = 4
indent_style = space
insert_final_newline = true
trim_trailing_whitespace = true

[*.md]
trim_trailing_whitespace = false
```

