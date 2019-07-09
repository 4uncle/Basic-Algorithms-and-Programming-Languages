#                       Python入门学习
<!-- TOC -->  
[Python入门学习](#python入门学习)  
[1.python在sublime 中执行](#1python在sublime-中执行)  
[2.在打印字符串时一定要加上单引号或者双引号，单引号换行不会保留格式，三引号才会保留格式](#2在打印字符串时一定要加上单引号或者双引号单引号换行不会保留格式三引号才会保留格式)  
[3.python中的字符串拼接的几种方式](#3python中的字符串拼接的几种方式)  
[4.python类型检测](#4python类型检测)  
[5.对象就是存储数据结构的一个容器，OOP编程中一切皆对象](#5对象就是存储数据结构的一个容器oop编程中一切皆对象)  
[6.关于对象的内存解释](#6关于对象的内存解释)  
[7.算术运算](#7算术运算)  
[8.赋值运算](#8赋值运算)  
[9.关系运算](#9关系运算)  
[10.逻辑运算](#10逻辑运算)  
[11.条件运算](#11条件运算)  
[12.关于代码块的缩进](#12关于代码块的缩进)  
[13.while循环使用方法](#13while循环使用方法)  
[14.在print中如果加入end=‘’，则输入不会换行](#14在print中如果加入end则输入不会换行)  
[15.关于切片概念](#15关于切片概念)  
[16.list的通用操作](#16list的通用操作)  
[17.for循环使用](#17for循环使用)  
[18.range的作用](#18range的作用)  
[19.关于 ==          !=         is            is not](#19关于--------------------is------------is-not)  
[20.关于python中的字典](#20关于python中的字典)  
[21.关于集合的用法](#21关于集合的用法)  
[22.元组及其解包运算](#22元组及其解包运算)  
[23.python中输入](#23python中输入)  
[24.函数的具体操作](#24函数的具体操作)  
[25.关于不定长参数传递](#25关于不定长参数传递)  
[26.关于函数和函数对象的区别](#26关于函数和函数对象的区别)  
[27.python中使用global对全局变量赋值](#27python中使用global对全局变量赋值)  
[28.高阶函数操作以及lambda函数](#28高阶函数操作以及lambda函数)  
[29.关于python的闭包处理](#29关于python的闭包处理)  
[30.python中类的初始化以及操作](#30python中类的初始化以及操作)  
[31.封装](#31封装)  
[31.2.使用装饰器](#312使用装饰器)  
[32.继承](#32继承)  
[33.多重继承](#33多重继承)  
[34.多态](#34多态)  
[35.类中方法](#35类中方法)  
[36.垃圾回收](#36垃圾回收)  
[37.模块的使用](#37模块的使用)  
[38.异常处理](#38异常处理)  
[39.文件操作](#39文件操作)  
[40.文件写入操作](#40文件写入操作)  
[41.文件读取模式](#41文件读取模式)  
[42.文件读取位置](#42文件读取位置)  
[43.python编写时注意指定文件编码格式](#43python编写时注意指定文件编码格式)  
<!-- /TOC -->
#### 1.python在sublime 中执行

ctrl+b即可执行sublime中的代码

#### 2.在打印字符串时一定要加上单引号或者双引号，单引号换行不会保留格式，三引号才会保留格式

```python
a = 'hello world'
#单引号无法换行
a = '''hello\
world'''
result:
hello world
helloworld
```

#### 3.python中的字符串拼接的几种方式

```python
name='孙悟空'

print('欢迎'+name+'光临')
print('欢迎',name,'光临')
print('欢迎%s光临'%name)
print(f'欢迎{name}光临')

result:
欢迎孙悟空光临
欢迎 孙悟空 光临
欢迎孙悟空光临
欢迎孙悟空光临
```

#### 4.python类型检测

```python
a = 10
b = 2.3
c = '123'
print(type(a))
print(type(b))
print(type(c))

result:
<class 'int'>
<class 'float'>
<class 'str'>
```

#### 5.对象就是存储数据结构的一个容器，OOP编程中一切皆对象

#### 6.关于对象的内存解释

```python
a = 123
#在内存中解释始终是自右向左的，所以先在内存中创建一个123的对象(若地址0x1)，然后将123在内存中的地址赋
#值给a
b = a
#此时b的值和a是相等的，因为b中存放的是123的内存地址(0x1)
a = 456
#当a的值发生改变，b的值并不会受到影响，因为内存中先解释456，重新创建一个对象并分配一个内存地址
#(若地址为0x2)，此时a = 0x2,b = 0x1 因此b的值不会因为a的改变而改变。
#类型转换同理，他是把新的值重新在内存中创建一个对象
a = 11.5
a = int(a)
print(a)

result :
11

```

#### 7.算术运算

```python
# 算术运算符
# + 加法运算符（如果是两个字符串之间进行加法运算，则会进行拼串操作）
# - 减法运算符
# * 乘法运算符（如果将字符串和数字相乘，则会对字符串进行复制操作，将字符串重复指定次数）
# / 除法运算符，运算时结果总会返回一个浮点类型
# // 整除，只会保留计算后的整数位，总会返回一个整型
# ** 幂运算，求一个值的几次幂
# % 取模，求两个数相除的余数

```

#### 8.赋值运算

```python
# 赋值运算符
# = 可以将等号右侧的值赋值给等号左侧的变量
# +=  a += 5 相当于 a = a + 5 
# -=  a -= 5 相当于 a = a - 5 
# *=  a *= 5 相当于 a = a * 5 
# **= a **= 5 相当于 a = a ** 5 
# /=  a /= 5 相当于 a = a / 5 
# //= a //= 5 相当于 a = a // 5 
# %=  a %= 5 相当于 a = a % 5 

```

#### 9.关系运算

```python
# 关系运算符
# 关系运算符用来比较两个值之间的关系，总会返回一个布尔值
# 如果关系成立，返回True，否则返回False
# > 比较左侧值是否大于右侧值
# >= 比较左侧的值是否大于或等于右侧的值
# < 比较左侧值是否小于右侧值
# <= 比较左侧的值是否小于或等于右侧的值
# == 比较两个对象的值是否相等
# != 比较两个对象的值是否不相等
#   相等和不等比较的是对象的值，而不是id
# is 比较两个对象是否是同一个对象，比较的是对象的id
# is not 比较两个对象是否不是同一个对象，比较的是对象的id
```

#### 10.逻辑运算

```python
# 逻辑运算符
# 逻辑运算符主要用来做一些逻辑判断
# not 逻辑非
#   not可以对符号右侧的值进行非运算
#       对于布尔值，非运算会对其进行取反操作，True变False，False变True
#       对于非布尔值，非运算会先将其转换为布尔值，然后再取反
#       
# and 逻辑与
#   and可以对符号两侧的值进行与运算
#    只有在符号两侧的值都为True时，才会返回True，只要有一个False就返回False
#    与运算是找False的
#    Python中的与运算是短路的与，如果第一个值为False，则不再看第二个值
#   
# or 逻辑或
#   or 可以对符号两侧的值进行或运算
#    或运算两个值中只要有一个True，就会返回True
#    或运算是找True的
#    Python中的或运算是短路的或，如果第一个值为True，则不再看第二个值
```

#### 11.条件运算

```python
# 条件运算符（三元运算符）
# 语法： 语句1 if 条件表达式 else 语句2
# 执行流程：
#   条件运算符在执行时，会先对条件表达式进行求值判断
#       如果判断结果为True，则执行语句1，并返回执行结果
#       如果判断结果为False，则执行语句2，并返回执行结果

# print('你好') if False else print('Hello')
```

#### 12.关于代码块的缩进

```python
if True:
    #这里是四个空格缩进,也可以使用tab
    
```



#### 13.while循环使用方法

```python
while [表达式]:
	[代码块]
#python中++ -- 不可用，只能+1 -1
```

#### 14.在print中如果加入end=‘’，则输入不会换行

```python
print('*',end='')
print('*',end='')
result:
**

print('*')
print('*')
result:
*
*
```

#### 15.关于切片概念

```python
#切片是获取一个list中的局部元素
my_List = [10,20,30]
print(my_List[0:2])
#切片格式为 列表名[起始元素，结束元素]
pirnt(my_List[0:2:2])
#还可以添加一个冒号后跟阅读步长

result:
[10, 20]
[10, 30]
```

#### 16.list的通用操作

```python
# in 和 not in
# in用来检查指定元素是否存在于列表中
#   如果存在，返回True，否则返回False
# not in用来检查指定元素是否不在列表中
#   如果不在，返回True，否则返回False
# len()获取列表中的元素的个数
# min() 获取列表中的最小值
# max() 获取列表中的最大值
# 两个方法（method），方法和函数基本上是一样，只不过方法必须通过 对象.方法() 的形式调用
# xxx.print() 方法实际上就是和对象关系紧密的函数
# s.index() 获取指定元素在列表中的第一次出现时索引
# print(stus.index('沙和尚'))
# index()的第二个参数，表示查找的起始位置 ， 第三个参数，表示查找的结束位置
# print(stus.index('沙和尚',3,7))
# 如果要获取列表中没有的元素，会抛出异常
# print(stus.index('牛魔王')) ValueError: '牛魔王' is not in list
# s.count() 统计指定元素在列表中出现的次数
```

#### 17.for循环使用

```python
my_List = [10,20,30,40]
for num in my_List :
	print(num)
# for 变量 in 序列 ：
#	代码块
#注意点 序列后要空格加冒号，代码块需要缩进

result:
10
20
30
40

```

#### 18.range的作用

```python
# range()是一个函数，可以用来生成一个自然数的序列
r = range(5) # 生成一个这样的序列[0,1,2,3,4]
r = range(0,10,2)
r = range(10,0,-1)
# 该函数需要三个参数
#   1.起始位置（可以省略，默认是0）
#   2.结束位置
#   3.步长（可以省略，默认是1）
# print(list(r))
# 通过range()可以创建一个执行指定次数的for循环
# for()循环除了创建方式以外，其余的都和while一样，
#   包括else、包括break continue都可以在for循环中使用
#   并且for循环使用也更加简单
# 将之前使用while循环做的练习，再使用for循环完成一次！
```

#### 19.关于 ==          !=         is            is not

```python
#==和!=是为了判断两个对象的值是否相等
#is  is not 判断两个对象是否为同一个在内存中的地址

```

#### 20.关于python中的字典

```python
#python中字典用关键字dict命名，就是键值对的形式，就是java中的Map，使用方法大同小异
d = {'name' : 'lulele',age : 22}
#第一种初始化方式
d = dict(name = 'lulele',age = 21)
#第二中初始化方式

result:
{'name': 'lulele', 'age': 22}
{'name': 'lulele', 'age': 21}

# 也可以将一个包含有双值子序列的序列转换为字典
# 双值序列，序列中只有两个值，[1,2] ('a',3) 'ab'
# 子序列，如果序列中的元素也是序列，那么我们就称这个元素为子序列
# [(1,2),(3,5)]
d = dict([('name','孙悟饭'),('age',18)])
# print(d , type(d))
d = dict(name='孙悟空',age=18,gender='男') 

# len() 获取字典中键值对的个数
# print(len(d))

# in 检查字典中是否包含指定的键
# not in 检查字典中是否不包含指定的键
# print('hello' in d)

# 获取字典中的值，根据键来获取值
# 语法：d[key]
# print(d['age'])

# n = 'name'
# print(d[n])

# 通过[]来获取值时，如果键不存在，会抛出异常 KeyError
# get(key[, default]) 该方法用来根据键来获取字典中的值
#   如果获取的键在字典中不存在，会返回None
#   也可以指定一个默认值，来作为第二个参数，这样获取不到值时将会返回默认值
# print(d.get('name'))
# print(d.get('hello','默认值'))

# 修改字典
# d[key] = value 如果key存在则覆盖，不存在则添加
d['name'] = 'sunwukong' # 修改字典的key-value
d['address'] = '花果山' # 向字典中添加key-value

# print(d)
# setdefault(key[, default]) 可以用来向字典中添加key-value
#   如果key已经存在于字典中，则返回key的值，不会对字典做任何操作
#   如果key不存在，则向字典中添加这个key，并设置value
result = d.setdefault('name','猪八戒')
result = d.setdefault('hello','猪八戒')

# print('result =',result)
# print(d)

# update([other])
# 将其他的字典中的key-value添加到当前字典中
# 如果有重复的key，则后边的会替换到当前的
d = {'a':1,'b':2,'c':3}
d2 = {'d':4,'e':5,'f':6, 'a':7}
d.update(d2)

# print(d)
# 删除，可以使用 del 来删除字典中的 key-value
del d['a']
del d['b']

# popitem()
# 随机删除字典中的一个键值对，一般都会删除最后一个键值对
#   删除之后，它会将删除的key-value作为返回值返回
#   返回的是一个元组，元组中有两个元素，第一个元素是删除的key，第二个是删除的value
# 当使用popitem()删除一个空字典时，会抛出异常 KeyError: 'popitem(): dictionary is empty'
# d.popitem()
# result = d.popitem()

# pop(key[, default])
# 根据key删除字典中的key-value
# 会将被删除的value返回！
# 如果删除不存在的key，会抛出异常
#   如果指定了默认值，再删除不存在的key时，不会报错，而是直接返回默认值
result = d.pop('d')
result = d.pop('z','这是默认值')

# del d['z'] z不存在，报错
# result = d.popitem()
# result = d.popitem()
# result = d.popitem()
# result = d.popitem()

# clear()用来清空字典
d.clear()

# print('result =',result)
# print(d)

# copy()
# 该方法用于对字典进行浅复制
# 复制以后的对象，和原对象是独立，修改一个不会影响另一个
# 注意，浅复制会简单复制对象内部的值，如果值也是一个可变对象，这个可变对象不会被复制
d = {'a':1,'b':2,'c':3}
d2 = d.copy()
# d['a'] = 100

d = {'a':{'name':'孙悟空','age':18},'b':2,'c':3}
d2 = d.copy()
d2['a']['name'] = '猪八戒'


print('d = ',d , id(d))
print('d2 = ',d2 , id(d2))
```

#### 21.关于集合的用法

```python
# 集合
# 使用 {} 来创建集合
s = {10,3,5,1,2,1,2,3,1,1,1,1} # <class 'set'>
# s = {[1,2,3],[4,6,7]} TypeError: unhashable type: 'list'
# 使用 set() 函数来创建集合
s = set() # 空集合
# 可以通过set()来将序列和字典转换为集合
s = set([1,2,3,4,5,1,1,2,3,4,5])
s = set('hello')
s = set({'a':1,'b':2,'c':3}) # 使用set()将字典转换为集合时，只会包含字典中的键

# 创建集合
s = {'a' , 'b' , 1 , 2 , 3 , 1}

# 使用in和not in来检查集合中的元素
# print('c' in s)

# 使用len()来获取集合中元素的数量
# print(len(s))

# add() 向集合中添加元素
s.add(10)
s.add(30)

# update() 将一个集合中的元素添加到当前集合中
#   update()可以传递序列或字典作为参数，字典只会使用键
s2 = set('hello')
s.update(s2)
s.update((10,20,30,40,50))
s.update({10:'ab',20:'bc',100:'cd',1000:'ef'})

# {1, 2, 3, 100, 40, 'o', 10, 1000, 'a', 'h', 'b', 'l', 20, 50, 'e', 30}
# pop()随机删除并返回一个集合中的元素
# result = s.pop()

# remove()删除集合中的指定元素
s.remove(100)
s.remove(1000)

# clear()清空集合
s.clear()

# copy()对集合进行浅复制

# print(result)
print(s , type(s))
```

集合的运算

```python
# 在对集合做运算时，不会影响原来的集合，而是返回一个运算结果
# 创建两个集合
s = {1,2,3,4,5}
s2 = {3,4,5,6,7}

# & 交集运算
result = s & s2 # {3, 4, 5}

# | 并集运算
result = s | s2 # {1,2,3,4,5,6,7}

# - 差集
result = s - s2 # {1, 2}

# ^ 异或集 获取只在一个集合中出现的元素
result = s ^ s2 # {1, 2, 6, 7}

# <= 检查一个集合是否是另一个集合的子集
# 如果a集合中的元素全部都在b集合中出现，那么a集合就是b集合的子集，b集合是a集合超集
a = {1,2,3}
b = {1,2,3,4,5}

result = a <= b # True
result = {1,2,3} <= {1,2,3} # True
result = {1,2,3,4,5} <= {1,2,3} # False

# < 检查一个集合是否是另一个集合的真子集
# 如果超集b中含有子集a中所有元素，并且b中还有a中没有的元素，则b就是a的真超集，a是b的真子集
result = {1,2,3} < {1,2,3} # False
result = {1,2,3} < {1,2,3,4,5} # True

# >= 检查一个集合是否是另一个的超集
# > 检查一个集合是否是另一个的真超集
print('result =',result)
```

#### 22.元组及其解包运算

```python
# 元组 tuple
# 元组是一个不可变的序列
# 它的操作的方式基本上和列表是一致的
# 所以你在操作元组时，就把元组当成是一个不可变的列表就ok了
# 一般当我们希望数据不改变时，就使用元组，其余情况都使用列表

# 创建元组
# 使用()来创建元组
my_tuple = () # 创建了一个空元组
# print(my_tuple,type(my_tuple)) # <class 'tuple'>

my_tuple = (1,2,3,4,5) # 创建了一个5个元素的元组
# 元组是不可变对象，不能尝试为元组中的元素重新赋值
# my_tuple[3] = 10 TypeError: 'tuple' object does not support item assignment
# print(my_tuple[3])

# 当元组不是空元组时，括号可以省略
# 如果元组不是空元组，它里边至少要有一个,
my_tuple = 10,20,30,40
my_tuple = 40,
# print(my_tuple , type(my_tuple))

my_tuple = 10 , 20 , 30 , 40

# 元组的解包（解构）
# 解包指就是将元组当中每一个元素都赋值给一个变量
a,b,c,d = my_tuple

# print("a =",a)
# print("b =",b)
# print("c =",c)
# print("d =",d)

a = 100
b = 300
# print(a , b)

# 交互a 和 b的值，这时我们就可以利用元组的解包
a , b = b , a

# print(a , b)
my_tuple = 10 , 20 , 30 , 40


# 在对一个元组进行解包时，变量的数量必须和元组中的元素的数量一致
# 也可以在变量前边添加一个*，这样变量将会获取元组中所有剩余的元素
a , b , *c = my_tuple
a , *b , c = my_tuple
*a , b , c = my_tuple
a , b , *c = [1,2,3,4,5,6,7]
a , b , *c = 'hello world'
# 不能同时出现两个或以上的*变量
# *a , *b , c = my_tuple SyntaxError: two starred expressions in assignment
print('a =',a)
print('b =',b)
print('c =',c)
```

#### 23.python中输入

```python
input()
#通过input监听键盘输入的数据
```

#### 24.函数的具体操作

```python
# 求任意三个数的乘积
def mul(a,b,c):
    print(a*b*c)

# 根据不同的用户名显示不同的欢迎信息   
def welcome(username):
    print('欢迎',username,'光临')

# mul(1,2,3)   
# welcome('孙悟空') 

# 定义一个函数
# 定义形参时，可以为形参指定默认值
# 指定了默认值以后，如果用户传递了参数则默认值没有任何作用
#   如果用户没有传递，则默认值就会生效
def fn(a = 5 , b = 10 , c = 20):
    print('a =',a)
    print('b =',b)
    print('c =',c)

# fn(1 , 2 , 3)
# fn(1 , 2)
# fn()

# 实参的传递方式
# 位置参数
# 位置参数就是将对应位置的实参复制给对应位置的形参
# 第一个实参赋值给第一个形参，第二个实参赋值给第二个形参 。。。
# fn(1 , 2 , 3)

# 关键字参数
# 关键字参数，可以不按照形参定义的顺序去传递，而直接根据参数名去传递参数
# fn(b=1 , c=2 , a=3)
# print('hello' , end='')
# 位置参数和关键字参数可以混合使用
# 混合使用关键字和位置参数时，必须将位置参数写到前面
# fn(1,c=30)

def fn2(a):
    print('a =',a)

# 函数在调用时，解析器不会检查实参的类型
# 实参可以传递任意类型的对象
b = 123
b = True
b = 'hello'
b = None
b = [1,2,3]

# fn2(b)    
fn2(fn)

def fn3(a , b):
    print(a+b)

# fn3(123,"456")

def fn4(a):
    # 在函数中对形参进行重新赋值，不会影响其他的变量
    # a = 20
    # a是一个列表，尝试修改列表中的元素
    # 如果形参执行的是一个对象，当我们通过形参去修改对象时
    #   会影响到所有指向该对象的变量
    a[0] = 30
    print('a =',a,id(a))

c = 10   
c = [1,2,3] 

# fn4(c)
# fn4(c.copy())
# fn4(c[:])

# print('c =',c,id(c))
```

#### 25.关于不定长参数传递

```python
def sum(*n):
#传递不定长参数时要在该参数前加*
	result = 0
    for x in n:
        result+=x
    

```

26.关于函数参数传递的解包操作

```python
# 不定长的参数
# 定义一个函数，可以求任意个数字的和
def sum(*nums):
    # 定义一个变量，来保存结果
    result = 0
    # 遍历元组，并将元组中的数进行累加
    for n in nums :
        result += n
    print(result)


# sum(123,456,789,10,20,30,40)

# 在定义函数时，可以在形参前边加上一个*，这样这个形参将会获取到所有的实参
# 它将会将所有的实参保存到一个元组中
# a,b,*c = (1,2,3,4,5,6)

# *a会接受所有的位置实参，并且会将这些实参统一保存到一个元组中（装包）
def fn(*a):
    print("a =",a,type(a))

# fn(1,2,3,4,5)
# 带星号的形参只能有一个
# 带星号的参数，可以和其他参数配合使用
# 第一个参数给a，第二个参数给b，剩下的都保存到c的元组中
# def fn2(a,b,*c):
#     print('a =',a)
#     print('b =',b)
#     print('c =',c)

# 可变参数不是必须写在最后，但是注意，带*的参数后的所有参数，必须以关键字参数的形式传递
# 第一个参数给a，剩下的位置参数给b的元组，c必须使用关键字参数
# def fn2(a,*b,c):
#     print('a =',a)
#     print('b =',b)
#     print('c =',c)

# 所有的位置参数都给a，b和c必须使用关键字参数
# def fn2(*a,b,c):
#     print('a =',a)
#     print('b =',b)
#     print('c =',c)

# 如果在形参的开头直接写一个*,则要求我们的所有的参数必须以关键字参数的形式传递
def fn2(*,a,b,c):
    print('a =',a)
    print('b =',b)
    print('c =',c)
# fn2(a=3,b=4,c=5)

# *形参只能接收位置参数，而不能接收关键字参数
# def fn3(*a) :
#     print('a =',a)

# **形参可以接收其他的关键字参数，它会将这些参数统一保存到一个字典中
#   字典的key就是参数的名字，字典的value就是参数的值
# **形参只能有一个，并且必须写在所有参数的最后
def fn3(b,c,**a) :
    print('a =',a,type(a))
    print('b =',b)
    print('c =',c)

# fn3(b=1,d=2,c=3,e=10,f=20)

# 参数的解包（拆包）
def fn4(a,b,c):
    print('a =',a)
    print('b =',b)
    print('c =',c)

# 创建一个元组
t = (10,20,30)

# 传递实参时，也可以在序列类型的参数前添加星号，这样他会自动将序列中的元素依次作为参数传递
# 这里要求序列中元素的个数必须和形参的个数的一致
# fn4(*t)    

# 创建一个字典
d = {'a':100,'b':200,'c':300}
# 通过 **来对一个字典进行解包操作
fn4(**d)
```

#### 26.关于函数和函数对象的区别

```python
def fn5():
    return 10

# fn5 和 fn5()的区别
print(fn5) # fn5是函数对象，打印fn5实际是在打印函数对象 <function fn5 at 0x05771BB8>
print(fn5()) # fn5()是在调用函数，打印fn5()实际上是在打印fn5()函数的返回值 10
```

#### 27.python中使用global对全局变量赋值

```python
a = 20
def fn3():
	global a
	a = 10
	print(a)
fn3()
print(a)

result:
    10
	10
```

#### 28.高阶函数操作以及lambda函数

```python
# 高阶函数
# 接收函数作为参数，或者将函数作为返回值的函数是高阶函数
# 当我们使用一个函数作为参数时，实际上是将指定的代码传递进了目标函数

# 创建一个列表
l = [1,2,3,4,5,6,7,8,9,10]

# 定义一个函数
#   可以将指定列表中的所有的偶数，保存到一个新的列表中返回

# 定义一个函数，用来检查一个任意的数字是否是偶数
def fn2(i) :
    if i % 2 == 0 :
        return True

    return False    

# 这个函数用来检查指定的数字是否大于5
def fn3(i):
    if i > 5 :
        return True    
    return False

def fn(func , lst) :

    '''
        fn()函数可以将指定列表中的所有偶数获取出来，并保存到一个新列表中返回

        参数：
            lst：要进行筛选的列表
    '''
    # 创建一个新列表
    new_list = []

    # 对列表进行筛选
    for n in lst :
        # 判断n的奇偶
        if func(n) :
            new_list.append(n)
        # if n > 5 :
        #     new_list.append(n)

            


    # 返回新列表
    return new_list

# def fn4(i):
#     if i % 3 == 0:
#         return True    
#     return False

def fn4(i):
    return i % 3 == 0
        
# print(fn(fn4 , l))

# filter()
# filter()可以从序列中过滤出符合条件的元素，保存到一个新的序列中
# 参数：
#  1.函数，根据该函数来过滤序列（可迭代的结构）
#  2.需要过滤的序列（可迭代的结构）
# 返回值：
#   过滤后的新序列（可迭代的结构）

# fn4是作为参数传递进filter()函数中
#   而fn4实际上只有一个作用，就是作为filter()的参数
#   filter()调用完毕以后，fn4就已经没用
# 匿名函数 lambda 函数表达式 （语法糖）
#   lambda函数表达式专门用来创建一些简单的函数，他是函数创建的又一种方式
#   语法：lambda 参数列表 : 返回值
#   匿名函数一般都是作为参数使用，其他地方一般不会使用

def fn5(a , b):
    return a + b

# (lambda a,b : a + b)(10,20)
# 也可以将匿名函数赋值给一个变量，一般不会这么做
fn6 = lambda a,b : a + b
# print(fn6(10,30))


r = filter(lambda i : i > 5 , l)
# print(list(r))

# map()
# map()函数可以对可跌倒对象中的所有元素做指定的操作，然后将其添加到一个新的对象中返回
l = [1,2,3,4,5,6,7,8,9,10]

r = map(lambda i : i ** 2 , l)

# print(list(r))

# sort()
# 该方法用来对列表中的元素进行排序
# sort()方法默认是直接比较列表中的元素的大小
# 在sort()可以接收一个关键字参数 ， key
#   key需要一个函数作为参数，当设置了函数作为参数
#   每次都会以列表中的一个元素作为参数来调用函数，并且使用函数的返回值来比较元素的大小
l = ['bb','aaaa','c','ddddddddd','fff']
# l.sort(key=len)

l = [2,5,'1',3,'6','4']
l.sort(key=int)
# print(l)

# sorted()
# 这个函数和sort()的用法基本一致，但是sorted()可以对任意的序列进行排序
#   并且使用sorted()排序不会影响原来的对象，而是返回一个新对象

l = [2,5,'1',3,'6','4']
# l = "123765816742634781"

print('排序前:',l)
print(sorted(l,key=int))
print('排序后:',l)
```

#### 29.关于python的闭包处理

```python
# 将函数作为返回值返回，也是一种高阶函数
# 这种高阶函数我们也称为叫做闭包，通过闭包可以创建一些只有当前函数能访问的变量
#   可以将一些私有的数据藏到的闭包中
#当自己所创建的对象中有不愿意被他人看到或者受到该对象外因素影响的时候可以使用闭包
# 形成闭包的要件
#   ① 函数嵌套
#   ② 将内部函数作为返回值返回
#   ③ 内部函数必须要使用到外部函数的变量
def make_averager():
	nums = []
	def averager(n):
		nums.append(n)
		return sum(nums)/len(nums)
	return averager

averager = make_averager()
print(averager(10))
print(averager(100))

result:
    10.0
	55.0


```

#### 30.python中类的初始化以及操作

```python
class 类名（[父类]）：
	name
 	#成员变量
#类的声明与java区别只有格式上的不同，括号包括继承的父类不是必须元素
	def _init_(self，name):
        #成员初始化函数
        self.name = name
    def hello():
        print('hello')
    #成员方法
 

```

#### 31.封装

```python
# 可以为对象的属性使用双下划线开头，__xxx
# 双下划线开头的属性，是对象的隐藏属性，隐藏属性只能在类的内部访问，无法通过对象访问
# 其实隐藏属性只不过是Python自动为属性改了一个名字
#   实际上是将名字修改为了，_类名__属性名 比如 __name -> _Person__name
class Person:
    def __init__(self,name):
         self.__name = name

     def get_name(self):
         return self.__name

     def set_name(self , name):
         self.__name = name        

 p = Person('孙悟空')

# print(p.__name) __开头的属性是隐藏属性，无法通过对象访问
# p.__name = '猪八戒'
# print(p._Person__name)
# p._Person__name = '猪八戒'

# print(p.get_name())

# 使用__开头的属性，实际上依然可以在外部访问，所以这种方式我们一般不用
#   一般我们会将一些私有属性（不希望被外部访问的属性）以_开头
#   一般情况下，使用_开头的属性都是私有属性，没有特殊需要不要修改私有属性

```

#### 31.2.使用装饰器

```python
class Person:
    def __init__(self,name,age):
        self._name = name
        self._age = age

    # property装饰器，用来将一个get方法，转换为对象的属性
    # 添加为property装饰器以后，我们就可以像调用属性一样使用get方法
    # 使用property装饰的方法，必须和属性名是一样的
    @property    
    def name(self):
        print('get方法执行了~~~')
        return self._name

    # setter方法的装饰器：@属性名.setter
    @name.setter    
    def name(self , name):
        print('setter方法调用了')
        self._name = name        

    @property
    def age(self):
        return self._age

    @age.setter    
    def age(self , age):
        self._age = age   
```

#### 32.继承

```python
class Animal:
	def run(self):
		print('running....')
	def sleep(self):
		print('sleeping...')

class Dog(Animal):
	def bark(self):
		print('woo....')
 # 有一个类，能够实现我们需要的大部分功能，但是不能实现全部功能
# 如何能让这个类来实现全部的功能呢？
#   ① 直接修改这个类，在这个类中添加我们需要的功能
#       - 修改起来会比较麻烦，并且会违反OCP原则
#   ② 直接创建一个新的类
#       - 创建一个新的类比较麻烦，并且需要大量的进行复制粘贴，会出现大量的重复性代码
#   ③ 直接从Animal类中来继承它的属性和方法
#       - 继承是面向对象三大特性之一
#       - 通过继承我们可以使一个类获取到其他类中的属性和方法
#       - 在定义类时，可以在类名后的括号中指定当前类的父类（超类、基类、super）
#           子类（衍生类）可以直接继承父类中的所有的属性和方法
#           
#  通过继承可以直接让子类获取到父类的方法或属性，避免编写重复性的代码，并且也符合OCP原则
#   所以我们经常需要通过继承来对一个类进行扩展
d = Dog()
d.run()
d.sleep()
d.bark()
result:
    running....
	sleeping...
	woo....
#继承的详细处理
    class Animal :
    def __init__(self,name):
        self._name = name

    def run(self):
        print('动物会跑~~~')

    def sleep(self):
        print('动物睡觉~~~')

    @property
    def name(self):
        return self._name

    @name.setter    
    def name(self,name):
        self._name = name

# 父类中的所有方法都会被子类继承，包括特殊方法，也可以重写特殊方法
class Dog(Animal):

    def __init__(self,name,age):
        # 希望可以直接调用父类的__init__来初始化父类中定义的属性
        # super() 可以用来获取当前类的父类，
        #   并且通过super()返回对象调用父类方法时，不需要传递self
        super().__init__(name)
        self._age = age

    def bark(self):
        print('汪汪汪~~~') 

    def run(self):
        print('狗跑~~~~')   

    @property
    def age(self):
        return self._age

    @age.setter    
    def age(self,age):
        self._age = name        

d = Dog('旺财',18) 

print(d.name)       
print(d.age)       
```

#### 33.多重继承

```python
class A(object):
    def test(self):
        print('AAA')

class B(object):
    def test(self):
        print('B中的test()方法~~')

    def test2(self):
        print('BBB') 

# 在Python中是支持多重继承的，也就是我们可以为一个类同时指定多个父类
#   可以在类名的()后边添加多个类，来实现多重继承
#   多重继承，会使子类同时拥有多个父类，并且会获取到所有父类中的方法
# 在开发中没有特殊的情况，应该尽量避免使用多重继承，因为多重继承会让我们的代码过于复杂
# 如果多个父类中有同名的方法，则会现在第一个父类中寻找，然后找第二个，然后找第三个。。。
#   前边父类的方法会覆盖后边父类的方法
class C(A,B):
    pass

# 类名.__bases__ 这个属性可以用来获取当前类的所有父类    
# print(C.__bases__) (<class '__main__.B'>,)
# print(B.__bases__) (<class 'object'>,)

# print(C.__bases__) # (<class '__main__.A'>, <class '__main__.B'>)

c = C()

c.test()

```

#### 34.多态

```python
# 多态是面向对象的三大特征之一
# 多态从字面上理解是多种形态
# 狗（狼狗、藏獒、哈士奇、古牧 。。。）
# 一个对象可以以不同的形态去呈现

# 定义两个类
class A:
    def __init__(self,name):
        self._name = name

    @property
    def name(self):
        return self._name
        
    @name.setter
    def name(self,name):
        self._name = name   

class B:
    def __init__(self,name):
        self._name = name

    def __len__(self):
        return 10

    @property
    def name(self):
        return self._name
        
    @name.setter
    def name(self,name):
        self._name = name   

class C:
    pass


a = A('孙悟空')
b = B('猪八戒')
c = C()

# 定义一个函数
# 对于say_hello()这个函数来说，只要对象中含有name属性，它就可以作为参数传递
#   这个函数并不会考虑对象的类型，只要有name属性即可
def say_hello(obj):
    print('你好 %s'%obj.name)

# 在say_hello_2中我们做了一个类型检查，也就是只有obj是A类型的对象时，才可以正常使用，
#   其他类型的对象都无法使用该函数，这个函数就违反了多态
# 违反了多态的函数，只适用于一种类型的对象，无法处理其他类型对象，这样导致函数的适应性非常的差
# 注意，向isinstance()这种函数，在开发中一般是不会使用的！
def say_hello_2(obj):
    # 做类型检查
    if isinstance(obj , A):
        print('你好 %s'%obj.name)    
# say_hello(b)    
# say_hello_2(b)

# 鸭子类型
# 如果一个东西，走路像鸭子，叫声像鸭子，那么它就是鸭子

# len()
# 之所以一个对象能通过len()来获取长度，是因为对象中具有一个特殊方法__len__
# 换句话说，只要对象中具有__len__特殊方法，就可以通过len()来获取它的长度
l = [1,2,3]
s = 'hello'

# print(len(l))
# print(len(s))
print(len(b))
print(len(c))

# 面向对象的三大特征：
#   封装
#       - 确保对象中的数据安全
#   继承
#       - 保证了对象的可扩展性
#   多态
#       - 保证了程序的灵活性
```

#### 35.类中方法

```python
class A:
	count = 0
	def __init__(self):
		self.name = 'swk'
        
#这是一个普通实例方法        
	def test(self):
		print('这是一个实例方法')

#这是一个类方法，因为添加了@classmethod装饰器
	@classmethod
	def test_2(cls):
		print(cls.count)

#这是一个静态方法，因为添加了@staticmethod装饰器
	@staticmethod
	def test_3():
		print('test_3.....')

a = A()
a.count = 10
print(A.count)
print(a.count)
##########################
a.test()	#	等
A.test(a)	#	价
##########################

##########################
a.test_2()	#	等
A.test_2()	#	价
##########################

##########################
a.test_3()	#	等
A.test_3()	#	价
##########################
```

#### 36.垃圾回收

```python
# 程序运行过程中产生的垃圾会影响到程序的运行的运行性能，所以这些垃圾必须被及时清理
# 没用的东西就是垃圾
# 在程序中没有被引用的对象就是垃圾，这种垃圾对象过多以后会影响到程序的运行的性能
#   所以我们必须进行及时的垃圾回收，所谓的垃圾回收就是讲垃圾对象从内存中删除
# 在Python中有自动的垃圾回收机制，它会自动将这些没有被引用的对象删除，
#   所以我们不用手动处理垃圾回收

class A:
    def __init__(self):
        self.name = 'A类'

    # del是一个特殊方法，它会在对象被垃圾回收前调用
    def __del__(self):
        print('A()对象被删除了~~~',self)

a = A()
b = a # 又使用一个变量b，来引用a对应的对象

print(a.name)

# a = None # 将a设置为了None，此时没有任何的变量对A()对象进行引用，它就是变成了垃圾
# b = None
# del a
# del b
input('回车键退出...')
```

#### 37.模块的使用

```python
# 在一个模块中引入外部模块
# ① import 模块名 （模块名，就是python文件的名字，注意不要py）
# ② import 模块名 as 模块别名
#   - 可以引入同一个模块多次，但是模块的实例只会创建一个
#   - import可以在程序的任意位置调用，但是一般情况下，import语句都会统一写在程序的开头
#   - 在每一个模块内部都有一个__name__属性，通过这个属性可以获取到模块的名字
#   - __name__属性值为 __main__的模块是主模块，一个程序中只会有一个主模块
#       主模块就是我们直接通过 python 执行的模块
import test_module as test

# print(test.__name__)
print(__name__)

# import m

# # 访问模块中的变量：模块名.变量名
# # print(m.a , m.b)

# # m.test2()

# p = m.Person()

# print(p.name)

def test2():
    print('这是主模块中的test2')


# 也可以只引入模块中的部分内容
# 语法 from 模块名 import 变量,变量....
# from m import Person
# from m import test
# from m import Person,test
# from m import * # 引入到模块中所有内容，一般不会使用
# p1 = Person()
# print(p1)
# test()
# test2()

# 也可以为引入的变量使用别名
# 语法：from 模块名 import 变量 as 别名
# from m import test2 as new_test2

# test2()
# new_test2()

from m import *
# print(_c)

# import xxx
# import xxx as yyy
# from xxx import yyy , zzz , fff
# from xxx import *
# from xxx import yyy as zz

```

#### 38.异常处理

```python
print('异常出现前')
l = []
try:
    # print(c)
    # l[10]
    # 1 + 'hello'
    print(10/0)
except NameError:
    # 如果except后不跟任何的内容，则此时它会捕获到所有的异常
    # 如果在except后跟着一个异常的类型，那么此时它只会捕获该类型的异常
    print('出现 NameError 异常')
except ZeroDivisionError:
    print('出现 ZeroDivisionError 异常')
except IndexError:
    print('出现 IndexError 异常')
# Exception 是所有异常类的父类，所以如果except后跟的是Exception，他也会捕获到所有的异常
# 可以在异常类后边跟着一个 as xx 此时xx就是异常对象
except Exception as e :
    print('未知异常',e,type(e))
finally :
    print('无论是否出现异常，该子句都会执行')

print('异常出现后')
```

#### 39.文件操作

```python
# 打开文件
file_name = 'demo.txt'

# 调用open()来打开文件
# file_obj = open(file_name)

# # 当我们获取了文件对象以后，所有的对文件的操作都应该通过对象来进行
# # 读取文件中的内容
# # read()方法，用来读取文件中的内容，它会将内容全部保存为一个字符串返回
# content = file_obj.read()

# print(content)

# # 关闭文件
# # 调用close()方法来关闭文件
# file_obj.close()

# with ... as 语句
# with open(file_name) as file_obj :
#     # 在with语句中可以直接使用file_obj来做文件操作
#     # 此时这个文件只能在with中使用，一旦with结束则文件会自动close()
#     print(file_obj.read())

# open(file, mode='r', buffering=-1, encoding_=None, errors=None, newline=None, closefd=True, opener=None)
file_name = 'demo.txt'
try:
	with open(file_name) as file_obj:
		print(file_obj.read())
except Exception as e:
	raise e
    
    try:
    # 调用open()来打开一个文件，可以将文件分成两种类型
    # 一种，是纯文本文件（使用utf-8等编码编写的文本文件）
    # 一种，是二进制文件（图片、mp3、ppt等这些文件）
    # open()打开文件时，默认是以文本文件的形式打开的，但是open()默认的编码为None
    #   所以处理文本文件时，必须要指定文件的编码
    with open(file_name,encoding='utf-8') as file_obj:
        # 通过 read() 来读取文件中的内容
        # 如果直接调用read()它会将文本文件的所有内容全部都读取出来
        #   如果要读取的文件较大的话，会一次性将文件的内容加载到内存中，容易导致内存泄漏
        #   所以对于较大的文件，不要直接调用read()
        # help(file_obj.read)
        # read()可以接收一个size作为参数，该参数用来指定要读取的字符的数量
        #   默认值为-1，它会读取文件中的所有字符
        #   可以为size指定一个值，这样read()会读取指定数量的字符，
        #       每一次读取都是从上次读取到位置开始读取的
        #       如果字符的数量小于size，则会读取剩余所有的
        #       如果已经读取到了文件的最后了，则会返回''空串
        # content = file_obj.read(-1)
        content = file_obj.read(6)
        content = file_obj.read(6)
        content = file_obj.read(6)
        content = file_obj.read(6)
        # print(content)
        # print(len(content))
except FileNotFoundError :
    print(f'{file_name} 这个文件不存在！')

# 读取大文件的方式
file_name = 'demo.txt'

try:
    with open(file_name,encoding='utf-8') as file_obj:
        # 定义一个变量，来保存文件的内容
        file_content = ''
        # 定义一个变量，来指定每次读取的大小
        chunk = 100
        # 创建一个循环来读取文件内容
        while True:
            # 读取chunk大小的内容
            content = file_obj.read(chunk)

            # 检查是否读取到了内容
            if not content:
                # 内容读取完毕，退出循环
                break

            # 输出内容
            # print(content,end='')
            file_content += content

except FileNotFoundError :
    print(f'{file_name} 这个文件不存在！')
    
#按行读取
# readline()
    # 该方法可以用来读取一行内容
    # print(file_obj.readline(),end='')
    # print(file_obj.readline())
    # print(file_obj.readline())

    # readlines()
    # 该方法用于一行一行的读取内容，它会一次性将读取到的内容封装到一个列表中返回
import pprint
import os
file_name = 'demo.txt'
with open(file_name,encoding = 'gbk') as file_obj:
	print(file_obj.readline())
    
```

#### 40.文件写入操作

```python
# 使用open()打开文件时必须要指定打开文件所要做的操作（读、写、追加）
# 如果不指定操作类型，则默认是 读取文件 ， 而读取文件时是不能向文件中写入的
# r 表示只读的
# w 表示是可写的，使用w来写入文件时，如果文件不存在会创建文件，如果文件存在则会截断文件
#   截断文件指删除原来文件中的所有内容
# a 表示追加内容，如果文件不存在会创建文件，如果文件存在则会向文件中追加内容
# x 用来新建文件，如果文件不存在则创建，存在则报错
# + 为操作符增加功能
#   r+ 即可读又可写，文件不存在会报错
#   w+
#   a+
# with open(file_name , 'w' , encoding='utf-8') as file_obj:
# with open(file_name , 'r+' , encoding='utf-8') as file_obj:
with open(file_name , 'x' , encoding='utf-8') as file_obj:
    # write()来向文件中写入内容，
    # 如果操作的是一个文本文件的话，则write()需要传递一个字符串作为参数
    # 该方法会可以分多次向文件中写入内容
    # 写入完成以后，该方法会返回写入的字符的个数
    file_obj.write('aaa\n')
    file_obj.write('bbb\n')
    file_obj.write('ccc\n')
    r = file_obj.write(str(123)+'123123\n')
    r = file_obj.write('今天天气真不错')
    print(r)

```

#### 41.文件读取模式

```python
file_name = 'c:/Users/lilichao/Desktop/告白气球.flac'

# 读取模式
# t 读取文本文件（默认值）
# b 读取二进制文件

with open(file_name , 'rb') as file_obj:
    # 读取文本文件时，size是以字符为单位的
    # 读取二进制文件时，size是以字节为单位
    # print(file_obj.read(100))

    # 将读取到的内容写出来
    # 定义一个新的文件
    new_name = 'aa.flac'

    with open(new_name , 'wb') as new_obj:

        # 定义每次读取的大小
        chunk = 1024 * 100

        while True :
            # 从已有的对象中读取数据
            content = file_obj.read(chunk)

            # 内容读取完毕，终止循环
            if not content :
                break

            # 将读取到的数据写入到新对象中
            new_obj.write(content)
```

#### 42.文件读取位置

```python
# with open('demo.txt','rb') as file_obj:
#     # print(file_obj.read(100))
#     # print(file_obj.read(30))

#     # seek() 可以修改当前读取的位置
#     file_obj.seek(55)
#     file_obj.seek(80,0)
#     file_obj.seek(70,1)
#     file_obj.seek(-10,2)
#     # seek()需要两个参数
#     #   第一个 是要切换到的位置
#     #   第二个 计算位置方式
#     #       可选值：
#     #           0 从头计算，默认值
#     #           1 从当前位置计算
#     #           2 从最后位置开始计算

#     print(file_obj.read())

#     # tell() 方法用来查看当前读取的位置
#     print('当前读取到了 -->',file_obj.tell())

with open('demo2.txt','rt' , encoding='utf-8') as file_obj:
    # print(file_obj.read(100))
    # print(file_obj.read(30))

    # seek() 可以修改当前读取的位置
    file_obj.seek(9)
    # seek()需要两个参数
    #   第一个 是要切换到的位置
    #   第二个 计算位置方式
    #       可选值：
    #           0 从头计算，默认值
    #           1 从当前位置计算
    #           2 从最后位置开始计算

    print(file_obj.read())

    # tell() 方法用来查看当前读取的位置
    print('当前读取到了 -->',file_obj.tell())
    
```

43.文件其他操作

```python
import os
from pprint import pprint

# os.listdir() 获取指定目录的目录结构
# 需要一个路径作为参数，会获取到该路径下的目录结构，默认路径为 . 当前目录
# 该方法会返回一个列表，目录中的每一个文件（夹）的名字都是列表中的一个元素
r = os.listdir()

# os.getcwd() 获取当前所在的目录
r = os.getcwd()

# os.chdir() 切换当前所在的目录 作用相当于 cd
# os.chdir('c:/')

# r = os.getcwd()

# 创建目录
# os.mkdir("aaa") # 在当前目录下创建一个名字为 aaa 的目录

# 删除目录
# os.rmdir('abc')

# open('aa.txt','w')
# 删除文件
# os.remove('aa.txt')

# os.rename('旧名字','新名字') 可以对一个文件进行重命名，也可以用来移动一个文件
# os.rename('aa.txt','bb.txt')
os.rename('bb.txt','c:/users/lilichao/desktop/bb.txt')

pprint(r)
```

#### 43.python编写时注意指定文件编码格式

```python
# -*- coding: utf-8 -*-

```

