# ʹ��editorconfig������ı༭��
���ճ������У��������л���ͬ�༭������Ҫ����һ������á�
�Ŷӿ�����ÿ����ʹ�ò�ͬ�ı༭����Ҫ��һ�������÷Ѿ����ࡣ
������ڷ�����Щ��.editorconfig����Ϊ���������ͨ������Ŀ��Ŀ¼�����.editorconfig�ļ�������һ�����򣬾Ϳ������ò�ͬ�༭������һ�´���淶��

### ���ý���

##### charset �ļ�����

- һ��ʹ��utf-8,��ѡ��latin1, utf-16be,utf-16le��

##### indent_style ��������
- space �ո�
- tab �Ʊ��

##### indent_size ��������
- ������һ��2��4
- tab

##### tab_width tab����
- ����

##### insert_final_newline �Ƿ����ļ�������һ������
- true
- false

##### end_of_line ���з���ʽ
- lf (����,*nuxϵͳ)
- crlf(windows)
- cr(<=MacOS9)

##### trim_trailing_whitespace �Ƿ�ɾ����β�ո�
- true
- false

##### max_line_length ������ַ���
�����Զ����У���֧��atom�������༭��
- ����

�����������Բ鿴[github/editorconfig/](https://github.com/editorconfig/editorconfig/wiki/EditorConfig-Properties)

### ʾ��

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

