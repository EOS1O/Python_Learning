
<div align="center">
  <a href="https://eosdota.xyz">
    <img src="https://i.loli.net/2019/10/23/iU9OX5LN1kZMSGm.png"  width="150" height="180">
  </a>
</div>

# <p align="center">Python</p>
### <p align="center">记录日常所学所惑所得</p>

|W3school|菜鸟|莫烦|V2EX|CheckiO|Django|Pandas|Github|Leetcode|Machine Learning
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-: 
|[💻](https://www.w3schools.com/python/default.asp)|[🎨](https://www.runoob.com/python/python-tutorial.html)|[☕️](https://morvanzhou.github.io/)|[📝](https://www.v2ex.com/)|[💡](https://py.checkio.org/)|[💾](https://www.djangoproject.com/)|[✏️](https://jvns.ca/blog/2013/12/22/cooking-with-pandas/)|[🍉](https://github.com/CodementorIO/Python-Learning-Resources)|[📚](https://leetcode-cn.com/)|[☁️](https://github.com/hangtwenty/dive-into-machine-learning) 

</br></br>
### [♪ 函数](#函数)　　　　　　　　　[♭ 方法](#方法)　　　　　　　　[♭ 实例](#实例)
</br></br>
# 函数
[⋌ print](#print函数)　　　[⋌ Random](#Random函数)　　　[⋌ range](#range函数)　　　[⋌ set](#set函数)　　　[⋌ abs](#abs函数)　　　[⋌ dir](#dir函数)　　　[⋌ map](#map函数)　　　

## print函数
%d  整数           %s 字符串
```python
print("I love %s" %Passion)
I love Passion

print("I own %d Apples" %100)
I own 100 Apples
```

## random()函数
```python
import random

print( random.randint(1,10) )                               # 产生 1 到 10 的一个整数型随机数  
print( random.random() )                                    # 产生 0 到 1 之间的随机浮点数
print( random.uniform(1.1,5.4) )                            # 产生  1.1 到 5.4 之间的随机浮点数，区间可以不是整数
print( random.choice('tomorrow') )                          # 从序列中随机选取一个元素
print( random.randrange(1,100,2) )                          # 生成从1到100的间隔为2的随机整数

a=[1,3,5,6,7]                                               # 将序列a中的元素顺序打乱
random.shuffle(a)
print(a)
```

## range()函数
· range(start, stop, step)
+ start: 开始位置，默认为 0 </br></br>
+ stop: 结束位置，输出时不包括 </br></br>
+ step: 间隔，默认为1 </br></br>
```python
range(10)                                                     #产生 0-9 间所有的整数
range(1,10,2)                                                 #输出 [1,3,5,7,9]
range(10,-10,-1)                                              #输出[10,-10)间所有的整数

for i in range(6, -1, -1):                                    #逆向输出
    new.append(i)
print(new)                                                    #Output: [6, 5, 4, 3, 2, 1, 0]

```
## set()函数
set() 函数创建一个无序不重复元素集，可进行关系测试，删除重复数据，还可以计算交集、差集、并集等
```python
#判断列表中是否存在重复元素
a = [1, 2, 3, 4, 5, 6, 6]
b = a.set()
if len(a) > len(b):                                           #len(a) = 7  len(b) = 6
  print("Yeah")                                               #Output: Yeah
```

## abs()函数
求取绝对值

## dir（）函数
当有参数时，以列表方式返回当前参数的属性和方法
#### Input
```python
dir([])    #查看列表的属性和方法
```
#### Output
```
['__add__', '__class__', '__contains__', '__delattr__', '__delitem__', '__delslice__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__getslice__', '__gt__', '__hash__', '__iadd__', '__imul__', '__init__', '__iter__', '__le__', '__len__', '__lt__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__reversed__', '__rmul__', '__setattr__', '__setitem__', '__setslice__', '__sizeof__', '__str__', '__subclasshook__', 'append', 'count', 'extend', 'index', 'insert', 'pop', 'remove', 'reverse', 'sort']
```

## map()函数
map(function, iterable, ...)   对迭代对象iterable object逐个使用function (注意，此处function不加（）)
```python
a = map(int,['1','2','68'])                                     #对['1','2','68']中每个元素使用int()函数，此处int不带()
print（a）                                                      #Output：[1, 2, 68]
```
</br></br>

# 方法
[⋌ split](#split方法)　　　[⋌ istitle](#istitle方法)　　　[⋌ lower & upper](#lower & upper)　　　[⋌ strip](#strip方法)　　　[⋌ continue](#continue)　　　
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
## istitle()方法
istitle()方法检测字符串中所有的单词拼写首字母是否为大写，且其他字母为小写

## lower() & upper()
lower()方法将字符串中所有的大写变味小写；upper（）相反

## pow()方法
pow() 方法返回x的y次方
```python
import math
pow(x,y)                                                      #返回x的y次方
```

## strip()方法
strip() 方法用于移除字符串头尾（只能是首尾）指定的字符（默认为空格或换行符）或字符序列
```python
a = str(123456)
print(a.strip('12'))                                            #Output: 3456   (type是str)
print(a.strip(12))                                              #Output: 123456
print(a.strip('34'))                                            #Output: 123456
```

## continue（）
continue 语句用来告诉Python跳过当前循环的剩余语句，然后继续进行下一轮循环 </br></br>
ps：continue 语句跳出本次循环，而break跳出整个循环
```python
n = 0
while n < 10:
    n = n + 1
    if n % 2 == 0:                                            # 如果n是偶数，执行continue语句
        continue                                              # continue语句会直接继续下一轮循环，后续的print()语句不会执行
    print(n)
```

</br></br>
# 实例
[⋌ 反转技术](#反转技术)　　　[⋌ 切片](#切片技术)　　　[⋌ 进制间转换](#进制间转换)　　　[⋌ 整数分离](#整数分离)　　　[⋌ 字符类型判断](#字符类型判断)　　　
## 反转技术
#### List反转
```python
# 法1：使用reverse()方法
a = [1,2,3,4,5]
a.reverse()                                                   #a列表本身被更改了
print(a)                                                      #Output:  [5,4,3,2,1]  

# 法2：使用分片
a = [1,2,3,4,5]                                               #a列表本身未被改变
b = a[::-1]                                                   #从后向前找，步长为1
print(b)                                                      #Output： [5,4,3,2,1]
``` 
#### 字典反转
```python
a = {a:1, b:2, c:3}
a.items()                                                     #Output: dict_items([('a', '1'), ('b', '2'),('c','3')])

for k,v in a.items:                                           #Output: a  1
    print(k,v)                                                b  2
                                                              c  3
b = {v:k for k,v in a.items()}          
print(b)                                                      #output： [1:a,2:b,3:c]
```

## 切片技术
切片是list索引的一项重要功能 </br></br>
· list = [0, 1, 2, 3, 4, 5, 6, 7, 8] </br></br>
　正向顺序：  0　１　２　３　４　５　６　７　８　９ </br></br>
　逆向顺序：　－９　－８　－７　－６　－５　－４　－３　－２　－１

· list[start_index:stop_index:step]
+ start_index:开始位置，可为负
+ stop_index:结束位置,此位不取
+ step：步长，默认为 1

```python
a = [0, 1, 2, 3, 4, 5, 6, 7, 8]
print(a[::])                                                  #输出a
print(a[::-1])                                                #逆向输出 [8, 7, 6, 5, 4, 3, 2, 1]
print(a[::2])                                                 #隔位取数 [0, 2, 4, 6, 8]
print(a[-8:6])                                                #Output: [1, 2, 3, 4, 5]
```

## 进制间转换
- 二进制　　　0b101　－以数字0和字母开头，如果出现大于等于2的数，会抛出SyntaxError异常 
- 八进制　　　0711　 －以数字0打头的数字，如果出现大于等于8的数，会抛出SyntaxError异常
- 十六进制　　0x15　 －以数字0和字符x开头，包括0-9和abcdef或ABCDEF，出现其他数值会抛出SyntaxError异常
```python
#10进制转2进制
bin(a)                                                         #a为10进制整数
#2进制转10进制
int("1011",2)

#10进制转8进制（3种）
print("%o" % 10)                                               #Output: 12
print('0' * 0 + f'{int(10):o}')                                #Output: 12
print(oct(10))                                                 #Output: 0o12

#10进制转16进制
hex(10)                                                        #Output：0xa
```

## 整数分离
将一个整数的每一位单独分离开来  例：12345678 → 1，2，3，4，5，6，7
```python
a = str(12345678)
list(map(int,a))                                                #Output:[1, 2, 3, 4, 5, 6, 7, 8]
```

## 字符类型判断
```python
.isalpha()                                                      #判断是否为字母
.isdigit()                                                      #判断是否为数字
.isspace()                                                      #判断是否为空格

#判断是否为标点符号
import String                                                   
punc = string.punctuation
if i == '_':
```
