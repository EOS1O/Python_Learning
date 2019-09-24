# 2019.9.21开始第一次python汇总 
# 预计持续更新至2021年研究生毕业

## print用法
%d  整数           %s 字符串
```python
print("I love %s" %Passion)
I love Passion

print("I own %d Apples" %100)
I own 100 Apples
```
## split()方法
split()通过指定分隔符对字符串进行切片，如果参数num 有指定值，则仅分隔 num 个子字符串；若str为空，则切割space
```
str.split(str="", num=string.count(str)
```
#### Input
```
str = "this is string example....wow!!!"
print (str.split( ))
print (str.split('i',1))
print (str.split('w'))
```
#### Output
```
['this', 'is', 'string', 'example....wow!!!']
['th', 's is string example....wow!!!']
['this is string example....', 'o', '!!!']
```
## istitle()
istitle()方法检测字符串中所有的单词拼写首字母是否为大写，且其他字母为小写


