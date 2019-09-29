# 2019.9.21开始第一次python汇总 
## 预计持续更新至2021年研究生毕业

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

## lower() & upper()
lower()方法将字符串中所有的大写变味小写；upper（）相反

## abs（）
求取绝对值

## random（）
```python
import random

print( random.randint(1,10) )        # 产生 1 到 10 的一个整数型随机数  
print( random.random() )             # 产生 0 到 1 之间的随机浮点数
print( random.uniform(1.1,5.4) )     # 产生  1.1 到 5.4 之间的随机浮点数，区间可以不是整数
print( random.choice('tomorrow') )   # 从序列中随机选取一个元素
print( random.randrange(1,100,2) )   # 生成从1到100的间隔为2的随机整数

a=[1,3,5,6,7]                # 将序列a中的元素顺序打乱
random.shuffle(a)
print(a)
```

## dir（）
当有参数时，以列表方式返回当前参数的属性和方法
### Input
```python
dir([])    #查看列表的属性和方法
```
### Output
```
['__add__', '__class__', '__contains__', '__delattr__', '__delitem__', '__delslice__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__getslice__', '__gt__', '__hash__', '__iadd__', '__imul__', '__init__', '__iter__', '__le__', '__len__', '__lt__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__reversed__', '__rmul__', '__setattr__', '__setitem__', '__setslice__', '__sizeof__', '__str__', '__subclasshook__', 'append', 'count', 'extend', 'index', 'insert', 'pop', 'remove', 'reverse', 'sort']
```

