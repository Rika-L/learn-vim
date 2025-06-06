# 替换字符串

替换命令 :substitute

公式 `:[range]s[ubstitue]/{pattern}/{string}/{flags}`

range 范围
* $ 到尾部
* % 全文
* number,number 基于行替换

pattern 要替换的 可以写正则

string 替换成什么

flag
* g 全文匹配 即 global
* c 弹出对话框询问是否替换

多选 gb 类似于 ctrl + v 的可视化模式

```
vnode vnode

Vnode vnode Vnode xxx
```