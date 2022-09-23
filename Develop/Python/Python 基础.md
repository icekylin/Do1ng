- [第一章 Python 变量](#第一章-python-变量)
  - [1. 定义变量](#1-定义变量)
    - [1.1 变量的多次赋值](#11-变量的多次赋值)
    - [1.2 向多个变量赋值](#12-向多个变量赋值)
    - [1.3 全局变量](#13-全局变量)
    - [1.4 global 关键字](#14-global-关键字)
    - [1.5 输出变量](#15-输出变量)
  - [2. 关键字](#2-关键字)
  - [3. 命名规则](#3-命名规则)
  - [4. 基本数据类型](#4-基本数据类型)
    - [4.1 内置数据类型](#41-内置数据类型)
    - [4.2 标准数据类型](#42-标准数据类型)
    - [4.3 Number (数字)](#43-number-数字)
    - [4.4 String（字符串）](#44-string字符串)
    - [4.5 List (列表)](#45-list-列表)
    - [4.6 Tuple（元组）](#46-tuple元组)
    - [4.7 Set (集合)](#47-set-集合)
    - [4.7 Dictionary（字典）](#47-dictionary字典)
  - [5. 类型转换](#5-类型转换)
    - [5.1 隐式类型转换](#51-隐式类型转换)
    - [5.2 显式类型转换](#52-显式类型转换)
    - [5.3 数据转换函数](#53-数据转换函数)
- [第二章 Python 运算符和表达式](#第二章-python-运算符和表达式)
  - [1 Python 算术运算符](#1-python-算术运算符)
  - [2 Python 赋值运算符](#2-python-赋值运算符)
  - [3. Python 比较运算符](#3-python-比较运算符)
  - [4. Python 逻辑运算符](#4-python-逻辑运算符)
  - [5. Python 身份运算符](#5-python-身份运算符)
  - [6. Python 成员运算符](#6-python-成员运算符)
  - [7. Python 位运算符](#7-python-位运算符)
- [第三章 Python 流程控制](#第三章-python-流程控制)
  - [1. 条件控制](#1-条件控制)
  - [2. 循环语句](#2-循环语句)
  - [3. break 和 continue 语句及循环中的 else 子句](#3-break-和-continue-语句及循环中的-else-子句)
  - [4. pass 语句](#4-pass-语句)
- [第四章 Python 基本数据结构](#第四章-python-基本数据结构)
  - [1. 列表](#1-列表)
    - [1.1 将列表当做堆栈使用](#11-将列表当做堆栈使用)
    - [1.2 将列表当作队列使用](#12-将列表当作队列使用)
    - [1.3 列表推导式](#13-列表推导式)
    - [1.4 嵌套列表解析](#14-嵌套列表解析)
  - [2. del 语句](#2-del-语句)
  - [3. 元组和序列](#3-元组和序列)
  - [4. 集合](#4-集合)
  - [5. 字典](#5-字典)
    - [5.1 遍历技巧](#51-遍历技巧)
- [第五章 Python 函数](#第五章-python-函数)
  - [0. return 返回值](#0-return-返回值)
  - [1. 定义函数](#1-定义函数)
    - [1.1 函数参数](#11-函数参数)
  - [2. 参数传递](#2-参数传递)
  - [3. 作用域](#3-作用域)
  - [4. lambda 表达式](#4-lambda-表达式)
  - [5 内置函数](#5-内置函数)
- [第六章 ython 面向对象](#第六章-ython-面向对象)
  - [0. 引言](#0-引言)
  - [1. 类和对象](#1-类和对象)
    - [1.1 定义类](#11-定义类)
    - [1.2 __init__()类构造方法](#12-init类构造方法)
    - [1.3 类对象的创建使用](#13-类对象的创建使用)
      - [1.3.1 Python类的实例化](#131-python类的实例化)
      - [1.3.2 Python类对象的使用](#132-python类对象的使用)
        - [(1) 类对象访问变量或方法](#1-类对象访问变量或方法)
        - [(2) 给类对象动态添加/删除变量](#2-给类对象动态添加删除变量)
        - [(3) 给类对象动态添加方法](#3-给类对象动态添加方法)
  - [2. 类的三大特性](#2-类的三大特性)
    - [2.1 封装](#21-封装)
      - [2.1.1 self](#211-self)
      - [2.1.2 属性](#212-属性)
        - [(1) 类属性 (类变量)](#1-类属性-类变量)
        - [(2) 实例属性 (实例变量)](#2-实例属性-实例变量)
        - [(3) 局部变量](#3-局部变量)
      - [2.1.3 方法](#213-方法)
        - [(1) 类实例方法](#1-类实例方法)
        - [(2) 类方法](#2-类方法)
        - [(3) 静态方法](#3-静态方法)
        - [(4) 类的专有方法](#4-类的专有方法)
        - [(5) 方法小结](#5-方法小结)
      - [2.1.4 访问控制](#214-访问控制)
        - [(1) 私有属性](#1-私有属性)
        - [(2) 保护属性](#2-保护属性)
        - [(3-拓展) 单下划线"`_`"](#3-拓展-单下划线_)
        - [(4-拓展) 双下划线"`__`"](#4-拓展-双下划线__)
    - [2.2 继承](#22-继承)
      - [2.2.1 单继承](#221-单继承)
      - [2.2.2 多继承](#222-多继承)
    - [2.3 多态](#23-多态)
      - [2.3.1 方法重写](#231-方法重写)
      - [2.3.2 调用重写后方法](#232-调用重写后方法)
  - [3. 运算符重载](#3-运算符重载)
      - [3.1 构造函数和析构函数：`__init__` 和 `__del__`](#31-构造函数和析构函数__init__-和-__del__)
      - [3.2 加减运算：`__add__` 和 `__sub__`](#32-加减运算__add__-和-__sub__)
      - [3.3 对象的字符串表达形式：`__repr__` 和 `__str__`](#33-对象的字符串表达形式__repr__-和-__str__)
      - [3.4 索引取值和赋值：`__getitem__` , `__setitem__`](#34-索引取值和赋值__getitem__--__setitem__)
      - [3.5 设置和访问属性：`__getattr__`、`__setattr__`](#35-设置和访问属性__getattr____setattr__)
      - [3.6 迭代器对象: `__iter__`,  `__next__`](#36-迭代器对象-__iter__--__next__)
  - [4. 装饰器](#4-装饰器)
  - [5. 反射](#5-反射)
    - [5.1 hasattr 和 getattr](#51-hasattr-和-getattr)
    - [5.2 setattr](#52-setattr)
    - [5.3 delattr](#53-delattr)
  - [Reference](#reference)
- [第七章 Python 模块](#第七章-python-模块)
  - [1. 导入模块](#1-导入模块)
    - [1.1 import 模块名 as 别名](#11-import-模块名-as-别名)
    - [1.2 from 模块名 import 成员名 as 别名](#12-from-模块名-import-成员名-as-别名)
  - [2. 常用模块](#2-常用模块)
    - [2.1 文件处理](#21-文件处理)
      - [2.1.1 os 模块](#211-os-模块)
        - [(1) 读取目录/结构](#1-读取目录结构)
        - [(2) 创建目录](#2-创建目录)
        - [(3) 删除目录](#3-删除目录)
        - [(4) 生成多级目录](#4-生成多级目录)
        - [(5) 删除多级目录](#5-删除多级目录)
        - [(6) 重命名文件](#6-重命名文件)
        - [(7) 获取文件或目录信息](#7-获取文件或目录信息)
        - [(8) 系统相关](#8-系统相关)
    - [2.2 时间日期](#22-时间日期)
      - [2.2.1 time模块](#221-time模块)
        - [(1) 获取时间戳](#1-获取时间戳)
        - [(2) 获取本地时间](#2-获取本地时间)
        - [(3) 获取格式化时间](#3-获取格式化时间)
        - [(4) 格式化日期](#4-格式化日期)
      - [2.2.2 calendar模块](#222-calendar模块)
        - [(1) 获取日历](#1-获取日历)
  - [Reference](#reference-1)
- [第八章 Python 包](#第八章-python-包)
    - [1. 创建包](#1-创建包)
    - [2. 导入包](#2-导入包)
      - [2.1 import 包名[.模块名 [as 别名]]](#21-import-包名模块名-as-别名)
      - [2.2 from 包名 import 模块名 [as 别名]](#22-from-包名-import-模块名-as-别名)
      - [2.3 from 包名.模块名 import 成员名 [as 别名]](#23from-包名模块名-import-成员名-as-别名)
  - [Reference](#reference-2)
- [第九章 Python 异常处理](#第九章-python-异常处理)
  - [0. 异常处理概述](#0-异常处理概述)
    - [0.1 Python语法错误](#01-python语法错误)
    - [0.2 Python运行时错误](#02-python运行时错误)
  - [1. 捕获异常](#1-捕获异常)
    - [1.1 try except 捕获异常](#11-try-except-捕获异常)
    - [1.2 获取特定异常的有关信息](#12-获取特定异常的有关信息)
  - [2. try...else...finaly 结构](#2-tryelsefinaly-结构)
    - [2.1 try except else](#21-try-except-else)
    - [2.2 try except finaly 资源回收](#22-try-except-finaly-资源回收)
  - [3. 自定义异常](#3-自定义异常)
    - [3.1 自定义异常类型](#31-自定义异常类型)
    - [3.2 如何手动抛出异常：raise](#32-如何手动抛出异常raise)
    - [3.3 捕捉用户手动抛出的异常](#33-捕捉用户手动抛出的异常)
  - [Reference](#reference-3)
- [第十章 Python 文件操作](#第十章-python-文件操作)
  - [1. 打开文件](#1-打开文件)
    - [1.1 open](#11-open)
    - [1.1 with...as...](#11-withas)
  - [2. 操作文件](#2-操作文件)
    - [2.1 逐个读取](#21-逐个读取)
    - [2.2 逐行读取](#22-逐行读取)
    - [2.3 读取文件位置](#23-读取文件位置)
    - [2.4 写入内容](#24-写入内容)
  - [3. 关闭文件](#3-关闭文件)
  - [Reference](#reference-4)

# 第一章 Python 变量

## 1. 定义变量

**变量是存放数据值的容器**

与其他编程语言不同，Python 没有声明变量的命令。

首次为其赋值时，才会创建变量。

在 Python 中，变量就是变量，它没有类型，我们所说的"类型"是变量所指的内存中对象的类型。

- 等号（=）用来给变量赋值。
- 等号（=）运算符左边是一个变量名
- 等号（=）运算符右边是存储在变量中的值。

**变量不需要使用任何特定类型声明，甚至可以在设置后更改其类型。**

```python
x = 5 # x is of type int
x = "Steve" # x is now of type str
print(x)
```

**字符串变量可以使用单引号或双引号进行声明：**

```python
x = "Bill"
# is the same as
x = 'Bill'
```

**变量由三部分组成**

- 标识：表示对象所存储的内存地址，使用内置函数id (obj) 来获取
- 类型：表示的是对象的数据类型，使用内置函数type (obj) 来获取
- 值：表示对象所存储的具体数据，使用orint(obj)可以将值进行打印输出

```python
name = 'kylin'  
print('id:', id(name))  
print('type:', type(name))  
print('value:', name)

# 输出结果
id: 4378058480
type: <class 'str'>
value: kylin
```

### 1.1 变量的多次赋值

当变量多次赋值时, 变量名会指向新的空间

```python
name = 'kylin'
name = 'moe'
print(name)

# 输出结果
moe
```

### 1.2 向多个变量赋值

Python 允许您在一行中为多个变量赋值：

```python
x, y, z = "Orange", "Banana", "Cherry"
print(x)
print(y)
print(z)
```

您可以在一行中为多个变量分配相同的值：

```python
x = y = z = "Orange"
print(x)
print(y)
print(z)
```

### 1.3 全局变量

在函数外部创建的变量（如上述所有实例所示）称为全局变量。

全局变量可以被函数内部和外部的每个人使用。

```python
# 在函数外部创建变量，并在函数内部使用它
x = "awesome"

def myfunc():
  print("Python is " + x)

myfunc()
```

如果在函数内部创建具有相同名称的变量，则该变量将是局部变量，并且只能在函数内部使用。具有相同名称的全局变量将保留原样，并拥有原始值。

```python
# 在函数内部创建一个与全局变量同名的变量：
x = "awesome"

def myfunc():
	# 局部变量 x
	x = "fantastic"
  print("Python is " + x)

myfunc()

print("Python is " + x)
```

### 1.4 global 关键字

通常，在函数内部创建变量时，该变量是局部变量，只能在该函数内部使用。

要在函数内部创建全局变量，您可以使用 global 关键字。

```python
# 如果您用了 global 关键字，则该变量属于全局范围：
def myfunc():
  global x
  x = "fantastic"

myfunc()

print("Python is " + x)
```

另外，如果要在函数内部更改全局变量，请使用 global 关键字。

```python
x = "awesome"

def myfunc():
  global x
  x = "fantastic"

myfunc()

print("Python is " + x)
```

### 1.5 输出变量

Python 的 print 语句通常用于输出变量。

**字符串 + 变量**

```python
x = "awesome"
print("Python is " + x)
```

**变量 + 变量**

```python
x = "abc"
y = "def"
print(x + y)
```

**数学运算**

```python
x = 1
y = 2
print(x + y)
```

**错误的输出**

```python
x = "Hello"
y = 1
print(x + y)

# TypeError: can only concatenate str (not "int") to str
```

## 2. 关键字

**Python 有一组关键字，这些关键字是保留字，不能用作变量名、函数名或任何其他标识符：**

| 关键字      | 描述                      |
|----------|-------------------------|
| and      | 逻辑运算符。                  |
| as       | 创建别名。                   |
| assert   | 用于调试。                   |
| break    | 跳出循环。                   |
| class    | 定义类。                    |
| continue | 继续循环的下一个迭代。             |
| def      | 定义函数。                   |
| del      | 删除对象。                   |
| elif     | 在条件语句中使用，等同于 else if。   |
| else     | 用于条件语句。                 |
| except   | 处理异常，发生异常时如何执行。         |
| False    | 布尔值，比较运算的结果。            |
| finally  | 处理异常，无论是否存在异常，都将执行一段代码。 |
| for      | 创建 for 循环。              |
| from     | 导入模块的特定部分。              |
| global   | 声明全局变量。                 |
| if       | 写一个条件语句。                |
| import   | 导入模块。                   |
| in       | 检查列表、元组等集合中是否存在某个值。     |
| is       | 测试两个变量是否相等。             |
| lambda   | 创建匿名函数。                 |
| None     | 表示 null 值。              |
| nonlocal | 声明非局部变量。                |
| not      | 逻辑运算符。                  |
| or       | 逻辑运算符。                  |
| pass     | null 语句，一条什么都不做的语句。     |
| raise    | 产生异常。                   |
| return   | 退出函数并返回值。               |
| True     | 布尔值，比较运算的结果。            |
| try      | 编写 try...except 语句。     |
| while    | 创建 while 循环。            |
| with     | 用于简化异常处理。               |
| yield    | 结束函数，返回生成器。             |

参考链接: [Python 关键字](https://www.w3school.com.cn/python/python_ref_keywords.asp)

## 3. 命名规则

变量可以使用短名称（如 x 和 y）或更具描述性的名称（age、carname、total_volume）。

Python 变量命名规则：

-   变量名必须以字母或下划线字符开头
-   变量名称不能以数字开头
-   变量名只能包含字母数字字符和下划线（A-z、0-9 和 _）
-   变量名称区分大小写（age、Age 和 AGE 是三个不同的变量）

请记住，变量名称区分大小写

## 4. 基本数据类型

### 4.1 内置数据类型

在编程中，数据类型是一个重要的概念。

变量可以存储不同类型的数据，并且不同类型可以执行不同的操作。

在这些类别中，Python 默认拥有以下内置数据类型：

| 文本类型：  | str                          |
|--------|------------------------------|
| 数值类型：  | int, float, complex          |
| 序列类型：  | list, tuple, range           |
| 映射类型：  | dict                         |
| 集合类型：  | set, frozenset               |
| 布尔类型：  | bool                         |
| 二进制类型： | bytes, bytearray, memoryview |

**获取数据类型**

```python
x = 10
print(type(x))
```

**设置数据类型**

在 Python 中，当您为变量赋值时，会设置数据类型：

| 示例                                           | 数据类型       |
|----------------------------------------------|------------|
| x = "Hello World"                        | str       |
| x = 29                                       | int        |
| x = 29.5                                     | float      |
| x = 1j                                       | complex    |
| x = ["apple", "banana", "cherry"]            | list       |
| x = ("apple", "banana", "cherry")            | tuple      |
| x = range(6)                                 | range      |
| x = {"name" : "Bill", "age" : 63}            | dict       |
| x = {"apple", "banana", "cherry"}            | set        |
| x = frozenset({"apple", "banana", "cherry"}) | frozenset  |
| x = True                                     | bool       |
| x = b"Hello"                                 | bytes      |
| x = bytearray(5)                             | bytearray  |
| x = memoryview(bytes(5))                     | memoryview |

**设定特定的数据类型**

如果希望指定数据类型，则您可以使用以下构造函数：

| 示例                                           | 数据类型       |
|----------------------------------------------|------------|
| x = str("Hello World")                       | str        |
| x = int(29)                                  | int        |
| x = float(29.5)                              | float      |
| x = complex(1j)                              | complex    |
| x = list(("apple", "banana", "cherry"))      | list       |
| x = tuple(("apple", "banana", "cherry"))     | tuple      |
| x = range(6)                                 | range      |
| x = dict(name="Bill", age=36)                | dict       |
| x = set(("apple", "banana", "cherry"))       | set        |
| x = frozenset(("apple", "banana", "cherry")) | frozenset  |
| x = bool(5)                                  | bool       |
| x = bytes(5)                                 | bytes      |
| x = bytearray(5)                             | bytearray  |
| x = memoryview(bytes(5))                     | memoryview |

### 4.2 标准数据类型

Python3 中有六个标准的数据类型：

-   Number（数字）
-   String（字符串）
-   List（列表）
-   Tuple（元组）
-   Set（集合）
-   Dictionary（字典）

Python3 的六个标准数据类型中：

-   **不可变数据（3 个）：**Number（数字）、String（字符串）、Tuple（元组）；
-   **可变数据（3 个）：**List（列表）、Dictionary（字典）、Set（集合）。

### 4.3 Number (数字)

Python3 支持 **int、float、bool、complex（复数）**。

在Python 3里，只有一种整数类型 **int**，表示为**长整型**，没有 python2 中的 Long。

像大多数语言一样，数值类型的赋值和计算都是很直观的。

内置的 type() 函数可以用来查询变量所指的对象类型。

### 4.4 String（字符串）

Python中的字符串用单引号 ' 或双引号 " 括起来，同时使用反斜杠 \ 转义特殊字符。

字符串的截取的语法格式如下：

`变量[头下标:尾下标]`

```python
#!/usr/bin/python3  
  
str = 'Runoob'  

print(str)          # 输出字符串  
print(str[0:-1])    # 输出第一个到倒数第二个的所有字符  
print(str[0])      # 输出字符串第一个字符  
print(str[2:5])        # 输出从第三个开始到第五个的字符  
print(str[2:])        # 输出从第三个开始的后的所有字符  
print(str * 2)           # 输出字符串两次，也可以写成 print (2 * str)  
print(str + "TEST")     # 连接字符串
```

**原始字符串**

Python 使用反斜杠 `\` 转义特殊字符，如果你不想让反斜杠发生转义，可以在字符串前面添加一个 r，表示原始字符串：

```python
>>> print('Ru\noob')
Ru  
oob  
>>> print(r'Ru\noob')
Ru\noob  
>>>
```

**跨越多行**

另外，反斜杠(\)可以作为续行符，表示下一行是上一行的延续。也可以使用 **"""..."""** 或者 **'''...'''** 跨越多行。

注意，Python 没有单独的字符类型，一个字符就是长度为1的字符串。

```python
print("""  
123  
456  
789  
""")
```

与 C 字符串不同的是，Python 字符串不能被改变。向一个索引位置赋值，比如word[0] = 'm'会导致错误。

-   1、反斜杠可以用来转义，使用r可以让反斜杠不发生转义。
-   2、字符串可以用+运算符连接在一起，用`*`运算符重复。
-   3、Python中的字符串有两种索引方式，从左往右以0开始，从右往左以-1开始。
-   4、Python中的字符串不能改变。

### 4.5 List (列表)

List（列表） 是 Python 中使用最频繁的数据类型。

列表可以完成大多数集合类的数据结构实现。列表中元素的类型可以不相同，它支持数字，字符串甚至可以包含列表（所谓嵌套）。

列表是写在方括号 `[]` 之间、用逗号分隔开的元素列表。

和字符串一样，列表同样可以被索引和截取，列表被截取后返回一个包含所需元素的新列表。

列表截取的语法格式如下：

`变量[头下标:尾下标]`

索引值以 0 为开始值，-1 为从末尾的开始位置。

加号 `+` 是列表连接运算符，星号 `*` 是重复操作。如下实例：

```python
#!/usr/bin/python3  
  
list = [ 'abcd', 786 , 2.23, 'runoob', 70.2 ]  
tinylist = [123, 'runoob']  
  
print (list)            # 输出完整列表  
print (list[0])         # 输出列表第一个元素  
print (list[1:3])       # 从第二个开始输出到第三个元素  
print (list[2:])        # 输出从第三个元素开始的所有元素  
print (tinylist * 2)    # 输出两次列表  
print (list + tinylist) # 连接列表
```

**可变的列表元素**

与Python字符串不一样的是，列表中的元素是可以改变的：

```python
>>> a = [1, 2, 3, 4, 5, 6]  
>>> a[0] = 9  
>>> a[2:5] = [13, 14, 15]  
>>> a  
[9, 2, 13, 14, 15, 6]  
>>> a[2:5] = []   # 将对应的元素值设置为 []  
>>> a  
[9, 2, 6]
```

-   1、List写在方括号之间，元素用逗号隔开。
-   2、和字符串一样，list可以被索引和切片。
-   3、List可以使用+操作符进行拼接。
-   4、List中的元素是可以改变的。

Python 列表截取可以接收第三个参数，参数作用是截取的步长，以下实例在索引 1 到索引 4 的位置并设置为步长为 2（间隔一个位置）来截取字符串, 如: `a[0::2]`

### 4.6 Tuple（元组）

元组（tuple）与列表类似，不同之处在于元组的元素不能修改。元组写在小括号 () 里，元素之间用逗号隔开。

元组中的元素类型也可以不相同：

```python
#!/usr/bin/python3

tuple = ( 'abcd', 786 , 2.23, 'runoob', 70.2  )
tinytuple = (123, 'runoob')

print(tuple)             # 输出完整元组
print(tuple[0])          # 输出元组的第一个元素
print(tuple[1:3])        # 输出从第二个元素开始到第三个元素
print(tuple[2:])         # 输出从第三个元素开始的所有元素
print(tinytuple * 2)     # 输出两次元组
print(tuple + tinytuple) # 连接元组
```

元组与字符串类似，可以被索引且下标索引从0开始，-1 为从末尾开始的位置。也可以进行截取（看上面，这里不再赘述）。

其实，可以把字符串看作一种特殊的元组。

```python
>>> tup = (1, 2, 3, 4, 5, 6)  
>>> print(tup[0])  
1  
>>> print(tup[1:5])  
(2, 3, 4, 5)  
>>> tup[0] = 11  # 修改元组元素的操作是非法的  
Traceback (most recent call last):  
  File "<stdin>", line 1, in <module>  
TypeError: 'tuple' object does not support item assignment  
>>>
```

虽然 tuple 的元素不可改变，但它可以包含可变的对象，比如 list 列表。

构造包含 0 个或 1 个元素的元组比较特殊，所以有一些额外的语法规则：

tup1 = ()    # 空元组

tup2 = (20,) # 一个元素，需要在元素后添加逗号

string、list 和 tuple 都属于 sequence（序列）。

-   1、与字符串一样，元组的元素不能修改。
-   2、元组也可以被索引和切片，方法一样。
-   3、注意构造包含 0 或 1 个元素的元组的特殊语法规则。
-   4、元组也可以使用+操作符进行拼接。

### 4.7 Set (集合)

集合（set）是由一个或数个形态各异的大小整体组成的，构成集合的事物或对象称作元素或是成员。

基本功能是进行成员关系测试和删除重复元素。

可以使用大括号 `{ }` 或者 `set()` 函数创建集合，注意：创建一个空集合必须用 `set()` 而不是 `{ }`，因为 `{ }` 是用来创建一个空字典。

创建格式：

```python
parame = {value01,value02,...}
或者
set(value)
```

集合示例:

```python
sites = {'Google', 'Taobao', 'Runoob', 'Facebook', 'Zhihu', 'Baidu'}  
  
print(sites)   # 输出集合，重复的元素被自动去掉  
  
# 成员测试  
if 'Runoob' in sites :  
    print('Runoob 在集合中')  
else :  
    print('Runoob 不在集合中')  
  
  
# set可以进行集合运算  
a = set('abracadabra')  
b = set('alacazam')  
  
print(a)  
  
print(a - b)     # a 和 b 的差集  
  
print(a | b)     # a 和 b 的并集  
  
print(a & b)     # a 和 b 的交集  
  
print(a ^ b)     # a 和 b 中不同时存在的元素
```

输出结果

```python
{'Taobao', 'Google', 'Facebook', 'Baidu', 'Runoob', 'Zhihu'}
Runoob 在集合中
{'a', 'r', 'b', 'd', 'c'}
{'r', 'b', 'd'}
{'a', 'm', 'r', 'l', 'z', 'b', 'd', 'c'}
{'a', 'c'}
{'b', 'r', 'm', 'l', 'd', 'z'}
```

### 4.7 Dictionary（字典）

字典（dictionary）是Python中另一个非常有用的内置数据类型。

列表是有序的对象集合，字典是无序的对象集合。两者之间的区别在于：字典当中的元素是通过键来存取的，而不是通过偏移存取。

字典是一种映射类型，字典用 `{ }` 标识，它是一个无序的 **键(key) : 值(value)** 的集合。

键(key)必须使用不可变类型。

在同一个字典中，键(key)必须是唯一的。

字典示例

```python
#!/usr/bin/python3

dict = {}
dict['one'] = "1 - 菜鸟教程"
dict[2]     = "2 - 菜鸟工具"

tinydict = {'name': 'runoob','code':1, 'site': 'www.runoob.com'}


print (dict['one'])       # 输出键为 'one' 的值
print (dict[2])           # 输出键为 2 的值
print (tinydict)          # 输出完整的字典
print (tinydict.keys())   # 输出所有键
print (tinydict.values()) # 输出所有值
```

输出结果

```python
1 - 菜鸟教程
2 - 菜鸟工具
{'name': 'runoob', 'code': 1, 'site': 'www.runoob.com'}
dict_keys(['name', 'code', 'site'])
dict_values(['runoob', 1, 'www.runoob.com'])
```

构造函数 dict() 可以直接从键值对序列中构建字典如下：

```python
>>> dict([('Runoob', 1), ('Google', 2), ('Taobao', 3)])
{'Runoob': 1, 'Google': 2, 'Taobao': 3}
>>> {x: x**2 for x in (2, 4, 6)}
{2: 4, 4: 16, 6: 36}
>>> dict(Runoob=1, Google=2, Taobao=3)
{'Runoob': 1, 'Google': 2, 'Taobao': 3}
```

字典类型也有一些内置的函数，例如 clear()、keys()、values() 等。

-   1、字典是一种映射类型，它的元素是键值对。
-   2、字典的关键字必须为不可变类型，且不能重复。
-   3、创建空字典使用 `{ }`。


## 5. 类型转换

Python 数据类型转换可以分为两种：

- 隐式类型转换 - 自动完成
- 显式类型转换 - 需要使用类型函数来转换

### 5.1 隐式类型转换

在隐式类型转换中，Python 会自动将一种数据类型转换为另一种数据类型，不需要我们去干预。

以下实例中，我们对两种不同类型的数据进行运算，较低数据类型（整数）就会转换为较高数据类型（浮点数）以避免数据丢失。
```python
num_int = 123  
num_flo = 1.23  
  
num_new = num_int + num_flo  
  
print("num_int 数据类型为:",type(num_int))  
print("num_flo 数据类型为:",type(num_flo))  
  
print("num_new 值为:",num_new)  
print("num_new 数据类型为:",type(num_new))
```

输出结果
```python
num_int 数据类型为: <class 'int'>
num_flo 数据类型为: <class 'float'>
num_new 值为: 124.23
num_new 数据类型为: <class 'float'>
```

- 实例中我们对两个不同数据类型的变量 `num_int` 和 `num_flo` 进行相加运算，并存储在变量 `num_new` 中。
- 然后查看三个变量的数据类型。
- 在输出结果中，我们看到 `num_int` 是 `整型（integer）` ， `num_flo` 是 `浮点型（float）`。
- 同样，新的变量 `num_new` 是 `浮点型（float）`，这是因为 Python 会将较小的数据类型转换为较大的数据类型，以避免数据丢失。

当 **字符串** 与 **整形** 数据进行加法运行时, 则无法转换, 会显示 `TypeError`, Python 提供了一种方案, 称为显示转换

### 5.2 显式类型转换

在显式类型转换中，用户将对象的数据类型转换为所需的数据类型。 我们使用 int()、float()、str() 等预定义函数来执行显式类型转换。

int() 强制转换为整型：
```python
x = int(1)   # x 输出结果为 1  
y = int(2.8) # y 输出结果为 2  
z = int("3") # z 输出结果为 3
```

float() 强制转换为浮点型：
```python
x = float(1)     # x 输出结果为 1.0  
y = float(2.8)   # y 输出结果为 2.8  
z = float("3")   # z 输出结果为 3.0  
w = float("4.2") # w 输出结果为 4.2
```

str() 强制转换为字符串类型：
```python
x = str("s1") # x 输出结果为 's1'  
y = str(2)    # y 输出结果为 '2'  
z = str(3.0)  # z 输出结果为 '3.0'
```

整型和字符串类型进行运算，就可以用强制类型转换来完成：
```python
num_int = 123  
num_str = "456"  
  
print("num_int 数据类型为:",type(num_int))  
print("类型转换前，num_str 数据类型为:",type(num_str))  
  
num_str = int(num_str)    # 强制转换为整型  
print("类型转换后，num_str 数据类型为:",type(num_str))  
  
num_sum = num_int + num_str  
  
print("num_int 与 num_str 相加结果为:",num_sum)  
print("sum 数据类型为:",type(num_sum))
```

输出结果
```python
num_int 数据类型为: <class 'int'>
类型转换前，num_str 数据类型为: <class 'str'>
类型转换后，num_str 数据类型为: <class 'int'>
num_int 与 num_str 相加结果为: 579
sum 数据类型为: <class 'int'>
```

### 5.3 数据转换函数

| 函数 | 描述 |
| --- | --- |
| [int(x [,base])](https://www.runoob.com/python3/python-func-int.html) | 将x转换为一个整数 |
| [float(x)](https://www.runoob.com/python3/python-func-float.html) | 将x转换到一个浮点数 |
| [complex(real [,imag])](https://www.runoob.com/python3/python-func-complex.html) | 创建一个复数 |
| [str(x)](https://www.runoob.com/python3/python-func-str.html) | 将对象 x 转换为字符串 |
| [repr(x)](https://www.runoob.com/python3/python-func-repr.html) | 将对象 x 转换为表达式字符串 |
| [eval(str)](https://www.runoob.com/python3/python-func-eval.html) | 用来计算在字符串中的有效Python表达式,并返回一个对象 |
| [tuple(s)](https://www.runoob.com/python3/python3-func-tuple.html) | 将序列 s 转换为一个元组 |
| [list(s)](https://www.runoob.com/python3/python3-att-list-list.html) | 将序列 s 转换为一个列表 |
| [set(s)](https://www.runoob.com/python3/python-func-set.html) | 转换为可变集合 |
| [dict(d)](https://www.runoob.com/python3/python-func-dict.html) | 创建一个字典。d 必须是一个 (key, value)元组序列。 |
| [frozenset(s)](https://www.runoob.com/python3/python-func-frozenset.html) | 转换为不可变集合 |
| [chr(x)](https://www.runoob.com/python3/python-func-chr.html) | 将一个整数转换为一个字符 |
| [ord(x)](https://www.runoob.com/python3/python-func-ord.html) | 将一个字符转换为它的整数值 |
| [hex(x)](https://www.runoob.com/python3/python-func-hex.html) | 将一个整数转换为一个十六进制字符串 |
| [oct(x)](https://www.runoob.com/python3/python-func-oct.html) | 将一个整数转换为一个八进制字符串 |

# 第二章 Python 运算符和表达式

## 1 Python 算术运算符

算术运算符与数值一起使用来执行常见的数学运算：

| 运算符 | 名称       | 实例     |
|-----|----------|--------|
| +   | 加        | x + y  |
| -   | 减        | x - y  |
| *   | 乘        | x * y  |
| /   | 除        | x / y  |
| %   | 取模       | x % y  |
| **  | 幂        | x ** y |
| //  | 地板除（取整除） | x // y |

## 2 Python 赋值运算符

赋值运算符用于为变量赋值：

| 运算符 | 实例      | 等同于        |
|-----|---------|------------|
| =   | x = 5   | x = 5      |
| +=  | x += 3  | x = x + 3  |
| -=  | x -= 3  | x = x - 3  |
| \*=  | x \*= 3  | x = x * 3  |
| /=  | x /= 3  | x = x / 3  |
| %=  | x %= 3  | x = x % 3  |
| //= | x //= 3 | x = x // 3 |
| \**= | x \**= 3 | x = x ** 3 |
| &=  | x &= 3  | x = x & 3  |
| \|=  | x \|= 3  | x = x \| 3  |
| ^=  | x ^= 3  | x = x ^ 3  |
| >>= | x >>= 3 | x = x >> 3 |
| <<= | x <<= 3 | x = x << 3 |

## 3. Python 比较运算符

比较运算符用于比较两个值：

| 运算符 | 名称    | 实例     |
|-----|-------|--------|
| ==  | 等于    | x == y |
| !=  | 不等于   | x != y |
| >   | 大于    | x > y  |
| <   | 小于    | x < y  |
| >=  | 大于或等于 | x >= y |
| <=  | 小于或等于 | x <= y |

## 4. Python 逻辑运算符

逻辑运算符用于组合条件语句：

| 运算符 | 描述                        | 实例                    |
|-----|---------------------------|-----------------------|
| and | 如果两个语句都为真，则返回 True。       | x > 3 and x < 10      |
| or  | 如果其中一个语句为真，则返回 True。      | x > 3 or x < 4        |
| not | 反转结果，如果结果为 true，则返回 False | not(x > 3 and x < 10) |

## 5. Python 身份运算符

身份运算符用于比较对象，不是比较它们是否相等，但如果它们实际上是同一个对象，则具有相同的内存位置：

| 运算符    | 描述                      | 实例         |
|--------|-------------------------|------------|
| is     | 如果两个变量是同一个对象，则返回 true。  | x is y     |
| is not | 如果两个变量不是同一个对象，则返回 true。 | x is not y |

## 6. Python 成员运算符

成员资格运算符用于测试序列是否在对象中出现：

| 运算符    | 描述                         | 实例         |
|--------|----------------------------|------------|
| in     | 如果对象中存在具有指定值的序列，则返回 True。  | x in y     |
| not in | 如果对象中不存在具有指定值的序列，则返回 True。 | x not in y |

## 7. Python 位运算符

位运算符用于比较（二进制）数字：

| 运算符 | 描述                   | 实例                           |
|-----|----------------------|------------------------------|
| &   | AND                  | 如果两个位均为 1，则将每个位设为 1。         |
| |   | OR                   | 如果两位中的一位为 1，则将每个位设为 1。       |
| ^   | XOR                  | 如果两个位中只有一位为 1，则将每个位设为 1。     |
| ~   | NOT                  | 反转所有位。                       |
| <<  | Zero fill left shift | 通过从右侧推入零来向左移动，推掉最左边的位。       |
| >>  | Signed right shift   | 通过从左侧推入最左边的位的副本向右移动，推掉最右边的位。 |

# 第三章 Python 流程控制

## 1. 条件控制

Python 条件语句是通过一条或多条语句的执行结果（True 或者 False）来决定执行的代码块。

**if 语句**

```python
if condition_1:
		statement_block_1
elif condition_2:
		statement_block_2
else:
		statement_block_3
```

-   如果 "condition_1" 为 True 将执行 "statement_block_1" 块语句
-   如果 "condition_1" 为False，将判断 "condition_2"
-   如果"condition_2" 为 True 将执行 "statement_block_2" 块语句
-   如果 "condition_2" 为False，将执行"statement_block_3"块语句

Python 中用 **elif** 代替了 **else if**，所以if语句的关键字为：**if – elif – else**。

-   1、每个条件后面要使用冒号 :，表示接下来是满足条件后要执行的语句块。
-   2、使用缩进来划分语句块，相同缩进数的语句在一起组成一个语句块。
-   3、在Python中没有switch – case语句。

if 示例
```python
#!/usr/bin/python3
var1 = 100
if var1:
	print ("1 - if 表达式条件为 true")
	print (var1)

var2 = 0
if var2:
	print ("2 - if 表达式条件为 true")
	print (var2)
print ("Good bye!")
```

输出结果
```python
1 - if 表达式条件为 true
100
Good bye!
```

在 if 中可以使用 **Python 比较运算符**

```python
#!/usr/bin/python3

# 程序演示了 == 操作符
# 使用数字
print(5 == 6)
# 使用变量
x = 5
y = 8
print(x == y)
```

high_low.py文件演示了数字的比较运算：
```python
#!/usr/bin/python3
# 该实例演示了数字猜谜游戏
number = 7
guess = -1
print("数字猜谜游戏!")
while guess != number:
	guess = int(input("请输入你猜的数字："))
	if guess == number:
		print("恭喜，你猜对了！")
	elif guess < number:
		print("猜的数字小了...")
	elif guess > number:
		print("猜的数字大了...")
```

**if 嵌套**

在嵌套 if 语句中，可以把 if...elif...else 结构放在另外一个 if...elif...else 结构中。

```python
if 表达式1:
    语句
    if 表达式2:
        语句
    elif 表达式3:
        语句
    else:
        语句
elif 表达式4:
    语句
else:
    语句
```

```python
num = int(input("输入一个数字："))  
if num % 2 == 0:  
    if num % 3 == 0:  
        print("你输入的数字可以整除 2 和 3")  
    else:  
        print("你输入的数字可以整除 2，但不能整除 3")  
else:  
    if num % 3 == 0:  
        print("你输入的数字可以整除 3，但不能整除 2")  
    else:  
        print("你输入的数字不能整除 2 和 3")
```

## 2. 循环语句

Python 中的循环语句有 for 和 while。

**4.2.1 while 循环**

Python 中 while 语句的一般形式：

```python
while 判断条件(condition)：
    执行语句(statements)……
```

同样需要注意冒号和缩进。另外，在 Python 中没有 do..while 循环。

以下实例使用了 while 来计算 1 到 100 的总和：

```python
# !/usr/bin/python3

counter = 1  
sum = 0  
n = 100  
  
while counter <= n:  
    sum = sum + counter  
    counter += 1  
  
print("1 到 %d 之和为 %d" % (n, sum))
```

**无限循环**

我们可以通过设置条件表达式永远不为 false 来实现无限循环，实例如下：

```python
#!/usr/bin/python3

var = 1
while var == 1 : # 表达式永远为 true
	num = int(input("输入一个数字 :"))
	print ("你输入的数字是: ", num)

print ("Good bye!")
```

**while 循环使用 else 语句**

如果 while 后面的条件语句为 false 时，则执行 else 的语句块。

```python
while <expr>:
    <statement(s)>
else:
    <additional_statement(s)>
```

expr 条件语句为 true 则执行 statement(s) 语句块，如果为 false，则执行 additional_statement(s)。

循环输出数字，并判断大小：

```python
#!/usr/bin/python3  
  
count = 0  
  
while count < 5:  
    print(count, "小于 5")  
    count += 1  
else:  
    print(count, "大于 5")
```

**简单语句组**

类似if语句的语法，如果你的while循环体中只有一条语句，你可以将该语句与while写在同一行中， 如下所示：

```python
flag = 1  
  
while (flag): print('我疯了!')  
  
print("Good bye!")
```

以上的无限循环你可以使用 CTRL+C 来中断循环。

**4.2.2 for 语句**

Python for 循环可以遍历任何可迭代对象，如一个列表或者一个字符串。

```python
for <variable> in <sequence>:
	<statements>
else:
	<statements>
```

for 循环输出示例

```python
languages = ["C", "C++", "Perl", "Python"]
for x in languages:
	print (x)
```

输出结果

```python
C
C++
Perl
Python
```

以下 for 实例中使用了 break 语句，break 语句用于跳出当前循环体：

```python
sites = ["Baidu", "Google", "Hello", "Taobao"]  
for site in sites:  
    if site == "Hello":  
        print("菜鸟教程!")  
        break  
    print("循环数据 " + site)  
else:  
    print("没有循环数据!")  
print("完成循环!")
```

**4.2.3 range()函数**

如果你需要遍历数字序列，可以使用内置range()函数。它会生成数列，例如:

```python
for i in range(5):
	print(i)
```

你也可以使用range指定区间的值：

```python
for i in range(5,9):
	print(i)
```

也可以使range以指定数字开始并指定不同的增量(甚至可以是负数，有时这也叫做'步长'):

```python
for i in range(-10, -100, -30):
	print(i)
```

您可以结合range()和len()函数以遍历一个序列的索引,如下所示:

```python
a = ['Google', 'Baidu', 'Runoob', 'Taobao', 'QQ']  
for i in range(len(a)):  
    print(i, a[i])
```
还可以使用range()函数来创建一个列表：

```python
list(range(5))
```

## 3. break 和 continue 语句及循环中的 else 子句

**break** 语句可以跳出 for 和 while 的循环体。如果你从 for 或 while 循环中终止，任何对应的循环 else 块将不执行。

```python
n = 5  
while n > 0:  
    n -= 1  
    if n == 2:  
        break  
    print(n)  
print('循环结束')
```

输出结果

```python
4
3
循环结束
```

**continue** 语句被用来告诉 Python 跳过当前循环块中的剩余语句，然后继续进行下一轮循环。

```python
n = 5  
while n > 0:  
    n -= 1  
    if n == 2:  
        continue  
    print(n)  
print('循环结束')
```

输出结果

```python
4
3
1
0
循环结束
```

**跳过输出示例**

```python
#!/usr/bin/python3  
  
for letter in 'good':  # 第一个实例  
    if letter == 'o':  # 字母为 o 时跳过输出  
        continue  
    print('当前字母 :', letter)  
  
var = 4  # 第二个实例  
while var > 0:  
    var = var - 1  
    if var == 2:  # 变量为 5 时跳过输出  
        continue  
    print('当前变量值 :', var)  
print("Good bye!")
```

输出结果

```python
当前字母 : g
当前字母 : d
当前变量值 : 3
当前变量值 : 1
当前变量值 : 0
Good bye!
```

## 4. pass 语句

Python pass是空语句，是为了保持程序结构的完整性。

pass 不做任何事情，一般用做占位语句，如下实例

```python
while True:
	pass # 等待键盘中断 (Ctrl+C)
```

以下实例在字母为 o 时 执行 pass 语句块:
```python
for letter in 'Runoob':  
    if letter == 'o':  
        pass  
        print('执行 pass 块')  
    print('当前字母 :', letter)  
  
print("Good bye!")
```

输出结果

```python
当前字母 : R
当前字母 : u
当前字母 : n
执行 pass 块
当前字母 : o
执行 pass 块
当前字母 : o
当前字母 : b
Good bye!
```

# 第四章 Python 基本数据结构

## 1. 列表

Python中列表是可变的，这是它区别于字符串和元组的最重要的特点，一句话概括即：列表可以修改，而字符串和元组不能。

以下是 Python 中列表的方法：

| 方法                | 描述                                                                                                                         |
|-------------------|----------------------------------------------------------------------------------------------------------------------------|
| list.append(x)    | 把一个元素添加到列表的结尾，相当于 a[len(a):] = [x]。                                                                                        |
| list.extend(L)    | 通过添加指定列表的所有元素来扩充列表，相当于 a[len(a):] = L。                                                                                     |
| list.insert(i, x) | 在指定位置插入一个元素。第一个参数是准备插入到其前面的那个元素的索引，例如 a.insert(0, x) 会插入到整个列表之前，而 a.insert(len(a), x) 相当于 a.append(x) 。                    |
| list.remove(x)    | 删除列表中值为 x 的第一个元素。如果没有这样的元素，就会返回一个错误。                                                                                       |
| list.pop([i])     | 从列表的指定位置移除元素，并将其返回。如果没有指定索引，a.pop()返回最后一个元素。元素随即从列表中被移除。（方法中 i 两边的方括号表示这个参数是可选的，而不是要求你输入一对方括号，你会经常在 Python 库参考手册中遇到这样的标记。） |
| list.clear()      | 移除列表中的所有项，等于del a[:]。                                                                                                      |
| list.index(x)     | 返回列表中第一个值为 x 的元素的索引。如果没有匹配的元素就会返回一个错误。                                                                                     |
| list.count(x)     | 返回 x 在列表中出现的次数。                                                                                                            |
| list.sort()       | 对列表中的元素进行排序。                                                                                                               |
| list.reverse()    | 倒排列表中的元素。                                                                                                                  |
| list.copy()       | 返回列表的浅复制，等于a[:]。                                                                                                           |

下面示例演示了列表的大部分方法：

```python
  
# 定义列表  
a = [66.25, 333, 333, 1, 1234.5]  
  
# 统计  
print(a.count(333), a.count(66.25), a.count('x'))  
  
# 在 2 的位置添加 -1 元素  
a.insert(2, -1)  
# 在末尾添加 333 元素  
a.append(333)  
print(a)  
  
# 返回列表中第一个值为 1 的元素  
print(a.index(1))  
  
# 删除列表中值为 333 的第一个元素  
a.remove(333)  
print(a)  
  
# 倒排列表中的元素  
a.reverse()  
print(a)  
  
# 对列表中的元素排序  
a.sort()  
print(a)
```

输出结果

```python
2 1 0
[66.25, 333, -1, 333, 1, 1234.5, 333]
4
[66.25, -1, 333, 1, 1234.5, 333]
[333, 1234.5, 1, 333, -1, 66.25]
[-1, 1, 66.25, 333, 333, 1234.5]
```

### 1.1 将列表当做堆栈使用

列表方法使得列表可以很方便的作为一个堆栈来使用，堆栈作为特定的数据结构，最先进入的元素最后一个被释放（后进先出）

用 append() 方法可以把一个元素添加到堆栈顶。用不指定索引的 pop() 方法可以把一个元素从堆栈顶释放出来。例如：

```python
stack = [3, 4, 5]  
stack.append(6)  
stack.append(7)  
print(stack)  
  
stack.pop()  
print(stack)  
[3, 4, 5, 6]  
  
stack.pop()  
print(stack)
```

输出结果

```python
[3, 4, 5, 6, 7]
[3, 4, 5, 6]
[3, 4, 5]
```

### 1.2 将列表当作队列使用

也可以把列表当做队列用，只是在队列里第一加入的元素，第一个取出来；但是拿列表用作这样的目的效率不高。

在列表的最后添加或者弹出元素速度快，然而在列表里插入或者从头部弹出速度却不快（因为所有其他的元素都得一个一个地移动）。

```python
from collections import deque  
  
queue = deque(["Eric", "John", "Michael"])  
print(queue)  
queue.append("Terry")  
print(queue)  
queue.append("Graham")  
print(queue)  
queue.popleft()  
print(queue)  
queue.popleft()  
print(queue)
```

输出结果

```python
deque(['Eric', 'John', 'Michael'])
deque(['Eric', 'John', 'Michael', 'Terry'])
deque(['Eric', 'John', 'Michael', 'Terry', 'Graham'])
deque(['John', 'Michael', 'Terry', 'Graham'])
deque(['Michael', 'Terry', 'Graham'])
```

### 1.3 列表推导式

列表推导式提供了从序列创建列表的简单途径。通常应用程序将一些操作应用于某个序列的每个元素，用其获得的结果作为生成新列表的元素，或者根据确定的判定条件创建子序列。

每个列表推导式都在 for 之后跟一个表达式，然后有零到多个 for 或 if 子句。返回结果是一个根据表达从其后的 for 和 if 上下文环境中生成出来的列表。如果希望表达式推导出一个元组，就必须使用括号。

这里我们将列表中每个数值乘三，获得一个新的列表：

```python
>>> vec = [2, 4, 6]
>>> [3*x for x in vec]
[6, 12, 18]
```

现在我们玩一点小花样：

```python
>>> [[x, x**2] for x in vec]
[[2, 4], [4, 16], [6, 36]]
```

这里我们对序列里每一个元素逐个调用某方法：

```python
>>> freshfruit = ['banana', 'loganberry', 'passion fruit']
>>> [weapon.strip() for weapon in freshfruit]
['banana', 'loganberry', 'passion fruit']
```

我们可以用 if 子句作为过滤器：

```python
>>> vec = [2, 4, 6]
>>> [3*x for x in vec if x > 3]
[12, 18]
>>> [3*x for x in vec if x < 2]
[]
```

以下是一些关于循环和其它技巧的演示：

```python
>>> vec1 = [2, 4, 6]
>>> vec2 = [4, 3, -9]
>>> [x*y for x in vec1 for y in vec2]
[8, 6, -18, 16, 12, -36, 24, 18, -54]
>>> [x+y for x in vec1 for y in vec2]
[6, 5, -7, 8, 7, -5, 10, 9, -3]
>>> [vec1[i]*vec2[i] for i in range(len(vec1))]
[8, 12, -54]
```

列表推导式可以使用复杂表达式或嵌套函数：

```python
>>> [str(round(355/113, i)) for i in range(1, 6)]
['3.1', '3.14', '3.142', '3.1416', '3.14159']
```

### 1.4 嵌套列表解析

Python的列表还可以嵌套。

以下实例展示了3X4的矩阵列表：

```python
matrix = [  
     [1,2,3,4],  
     [5,6,7,8],  
     [9,10,11,12],  
]  
  
print([[row[i] for row in matrix] for i in range(4)])
```

输出结果

```python
[[1, 5, 9], [2, 6, 10], [3, 7, 11], [4, 8, 12]]
```

## 2. del 语句

使用 del 语句可以从一个列表中根据索引来删除一个元素，而不是值来删除元素。这与使用 pop() 返回一个值不同。可以用 del 语句从列表中删除一个切割，或清空整个列表（我们以前介绍的方法是给该切割赋一个空列表）。例如：

```python
>>> a = [-1, 1, 66.25, 333, 333, 1234.5]
>>> del a[0]
>>> a
[1, 66.25, 333, 333, 1234.5]
>>> del a[2:4]
>>> a
[1, 66.25, 1234.5]
>>> del a[:]
>>> a
[]
```

也可以用 del 删除实体变量：

```python
del a
```

## 3. 元组和序列

元组由若干逗号分隔的值组成，例如：

```python
>>> t = 12345, 54321, 'hello!'
>>> t[0]
12345
>>> t
(12345, 54321, 'hello!')
>>> # 元组可以嵌套
>>> u = t, (1, 2, 3, 4, 5)
>>> u
((12345, 54321, 'hello!'), (1, 2, 3, 4, 5))
```

## 4. 集合

集合是一个无序不重复元素的集。基本功能包括关系测试和消除重复元素。

可以用大括号({})创建集合。注意：如果要创建一个空集合，你必须用 set() 而不是 {} ；后者创建一个空的字典，下一节我们会介绍这个数据结构。

以下是一个简单的演示：

```python
>>> basket = {'apple', 'orange', 'apple', 'pear', 'orange', 'banana'}
>>> print(basket)
>>> # 输出不包含重复元素
{'orange', 'banana', 'pear', 'apple'}
# 检测成员
>>> 'orange' in basket
True
>>> 'crabgrass' in basket
False

>>> # 以下演示了两个集合的操作
...
>>> a = set('abracadabra')
>>> b = set('alacazam')
>>>  # a 中唯一的字母
>>> a
{'a', 'r', 'b', 'c', 'd'}
>>> # 在 a 中的字母，但不在 b 中
>>> a - b
{'r', 'd', 'b'}
>>> # 在 a 或 b 中的字母
>>> a | b
{'a', 'c', 'r', 'd', 'b', 'm', 'z', 'l'}
>>> # 在 a 和 b 中都有的字母
>>> a & b
{'a', 'c'}
>>> # 在 a 或 b 中的字母，但不同时在 a 和 b 中
>>> a ^ b
{'r', 'd', 'b', 'm', 'z', 'l'}
```

## 5. 字典

另一个非常有用的 Python 内建数据类型是字典。

序列是以连续的整数为索引，与此不同的是，字典以关键字为索引，关键字可以是任意不可变类型，通常用字符串或数值。

理解字典的最佳方式是把它看做无序的键=>值对集合。在同一个字典之内，关键字必须是互不相同。

一对大括号创建一个空的字典：{}。

这是一个字典运用的简单例子：

```python
tel = {'jack': 4098, 'sape': 4139}
# 字典新增内容
tel['guido'] = 4127
print(tel)

# 查看 jack 键值对应元素
tel['jack']

# 删除 sape 键值
del tel['sape']

# 新增键值 irv 元素为 4127
tel['irv'] = 4127
print(tel)

# 列表形式输出 tel 键值
print(list(tel.keys()))

# 排序输出键值
sorted(tel.keys())
['guido', 'irv', 'jack']

# 判断键值是否存在于 tel
'guido' in tel
'jack' not in tel
```

输出结果

```python
{'jack': 4098, 'sape': 4139, 'guido': 4127}
{'jack': 4098, 'guido': 4127, 'irv': 4127}
['jack', 'guido', 'irv']
True
False
```

构造函数 dict() 直接从键值对元组列表中构建字典。如果有固定的模式，列表推导式指定特定的键值对：

```python
>>> dict([('sape', 4139), ('guido', 4127), ('jack', 4098)])
{'sape': 4139, 'jack': 4098, 'guido': 4127}
```

此外，字典推导可以用来创建任意键和值的表达式词典：

```python
>>> {x: x**2 for x in (2, 4, 6)}
{2: 4, 4: 16, 6: 36}
```

如果关键字只是简单的字符串，使用关键字参数指定键值对有时候更方便：

```python
>>> dict(sape=4139, guido=4127, jack=4098)
{'sape': 4139, 'jack': 4098, 'guido': 4127}
```

### 5.1 遍历技巧

在字典中遍历时，关键字和对应的值可以使用 items() 方法同时解读出来：

```python
>>> knights = {'gallahad': 'the pure', 'robin': 'the brave'}
>>> for k, v in knights.items():
     print(k, v)

gallahad the pure
robin the brave

>>> for k in knights.items():
     print(k)

('gallahad', 'the pure')
('robin', 'the brave')
```

在序列中遍历时，索引位置和对应值可以使用 enumerate() 函数同时得到：

```python
>>> for i, v in enumerate(['tic', 'tac', 'toe']):
     print(i, v)

0 tic
1 tac
2 toe
```

同时遍历两个或更多的序列，可以使用 zip() 组合：

```python
>>> questions = ['name', 'quest', 'favorite color']
>>> answers = ['lancelot', 'the holy grail', 'blue']
>>> for q, a in zip(questions, answers):
     print('What is your {0}?  It is {1}.'.format(q, a))

What is your name?  It is lancelot.
What is your quest?  It is the holy grail.
What is your favorite color?  It is blue.
```

要反向遍历一个序列，首先指定这个序列，然后调用 reversed() 函数：

```python
>>> for i in reversed(range(1, 10, 2)):
     print(i)

9
7
5
3
1
```

要按顺序遍历一个序列，使用 sorted() 函数返回一个已排序的序列，并不修改原值：

```python
>>> basket = ['apple', 'orange', 'apple', 'pear', 'orange', 'banana']
>>> for f in sorted(set(basket)):
     print(f)

apple
banana
orange
pear
```

# 第五章 Python 函数


## 0. return 返回值

**return 语句**

**return [表达式]** 语句用于退出函数，选择性地向调用方返回一个表达式。不带参数值的 return 语句返回 None。之前的例子都没有示范如何返回数值，以下实例演示了 return 语句的用法

```python
#!/usr/bin/python3  
  
# 可写函数说明  
def sum(arg1, arg2):  
    # 返回2个参数的和."  
    total = arg1 + arg2  
    print("函数内 : ", total)  
    return total  
  
  
# 调用sum函数  
total = sum(10, 20)  
print("函数外 : ", total)
```

输出结果

```python
函数内 :  30
函数外 :  30
```


## 1. 定义函数

你可以定义一个由自己想要功能的函数，以下是简单的规则：

-   函数代码块以 **def** 关键词开头，后接函数标识符名称和圆括号 **()**。
-   任何传入参数和自变量必须放在圆括号中间，圆括号之间可以用于定义参数。
-   函数的第一行语句可以选择性地使用文档字符串—用于存放函数说明。
-   函数内容以冒号 : 起始，并且缩进。
-   **return [表达式]** 结束函数，选择性地返回一个值给调用方，不带表达式的 return 相当于返回 None。

```python
def 函数名(参数列表):
    函数体
```

**定义输出 Hello World + [value] 的函数, 并且调用 hello 函数**

```python
def hello(value):  
   print('Hello %s!' % value)  
  
hello("kylin")
```

### 1.1 函数参数

以下是调用函数时可使用的正式参数类型：

-   必需参数
-   关键字参数
-   默认参数
-   不定长参数

**6.2.1 必需参数**

必需参数须以正确的顺序传入函数。调用时的数量必须和声明时的一样。

调用 printme() 函数，你必须传入一个参数，不然会出现语法错误：

```python
#!/usr/bin/python3  
  
# 可写函数说明  
def printme(str):  
    "打印任何传入的字符串"  
    print(str)  
    return  
  
# 调用 printme 函数，不加参数会报错  
printme()
```

输出结果

```python
    printme()
TypeError: printme() missing 1 required positional argument: 'str'
```

**6.2.2 关键字参数**

关键字参数和函数调用关系紧密，函数调用使用关键字参数来确定传入的参数值。

使用关键字参数允许函数调用时参数的顺序与声明时不一致，因为 Python 解释器能够用参数名匹配参数值。

以下实例在函数 printme() 调用时使用参数名：

```python
#!/usr/bin/python3  
  
# 可写函数说明  
def printme(str):  
    "打印任何传入的字符串"  
    print(str)  
    return  
  
# 调用printme函数  
printme(str="菜鸟教程")
```

以下实例中演示了函数参数的使用不需要使用指定顺序：

```python
#!/usr/bin/python3  
  
# 可写函数说明  
def printinfo(name, age):  
    "打印任何传入的字符串"  
    print("名字: ", name)  
    print("年龄: ", age)  
    return  
  
# 调用printinfo函数  
printinfo(age=50, name="kylin")
```

输出结果

```python
名字:  kylin
年龄:  50
```

**6.2.3 默认参数**

调用函数时，如果没有传递参数，则会使用默认参数。以下实例中如果没有传入 age 参数，则使用默认值：

```python
#!/usr/bin/python3  
  
# 可写函数说明  
def printinfo(name, age=35):  
    print("名字: ", name)  
    print("年龄: ", age)  
    return  
  
# 调用printinfo函数, 不传递 age 参数  
printinfo(name="kylin")
```

**6.2.4 不定长参数**

你可能需要一个函数能处理比当初声明时更多的参数。这些参数叫做不定长参数，和上述 2 种参数不同，声明时不会命名。基本语法如下：

```python
def functionname([formal_args,] *var_args_tuple ):
   "函数_文档字符串"
   function_suite
   return [expression]
```

加了星号 `*` 的参数会以**元组(tuple)** 的形式导入，存放所有未命名的变量参数。

```python
#!/usr/bin/python3  
  
# 可写函数说明  
def printinfo(arg1, *vartuple):  
    # 打印任何传入的参数  
    print("输出: ")  
    print(arg1)  
    print(vartuple)  
  
# 调用 printinfo 函数  
printinfo(70, 60, 50)
```

输出结果

```python
输出: 
70
(60, 50)
```

如果在函数调用时没有指定参数，它就是一个空元组。我们也可以不向函数传递未命名的变量。如下实例：

```python
#!/usr/bin/python3  
  
# 可写函数说明  
def printinfo(arg1, *vartuple):  
    "打印任何传入的参数"  
    print("输出: ")  
    print(arg1)  
    for var in vartuple:  
        print(var)  
    return  

# 调用 printinfo 函数  
printinfo(10)
printinfo(70, 60, 50)
```

输出结果

```python
输出: 
10
输出: 
70
60
50
```

还有一种就是参数带两个星号 **基本语法如下：

```python
def functionname([formal_args,] **var_args_dict ):
   "函数_文档字符串"
   function_suite
   return [expression]
```

加了两个星号 ** 的参数会以 **字典(dict)** 的形式导入。

```python
#!/usr/bin/python3  
  
# 可写函数说明  
def printinfo(arg1, **vardict):  
    # 打印任何传入的参数  
    print(arg1)  
    print(vardict)  
  
# 调用 printinfo 函数  
printinfo(1, a=2, b=3)
```

输出结果

```python
1
{'a': 2, 'b': 3}
```

声明函数时，参数中星号 * 可以单独出现，例如:

```python
def f(a,b,*,c):
    return a+b+c
```

如果单独出现星号 \*，则星号 \* 后的参数必须用关键字传入：

```python
def f(a,b,*,c):  
    return a+b+c  
  
f(1,2,3)   # 报错  
  
f(1,2,c=3) # 正常
```

## 2. 参数传递

在 python 中，类型属于对象，对象有不同类型的区分，变量是没有类型的：

```python
a=[1,2,3]

a="Runoob"
```

以上代码中，**[1,2,3]** 是 List 类型，**"Runoob"** 是 String 类型，而变量 a 是没有类型，她仅仅是一个对象的引用（一个指针），可以是指向 List 类型对象，也可以是指向 String 类型对象。

**可更改(mutable)与不可更改(immutable)对象**

在 python 中，strings, tuples, 和 numbers 是不可更改的对象，而 list,dict 等则是可以修改的对象。

- **不可变类型：** 变量赋值 **a=5** 后再赋值 **a=10**，这里实际是新生成一个 int 值对象 10，再让 a 指向它，而 5 被丢弃，不是改变 a 的值，相当于新生成了 a。 
- **可变类型：** 变量赋值 **la=[1,2,3,4]** 后再赋值 **la[2]=5** 则是将 list la 的第三个元素值更改，本身la没有动，只是其内部的一部分值被修改了。

python 中一切都是对象，严格意义我们不能说值传递还是引用传递，我们应该说传不可变对象和传可变对象。

**python 传不可变对象实例**

通过 **id()** 函数来查看内存地址变化：

```python
def change(a):  
    print(id(a), a)  # 指向的是同一个对象  
    a = 10  
    print(id(a), a)  # 一个新对象  
  
a = 1  
print(id(a), a)  
change(a)
```

输出结果

```python
4387152120 1
4387152120 1
4387152408 10
```

可以看见在调用函数前后，形参和实参指向的是同一个对象（对象 id 相同），在函数内部修改形参后，形参指向的是不同的 id。

**传可变对象实例**

可变对象在函数里修改了参数，那么在调用这个函数的函数里，原始的参数也被改变了。例如：

```python
#!/usr/bin/python3  
  
# 可写函数说明  
def changeme(mylist):  
    # 修改传入的列表  
    mylist.append([1, 2, 3, 4])  
    print("函数内取值: ", mylist)  
    return  
  
# 调用changeme函数  
mylist = [10, 20, 30]  
changeme(mylist)  
print("函数外取值: ", mylist)
```

传入函数的和在末尾添加新内容的对象用的是同一个引用。故输出结果如下：

```python
函数内取值:  [10, 20, 30, [1, 2, 3, 4]]
函数外取值:  [10, 20, 30, [1, 2, 3, 4]]
```

## 3. 作用域

作用域就是一个 Python 程序可以直接访问命名空间的正文区域。

在一个 python 程序中，直接访问一个变量，会从内到外依次访问所有的作用域直到找到，否则会报未定义的错误。

Python 中，程序的变量并不是在哪个位置都可以访问的，访问权限决定于这个变量是在哪里赋值的。

变量的作用域决定了在哪一部分程序可以访问哪个特定的变量名称。Python 的作用域一共有4种，分别是：

有四种作用域：

-   **L（Local）**：最内层，包含局部变量，比如一个函数/方法内部。
-   **E（Enclosing）**：包含了非局部(non-local)也非全局(non-global)的变量。比如两个嵌套函数，一个函数（或类） A 里面又包含了一个函数 B ，那么对于 B 中的名称来说 A 中的作用域就为 nonlocal。
-   **G（Global）**：当前脚本的最外层，比如当前模块的全局变量。
-   **B（Built-in）**： 包含了内建的变量/关键字等，最后被搜索。

规则顺序： **L –> E –> G –> B**。

在局部找不到，便会去局部外的局部找（例如闭包），再找不到就会去全局找，再者去内置中找。

```python
g_count = 0  # 全局作用域
def outer():
    o_count = 1  # 闭包函数外的函数中
    def inner():
        i_count = 2  # 局部作用域
```

内置作用域是通过一个名为 builtin 的标准模块来实现的，但是这个变量名自身并没有放入内置作用域内，所以必须导入这个文件才能够使用它。在Python3.0中，可以使用以下的代码来查看到底预定义了哪些变量:

```python
import builtins
dir(builtins)
```

Python 中只有模块（module），类（class）以及函数（def、lambda）才会引入新的作用域，其它的代码块（如 if/elif/else/、try/except、for/while等）是不会引入新的作用域的，也就是说这些语句内定义的变量，外部也可以访问，如下代码：

```python
>>> if True:
	msg = 'I am from Runoob'
>>> msg
	'I am from Runoob'
```

实例中 msg 变量定义在 if 语句块中，但外部还是可以访问的。

如果将 msg 定义在函数中，则它就是局部变量，外部不能访问：

```python
>>> def test():
     msg_inner = 'I am from Runoob'
>>> msg_inner
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'msg_inner' is not defined
```

从报错的信息上看，说明了 msg_inner 未定义，无法使用，因为它是局部变量，只有在函数内可以使用。

**6.4.1 全局变量和局部变量**

定义在函数内部的变量拥有一个局部作用域，定义在函数外的拥有全局作用域。

局部变量只能在其被声明的函数内部访问，而全局变量可以在整个程序范围内访问。调用函数时，所有在函数内声明的变量名称都将被加入到作用域中。如下实例：

```python
#!/usr/bin/python3  
  
total = 0  # 这是一个全局变量  
  
# 可写函数说明  
def sum(arg1, arg2):  
    # 返回2个参数的和."  
    total = arg1 + arg2  # total在这里是局部变量.  
    print("函数内是局部变量 : ", total)  
    return total  
  
# 调用sum函数  
sum(10, 20)  
print("函数外是全局变量 : ", total)
```

输出结果

```python
函数内是局部变量 :  30
函数外是全局变量 :  0
```

**6.4.2 global 和 nonlocal 关键字**

当内部作用域想修改外部作用域的变量时，就要用到 **global** 和 **nonlocal** 关键字了。

以下实例修改全局变量 num：

```python
#!/usr/bin/python3  
 
num = 1  
 

def fun1():  
    global num  # 需要使用 global 关键字声明  
    print(num)  
    num = 123  
    print(num)


fun1()  
print(num)
```

输出结果

```python
1
123
123
```

如果要修改嵌套作用域（enclosing 作用域，外层非全局作用域）中的变量则需要 **nonlocal** 关键字了，如下实例：

```python
#!/usr/bin/python3  
  
def outer():  
    num = 10  
  
    def inner():  
        nonlocal num  # nonlocal关键字声明  
        num = 100  
        print(num)  
  
    inner()  
    print(num)  
  
  
outer()
```

输出结果

```python
100
100
```

另外有一种特殊情况，假设下面这段代码被运行：

```python
#!/usr/bin/python3 a = 10 def test(): a = a + 1 print(a) test()
```

报错信息如下

```python
Traceback (most recent call last):
  File "test.py", line 7, in <module>
    test()
  File "test.py", line 5, in test
    a = a + 1
UnboundLocalError: local variable 'a' referenced before assignment
```

错误信息为局部作用域引用错误，因为 test 函数中的 a 使用的是局部，未定义，无法修改。

修改 a 为全局变量即可运行：

```python
#!/usr/bin/python3  
  
a = 10  
  
  
def test():  
    global a  
    a = a + 1  
    print(a)  
  
  
test()
```

也可以通过函数参数传递：

```python
#!/usr/bin/python3  
  
a = 10  
  
  
def test(a):  
    a = a + 1  
    print(a)  
  
  
test(a)
```

## 4. lambda 表达式

lambda 表达式，又称匿名函数，常用来表示内部仅包含 1 行表达式的函数。如果一个函数的函数体仅有 1 行表达式，则该函数就可以用 lambda 表达式来代替。

lambda 表达式的语法格式如下：

```python
name = lambda [list] : 表达式
```

其中，定义 lambda 表达式，必须使用 lambda 关键字；[list] 作为可选参数，等同于定义函数是指定的参数列表；value 为该表达式的名称。

该语法格式转换成普通函数的形式，如下所示：

```python
def name(list):
    return 表达式
name(list)
```

> 显然，使用普通方法定义此函数，需要 3 行代码，而使用 lambda 表达式仅需 1 行。

举个例子，如果设计一个求 2 个数之和的函数，使用普通函数的方式，定义如下：

```python
def add(x, y):
    return x+ y
print(add(3,4))
```

由于上面程序中，add() 函数内部仅有 1 行表达式，因此该函数可以直接用 lambda 表达式表示：

```python
add = lambda x,y:x+y
print(add(3,4))
```

可以这样理解 lambda 表达式，其就是简单函数（函数体仅是单行的表达式）的简写版本。相比函数，lamba 表达式具有以下  2 个优势：

-   对于单行函数，使用 lambda 表达式可以省去定义函数的过程，让代码更加简洁；
-   对于不需要多次复用的函数，使用 lambda 表达式可以在用完之后立即释放，提高程序执行的性能。

> 下面是 [菜鸟教程](https://www.runoob.com/python/python-functions.html) 对 lambda 函数的说明

Python 使用 lambda 来创建匿名函数。

所谓匿名，意即不再使用 **def** 语句这样标准的形式定义一个函数。

-   lambda 只是一个表达式，函数体比 **def** 简单很多。
-   lambda 的主体是一个表达式，而不是一个代码块。仅仅能在 lambda 表达式中封装有限的逻辑进去。
-   lambda 函数拥有自己的命名空间，且不能访问自己参数列表之外或全局命名空间里的参数。
-   虽然 lambda 函数看起来只能写一行，却不等同于 C 或 C++ 的内联函数，后者的目的是调用小函数时不占用栈内存从而增加运行效率。

**语法**

lambda 函数的语法只包含一个语句，如下：

```python
lambda [arg1 [,arg2,.....argn]]:expression
```

设置参数 a 加上 10:

```python
x = lambda a : a + 10  
print(x(5))
```

输出结果

```python
15
```

以下实例匿名函数设置两个参数：

```python
#!/usr/bin/python3  
  
# 可写函数说明  
sum = lambda arg1, arg2: arg1 + arg2  
  
# 调用sum函数  
print("相加后的值为 : ", sum(10, 20))  
print("相加后的值为 : ", sum(20, 20))
```

输出结果

```python
相加后的值为 :  30
相加后的值为 :  40
```

我们可以将匿名函数封装在一个函数内，这样可以使用同样的代码来创建多个匿名函数。

以下实例将匿名函数封装在 myfunc 函数中，通过传入不同的参数来创建不同的匿名函数：

```python
def myfunc(n):  
    return lambda a: a * n  
  
  
mydoubler = myfunc(2)  
mytripler = myfunc(3)  
  
print(mydoubler(11))  
print(mytripler(11))
```

输出结果

```python
22
33
```

## 5 内置函数

- 相关链接
	- [Python3 内置函数 | 菜鸟教程](https://www.runoob.com/python3/python3-built-in-functions.html)
	- [Python 内置函数](https://www.w3schools.cn/python/python_ref_functions.asp)

# 第六章 ython 面向对象

> Python 面向对象, 建议先去 菜鸟教程, w3schools, 廖雪峰博客 粗略的学习,梳理基础概念

## 0. 引言

- 相关链接
	- [面向对象编程 - 廖雪峰的官方网站](https://www.liaoxuefeng.com/wiki/1016959663602400/1017495723838528)

面向对象编程——Object Oriented Programming，简称OOP，是一种程序设计思想。OOP把对象作为程序的基本单元，一个对象包含了数据和操作数据的函数。

面向过程的程序设计把计算机程序视为一系列的命令集合，即一组函数的顺序执行。为了简化程序设计，面向过程把函数继续切分为子函数，即把大块函数通过切割成小块函数来降低系统的复杂度。

而面向对象的程序设计把计算机程序视为一组对象的集合，而每个对象都可以接收其他对象发过来的消息，并处理这些消息，计算机程序的执行就是一系列消息在各个对象之间传递。

在Python中，所有数据类型都可以视为对象，当然也可以自定义对象。自定义的对象数据类型就是面向对象中的类（Class）的概念。

我们以一个例子来说明面向过程和面向对象在程序流程上的不同之处。

```python
# 假设我们要处理学生的成绩表，为了表示一个学生的成绩，面向过程的程序可以用一个dict表示：  
std1 = { 'name': 'Michael', 'score': 98 }  
std2 = { 'name': 'Bob', 'score': 81 }  
  
  
# 而处理学生成绩可以通过函数实现，比如打印学生的成绩：  
def print_score(std):  
    print('%s: %s' % (std['name'], std['score']))  
  
  
print_score(std1)
```

输出结果

```python
Michael: 98
```

如果采用面向对象的程序设计思想，我们首选思考的不是程序的执行流程，而是 `Student` 这种数据类型应该被视为一个对象，这个对象拥有 `name` 和 `score` 这两个属性（Property）。如果要打印一个学生的成绩，首先必须创建出这个学生对应的对象，然后，给对象发一个 `print_score` 消息，让对象自己把自己的数据打印出来。

**通过类创建对象**

```python
class Student(object):

    def __init__(self, name, score):
        self.name = name
        self.score = score

    def print_score(self):
        print('%s: %s' % (self.name, self.score))
```

给对象发消息实际上就是调用对象对应的关联函数，我们称之为对象的方法（Method）。面向对象的程序写出来就像这样：

```python
bart = Student('Bart Simpson', 59)
lisa = Student('Lisa Simpson', 87)
bart.print_score()
lisa.print_score()
```

面向对象的设计思想是从自然界中来的，因为在自然界中，类（Class）和实例（Instance）的概念是很自然的。Class是一种抽象概念，比如我们定义的Class——Student，是指学生这个概念，而实例（Instance）则是一个个具体的Student，比如，Bart Simpson和Lisa Simpson是两个具体的Student。

所以，面向对象的设计思想是抽象出Class，根据Class创建Instance。

面向对象的抽象程度又比函数要高，因为一个Class既包含数据，又包含操作数据的方法。

## 1. 类和对象

### 1.1 定义类

定义类时, 使用 `class` 关键字, 格式如下:

```python
class 类名：  
    多个（≥0）类属性...  
    多个（≥0）类方法...
```

注意，无论是类属性还是类方法，对于类来说，它们都不是必需的，可以有也可以没有。另外，Python 类中属性和方法所在的位置是任意的，即它们之间并没有固定的前后次序。

和变量名一样，类名本质上就是一个**标识符**，因此我们在给类起名字时，必须让其符合 Python 的语法。有读者可能会问，用 a、b、c 作为类的类名可以吗？从 Python 语法上讲，是完全没有问题的，但作为一名合格的程序员，我们必须还要考虑程序的可读性。

因此，在给类起名字时，最好使用能代表该类功能的单词，例如用“Student”作为学生类的类名；甚至如果必要，可以使用多个单词组合而成，例如初学者定义的第一个类的类名可以是“TheFirstDemo”。

> 注意，如果由单词构成类名，建议每个单词的首字母大写，其它字母小写。

给类起好名字之后，其后要跟有冒号 ":" ，表示告诉 Python 解释器，下面要开始设计类的内部功能了，也就是编写类属性和类方法。

其实，**类属性**指的就是包含在类中的**变量**；而**类方法**指的是包含类中的**函数**。换句话说，类属性和类方法其实分别是包含类中的变量和函数的别称。需要注意的一点是，同属一个类的所有类属性和类方法，要保持统一的缩进格式，通常统一缩进 4 个空格。

通过上面的分析，可以得出这样一个结论，即 Python 类是由类头（class 类名）和类体（统一缩进的变量和函数）构成。例如，下面程序定义一个 TheFirstDemo 类：

```python
class TheFirstDemo:
    '''这是一个学习Python定义的第一个类'''
    # 下面定义了一个类属性
    add = 'http://c.biancheng.net'
    # 下面定义了一个say方法
    def say(self, content):
        print(content)
```

和函数一样，我们也可以为类定义说明文档，其要放到类头之后，类体之前的位置，如上面程序中第二行的字符串，就是 TheFirstDemo 这个类的说明文档。

另外分析上面的代码可以看到，我们创建了一个名为 `TheFirstDemo` 的**类**，其包含了一个名为 `add` 的**类属性**。注意，根据定义属性位置的不同，在各个类方法之外定义的变量称为类属性或类变量（如 add 属性），而在类方法中定义的属性称为实例属性（或实例变量），它们的区别和用法可阅读《[Python类变量和实例变量](http://c.biancheng.net/view/2283.html)》一节。

同时，TheFirstDemo 类中还包含一个 say() 类方法，细心的读者可能已经看到，该方法包含两个参数，分别是 self 和 content。可以肯定的是，content 参数就只是一个普通参数，没有特殊含义，但 self 比较特殊，并不是普通的参数，它的作用会在后续章节中详细介绍。

> 更确切地说，say() 是一个实例方法，除此之外，Python 类中还可以定义类方法和静态方法，这 3 种类方法的区别和具体用法，可阅读《[Python实例方法、静态方法和类方法](http://c.biancheng.net/view/4552.html)》。


事实上，我们完全可以创建一个没有任何类属性和类方法的类，换句话说，Python 允许创建空类，例如：

```python
class Empty:
    pass
```

可以看到，如果一个类没有任何类属性和类方法，那么可以直接用 pass 关键字作为类体即可。但在实际应用中，很少会创建空类，因为空类没有任何实际意义。

### 1.2 __init__()类构造方法

在创建类时，我们可以手动添加一个` __init__()` 方法，该方法是一个特殊的类实例方法，称为**构造方法**（或构造函数）。

构造方法用于创建对象时使用，每当创建一个类的实例对象时，Python 解释器都会自动调用它。Python 类中，手动添加构造方法的语法格式如下：

```python
def __init__(self,...):  
    代码块
```

注意，此方法的方法名中，开头和结尾各有 2 个下划线，且中间不能有空格。Python 中很多这种以双下划线开头、双下划线结尾的方法，都具有特殊的意义

另外，`__init__()` 方法可以包含多个参数，但必须包含一个名为 self 的参数，且必须作为第一个参数。也就是说，类的构造方法最少也要有一个 self 参数。例如，仍以 TheFirstDemo 类为例，添加构造方法的代码如下所示：

```python
class TheFirstDemo:
    '''这是一个学习Python定义的第一个类'''
    
    #构造方法
    def __init__(self):
        print("调用构造方法")
        
    # 下面定义了一个类属性
    add = 'http://c.biancheng.net'
    
    # 下面定义了一个say方法
    def say(self, content):
        print(content)
```

注意，即便不手动为类添加任何构造方法，Python 也会自动为类添加一个仅包含 self 参数的构造方法。

> 仅包含 self 参数的 `__init__()  **构造方法**，又称为类的**默认构造方法**。

在上面代码的后面，顶头（不缩进）直接添加如下代码：

```python
zhangsan = TheFirstDemo()
```

这行代码的含义是创建一个名为 zhangsan 的 TheFirstDemo 类对象。运行代码可看到如下结果：

```python
调用构造方法
```

显然，在创建 zhangsan 这个对象时，隐式调用了我们手动创建的 __init__() 构造方法。

不仅如此，在 __init__() 构造方法中，除了 self 参数外，还可以自定义一些参数，参数之间使用逗号“,”进行分割。例如，下面的代码在创建 __init__() 方法时，额外指定了 2 个参数：

```python
class SayHello:
    '''这是一个学习Python定义的一个类'''
	
	# 这里的 *name 是巩固前面知识点, 可以省略
	# 下面则修改为 add = SayHello("09:26", "Kylin")
    def __init__(self,time,*name):
        print(time,"Hello, ",name)
		
#创建 add 对象，并传递参数给构造函数
add = SayHello("09:26","Kylin", 'Bob')
```

注意，由于创建对象时会调用类的构造方法，如果构造函数有多个参数时，需要手动传递参数，传递方式如代码中所示

输出结果

```python
09:26 Hello,  ('Kylin', 'Bob')
```

可以看到，虽然构造方法中有 self、name、add 3 个参数，但实际需要传参的仅有 name 和 add，也就是说，self 不需要手动传递参数。

> 就创建类对象来说，此时无需给 self 传参即可。

### 1.3 类对象的创建使用

#### 1.3.1 Python类的实例化

对已定义好的类进行实例化，其语法格式如下：

```python
类名(参数)
```

定义类时，如果没有手动添加 `__init__()` 构造方法，又或者添加的 `__init__()` 中仅有一个 self 参数，则创建类对象时的参数可以省略不写。

例如，如下代码创建了名为 CLanguage 的类，并对其进行了实例化：

```python
class CLanguage :
    # 下面定义了2个类变量
    name = "C语言中文网"
    add = "http://c.biancheng.net"
    def __init__(self,name,add):
        #下面定义 2 个实例变量
        self.name = name
        self.add = add
        print(name,"网址为：",add)
    # 下面定义了一个say实例方法
    def say(self, content):
        print(content)
# 将该CLanguage对象赋给clanguage变量
clanguage = CLanguage("C语言中文网","http://c.biancheng.net")
```

输出结果

```python
C语言中文网 网址为： http://c.biancheng.net
```

在上面的程序中，由于构造方法除 self 参数外，还包含 2 个参数，且这 2 个参数没有设置默认参数，因此在实例化类对象时，需要传入相应的 name 值和 add 值（self 参数是特殊参数，不需要手动传值，Python 会自动传给它值）。

> 类变量和实例变量，简单地理解，定义在各个类方法之外（包含在类中）的变量为类变量（或者类属性），定义在类方法中的变量为实例变量（或者实例属性）

#### 1.3.2 Python类对象的使用

定义的类只有进行实例化，也就是使用该类创建对象之后，才能得到利用。总的来说，实例化后的类对象可以执行以下操作：

-   访问或修改类对象具有的实例变量，甚至可以添加新的实例变量或者删除已有的实例变量；
-   调用类对象的方法，包括调用现有的方法，以及给类对象动态添加方法。

##### (1) 类对象访问变量或方法

使用已创建好的类对象访问类中实例变量的语法格式如下：

```python
类对象名.变量名
```

使用类对象调用类中方法的语法格式如下：

```python
对象名.方法名(参数)
```

注意，对象名和变量名以及方法名之间用点 "." 连接。

例如，下面代码演示了如何通过 a 对象调用类中的实例变量和方法：

```python
class FirstClass :  
    # 下面定义了2个类变量  
    name = "Kylin"  
    age = "50"  
  
    def __init__(self,name,age):  
        #下面定义 2 个实例变量  
        self.name = name  
        self.age = age  
        print(name,"Age is：",age)  
  
    # 下面定义了一个say实例方法  
    def say(self, content):  
        print(content)  
  
# 将该 FirstClass 对象赋给 a 变量  
a = FirstClass("Kylin","50")  
  
#输出 name 和 age 实例变量的值  
print(a.name,a.age)  
  
#修改实例变量的值  
a.name = "Kylin"  
a.age = "18"  
  
#调用 a 的say()方法  
a.say("人生苦短, 我用Python, 重返 18")  
  
#再次输出 name 和 age 的值  
print(a.name,a.age)
```

输出结果

```python
Kylin Age is： 50
Kylin 50
人生苦短，我用Python, 重返 18
Kylin 18
```

##### (2) 给类对象动态添加/删除变量

Python 支持为已创建好的对象动态增加实例变量，方法也很简单，举个例子：

```python
class FirstClass:  
    name = 'kylin'  
    age = '18'  
  
# 为clanguage对象增加一个money实例变量  
FirstClass.money = 159.9  
print(FirstClass.name, FirstClass.age, FirstClass.money)
```

输出结果

```python
kylin 18 159.9
```

可以看到，通过直接增加一个新的实例变量并为其赋值，就成功地为 FirstClass 对象添加了 money 变量。

既然能动态添加，那么是否能动态删除呢？答案是肯定的，使用 del 语句即可实现，例如：

```python
#删除新添加的 money 实例变量
del FirstClass.money
#再次尝试输出 money，此时会报错
print(FirstClass.money)
```

```python
Traceback (most recent call last):  
  File "[Local_Path]", line [Number of rows], in <module>  
    print(FirstClass.money)  
AttributeError: 'FirstClass' object has no attribute 'money'
```

##### (3) 给类对象动态添加方法

> 注意，初学者在理解下面内容之前，需明白 self 参数的含义和作用，可参考 [[6. Python 面向对象#2 1 1 self]] 理解

Python 也允许为对象动态增加方法。以 FirstClass 类为例，由于其内部只包含一个 say() 方法，因此该类实例化出的 clanguage 对象也只包含一个 say() 方法。但其实，我们还可以为 clanguage 对象动态添加其它方法。

需要注意的一点是，为 FirstClass 对象动态增加的方法，Python 不会自动将调用者自动绑定到第一个参数（即使将第一个参数命名为 self 也没用）。例如如下代码：

```python
class FirstClass :  
    name = "Kylin"  
    age = "50"  
  
    def __init__(self,name,age):  
        self.name = name  
        self.age = age  
        print(name,"Age is：",age)  
  
    # 下面定义了一个say实例方法  
    def say(self, content):  
        print(content)  

a = FirstClass("Kylin","50")

# 先定义一个函数
def info(self):
    print("---info函数---", self)

# 分别使用函数、lambda 表达式为 FirstClass 对象动态增加方法

# 1. 使用 info 对 a 的 foo 方法赋值（动态绑定方法）
a.foo = info

# Python不会自动将调用者绑定到第一个参数,
# 因此程序需要手动将调用者绑定为第一个参数
a.foo(a) # ①

# 2. 使用 lambda 表达式为 a 对象的 bar 方法赋值（动态绑定方法）
a.bar = lambda self: print('--lambda表达式--', self)
a.bar(a) # ②
```

输出结果

```python
---info函数--- <__main__.FirstClass object at 0x102a4e310>
--lambda表达式-- <__main__.FirstClass object at 0x102a4e310>
```

对于动态增加的方法，Python 不会自动将方法调用者绑定到它们的第一个参数，因此程序必须手动为第一个参数传入参数值，如上面程序中 ① 号、② 号代码所示。

通过借助 types 模块下的 MethodType 可以实现不用手动给 self 传值的方法，仍以上面的 info() 函数为例：

```python
class FirstClass:  
    name = "Kylin"  
    age = "50"  
  
    def __init__(self, name, age):  
        self.name = name  
        self.age = age  
        print(name, "Age is：", age)  
  
    # 下面定义了一个say实例方法  
    def say(self, content):  
        print(content)  
  
a = FirstClass("Kylin", "50")  
  
def info(self,content):  
    print("Hello, %s" % content)  
  
# 导入 MethodTypefrom types import MethodType  
a.info = MethodType(info, a)  
  
# 第一个参数已经绑定了，无需传入  
a.info("Kylin")
```

输出结果

```python
Hello, Kylin
```

可以看到，由于使用 MethodType 包装 info() 函数时，已经将该函数的 self 参数绑定为 clanguage，因此后续再使用 info() 函数时，就不用再给 self 参数绑定值了。

## 2. 类的三大特性

### 2.1 封装

#### 2.1.1 self

在定义类的过程中，无论是显式创建类的构造方法，还是向类中添加实例方法，都要求将 self 参数作为方法的第一个参数。例如，定义一个 Person 类：

```python
class Person:
    def __init__(self):
        print("正在执行构造方法")
        
    # 定义一个study()实例方法
    def study(self,name):
        print(name,"正在学Python")
```

那么，self 到底扮演着什么样的角色呢？本节就对 self 参数做详细的介绍。

事实上，Python 只是规定，无论是构造方法还是实例方法，最少要包含一个参数，并没有规定该参数的具体名称。之所以将其命名为 self，只是程序员之间约定俗成的一种习惯，遵守这个约定，可以使我们编写的代码具有更好的可读性（大家一看到 self，就知道它的作用）。

那么，self 参数的具体作用是什么呢？打个比方，如果把类比作造房子的图纸，那么类实例化后的对象是真正可以住的房子。根据一张图纸（类），我们可以设计出成千上万的房子（类对象），每个房子长相都是类似的（都有相同的类变量和类方法），但它们都有各自的主人，那么如何对它们进行区分呢？

当然是通过 self 参数，它就相当于每个房子的门钥匙，可以保证每个房子的主人仅能进入自己的房子（每个类对象只能调用自己的类变量和类方法）。

> 如果你接触过其他面向对象的编程语言（例如 [C++](http://c.biancheng.net/cplus/)），其实 Python 类方法中的 self 参数就相当于 C++ 中的 this 指针。

也就是说，同一个类可以产生多个对象，当某个对象调用类方法时，该对象会把自身的引用作为第一个参数自动传给该方法，换句话说，Python 会自动绑定类方法的第一个参数指向调用该方法的对象。如此，Python解释器就能知道到底要操作哪个对象的方法了。

因此，程序在调用实例方法和构造方法时，不需要手动为第一个参数传值。例如，更改前面的 Person 类，如下所示：

```python
class Person:
    def __init__(self):
        print("正在执行构造方法")
    # 定义一个study()实例方法
    def study(self):
        print(self,"正在学Python")
zhangsan = Person()
zhangsan.study()
lisi = Person()
lisi.study()
```

上面代码中，study() 中的 self 代表该方法的调用者，即谁调用该方法，那么 self 就代表谁。因此，该程序的输出结果为：

```python
正在执行构造方法  
<__main__.Person object at 0x0000021ADD7D21D0> 正在学Python  
正在执行构造方法  
<__main__.Person object at 0x0000021ADD7D2E48> 正在学Python
```

另外，对于构造函数中的 self 参数，其代表的是当前正在初始化的类对象。举个例子：

```python
class Person:
    name = "xxx"
    def __init__(self,name):
        self.name=name
        
zhangsan = Person("zhangsan")
print(zhangsan.name)
lisi = Person("lisi")
print(lisi.name)
```

输出结果

```python
zhangsan
lisi
```

可以看到，zhangsan 在进行初始化时，调用的构造函数中 self 代表的是 zhangsan；而 lisi 在进行初始化时，调用的构造函数中 self 代表的是 lisi。

值得一提的是，除了类对象可以直接调用类方法，还有一种函数调用的方式，例如：

```python
class Person:
    def who(self):
        print(self)
        
zhangsan = Person()

#第一种方式
zhangsan.who()

#第二种方式
who = zhangsan.who
who()#通过 who 变量调用zhangsan对象中的 who() 方法
```

输出结果

```python
<__main__.Person object at 0x105316310>
<__main__.Person object at 0x105316310>
```

显然，无论采用哪种方法，self 所表示的都是实际调用该方法的对象。

> 无论是类中的构造函数还是普通的类方法，实际调用它们的谁，则第一个参数 self 就代表谁。

#### 2.1.2 属性

无论是类属性还是类方法，都无法像普通变量或者函数那样，在类的外部直接使用它们。我们可以将类看做一个独立的空间，则类属性其实就是在类体中定义的变量，类方法是在类体中定义的函数。

前面章节提到过，在类体中，根据变量定义的位置不同，以及定义的方式不同，类属性又可细分为以下 3 种类型：

1.  类体中、所有函数之外：此范围定义的变量，称为类属性或类变量；
2.  类体中，所有函数内部：以“self.变量名”的方式定义的变量，称为实例属性或实例变量；
3.  类体中，所有函数内部：以“变量名=变量值”的方式定义的变量，称为局部变量。

> 不仅如此，类方法也可细分为实例方法、静态方法和类方法，后续章节会做详细介绍。

那么，类变量、实例变量以及局部变量之间有哪些不同呢？接下来就围绕此问题做详细地讲解。

##### (1) 类属性 (类变量)

类变量指的是在类中，但在各个类方法外定义的变量。举个例子：

```python
class Classmate:
    # 下面定义了2个类变量
    name = "小明"
    age = "11"
    # 下面定义了一个say实例方法
    def say(self, content):
        print(content)
```

上面程序中，name 和 age 就属于类变量。

类变量的特点是，**所有类的实例化对象都同时共享类变量**，也就是说，类变量在所有实例化对象中是作为公用资源存在的。类方法的调用方式有 2 种，既可以使用类名直接调用，也可以使用类的实例化对象调用。

比如，在 Classmate 类的外部，添加如下代码：

```python
#使用类名直接调用
print(Classmate.name)
print(Classmate.age)
#修改类变量的值
Classmate.name = "小红"
Classmate.age = "12"
print(Classmate.name)
print(Classmate.age)
```

输出结果

```python
小明
11
小红
12
```

可以看到，通过类名不仅可以调用类变量，也可以修改它的值。

当然，也可以使用类对象来调用所属类中的类变量（此方式不推荐使用，原因后续会讲）。例如，在 Classmate 类的外部，添加如下代码：

```python
people = Classmate()
print(people.name)
print(people.age)
```

输出结果

```python
小明
11
```

注意，因为类变量为所有实例化对象共有，通过类名修改类变量的值，会影响所有的实例化对象。例如，在 Classmate 类体外部，添加如下代码：

```python
# 修改前
print("修改前，各类对象中类变量的值：")
people1 = Classmate()
print(people1.name)
print(people1.age)
people2 = Classmate()
print(people2.name)
print(people2.age)

# 修改后
print("修改后，各类对象中类变量的值：")
Classmate.name = "小红"
Classmate.add = "13"
print(people1.name)
print(people1.add)
print(people2.name)
print(people2.add)
```

输出结果

```python
修改前，各类对象中类变量的值：
小明
11
小明
11
修改后，各类对象中类变量的值：
小红
13
小红
13
```

显然，通过类名修改类变量，会作用到所有的实例化对象（例如这里的 people1 和 people2）。

> 注意，通过类对象是无法修改类变量的。通过类对象对类变量赋值，其本质将不再是修改类变量的值，而是在给该对象定义新的实例变量（在讲实例变量时会进行详细介绍）。

值得一提的是，除了可以通过类名访问类变量之外，还可以动态地为类和对象添加类变量。例如，在 Classmate 类的基础上，添加以下代码：

```python
clang = Classmate()
Classmate.like = "唱跳rap"
Classmate.name = "小菜"
print(clang.name)
print(clang.age)
print(clang.like)
```

输出结果

```python
小菜
11
唱跳rap
```

##### (2) 实例属性 (实例变量)

实例变量指的是在任意类方法内部，以“self.变量名”的方式定义的变量，其特点是只作用于调用方法的对象。另外，实例变量只能通过对象名访问，无法通过类名访问。

```python
class Classmate :
    def __init__(self):
        self.name = "小菜"
        self.age = "3"
    # 下面定义了一个say实例方法
    def say(self):
        self.like = "唱跳rap"
```

此 Classmate 类中，name、age 以及 like 都是实例变量。其中，由于 __init__() 函数在创建类对象时会自动调用，而 say() 方法需要类对象手动调用。因此，Classmate 类的类对象都会包含 name 和 age 实例变量，而只有调用了 say() 方法的类对象，才包含 like 实例变量。

例如，在上面代码的基础上，添加如下语句：

```python
people1 = Classmate()  
print(people1.name)  
print(people1.age)  
#由于 people1 对象未调用 say() 方法，因此其没有 like 变量，下面这行代码会报错  
#print(clang.catalog)  
people2 = Classmate()  
print(people2.name)  
print(people2.age)  
#只有调用 say()，才会拥有 like 实例变量  
people2.say()  
print(people2.like)
```

输出结果

```python
小菜
3
小菜
3
唱跳rap
```

前面讲过，通过类对象可以访问类变量，但无法修改类变量的值。这是因为，通过类对象修改类变量的值，不是在给“类变量赋值”，而是定义新的实例变量。例如，在 Classmate 类体外，添加如下程序：

```python
class Classmate :  
    name = "小菜"  
    age = "3"  
  
people = Classmate()  
# people 访问类变量  
print(people.name)  
print(people.age)  
people.name = "小明"  
people.age = "11"  
  
# people 实例变量的值  
print(people.name)  
print(people.age)  
  
#类变量的值  
print(Classmate.name)  
print(Classmate.age)
```

输出结果

```python
小菜
3
小明
11
小菜
3
```

显然，通过类对象是无法修改类变量的值的，本质其实是给 clang 对象新添加 name 和 add 这 2 个实例变量。

> 类中，实例变量和类变量可以同名，但这种情况下使用类对象将无法调用类变量，它会首选实例变量，这也是不推荐“类变量使用对象名调用”的原因。

另外，和类变量不同，通过某个对象修改实例变量的值，不会影响类的其它实例化对象，更不会影响同名的类变量。例如：

```python
class Classmate :  
    name = "小菜"  #类变量  
    age = "3"  #类变量  
  
    def __init__(self):  
        self.name = "小明"   #实例变量  
        self.age = "11"   #实例变量  
  
    # 下面定义了一个say实例方法  
    def say(self):  
        self.like = "唱跳rap"  #实例变量  
  
people1 = Classmate()  
  
#修改 people1 对象的实例变量  
people1.name = "小红"  
people1.age = "12"  
print(people1.name)  
print(people1.age)  
  
people2 = Classmate()  
print(people2.name)  
print(people2.age)  
  
#输出类变量的值  
print("没想到吧, 还是我")  
print(Classmate.name)  
print(Classmate.age)
```

输出结果

```python
小红
12
小明
11
没想到吧, 还是我
小菜
3
```

不仅如此，Python 只支持为特定的对象添加实例变量。例如，在之前代码的基础上，为 people1 对象添加 money 实例变量，实现代码为：

```python
people1.money = 30
print(people1.money)
```

##### (3) 局部变量

除了实例变量，类方法中还可以定义局部变量。和前者不同，局部变量直接以“变量名=值”的方式进行定义，例如：

```python
class Discount:  
    # 下面定义了一个 half_fare 半价折扣实例方法  
    def half_fare(self, money):  
        result = 0.5 * money  
        print("优惠后的价格为：", result)  
  
  
money = Discount()  
# 计算 100 的折扣价  
money.half_fare(100)
```

输出结果

```python
优惠后的价格为： 50.0
```

通常情况下，定义局部变量是为了所在类方法功能的实现。需要注意的一点是，局部变量只能用于所在函数中，函数执行完成后，局部变量也会被销毁。

---

由于Python是动态语言，根据类创建的实例可以任意绑定属性。

给实例绑定属性的方法是通过实例变量，或者通过`self`变量：

```python
class Student(object):
    def __init__(self, name):
        self.name = name

s = Student('Bob')
s.score = 90
```

但是，如果`Student`类本身需要绑定一个属性呢？可以直接在class中定义属性，这种属性是类属性，归`Student`类所有：

```python
class Student(object):
    name = 'Student'
```

当我们定义了一个类属性后，这个属性虽然归类所有，但类的所有实例都可以访问到。来测试一下：

```python
>>> class Student(object):
...     name = 'Student'
...
>>> s = Student() # 创建实例s
>>> print(s.name) # 打印name属性，因为实例并没有name属性，所以会继续查找class的name属性
Student
>>> print(Student.name) # 打印类的name属性
Student
>>> s.name = 'Michael' # 给实例绑定name属性
>>> print(s.name) # 由于实例属性优先级比类属性高，因此，它会屏蔽掉类的name属性
Michael
>>> print(Student.name) # 但是类属性并未消失，用Student.name仍然可以访问
Student
>>> del s.name # 如果删除实例的name属性
>>> print(s.name) # 再次调用s.name，由于实例的name属性没有找到，类的name属性就显示出来了
Student
```

从上面的例子可以看出，在编写程序的时候，千万不要对实例属性和类属性使用相同的名字，因为相同名称的实例属性将屏蔽掉类属性，但是当你删除实例属性后，再使用相同的名称，访问到的将是类属性。

---

**修改对象属性**

```python
# 创建 Person 类, 使用 __init__() 函数赋值  
class Person():  
    def __init__(self, name, age):  
        self.name = name  
        self.age = age  
  
    def myfunc(self):  
        print("My name is: ", self.name)  
        print("My age is: ", self.age)  

# 实例化 p1 并传入参数 'kylin' 和 11
p1 = Person("kylin", 11)  
p1.myfunc()  

# 修 p1 对象 age 属性为 40
p1.age = 40  

p1.myfunc()
```

输出结果

```python
My name is:  kylin
My age is:  11
My name is:  kylin
My age is:  40
```

**删除对象属性**

```python
del p1.age
```

**删除对象**

```python
del p1
```

#### 2.1.3 方法

##### (1) 类实例方法

通常情况下，在类中定义的方法默认都是实例方法。前面章节中，我们已经定义了不只一个实例方法。不仅如此，类的构造方法理论上也属于实例方法，只不过它比较特殊。

比如，下面的类中就用到了实例方法：

```python
class CLanguage:
    #类构造方法，也属于实例方法
    def __init__(self):
        self.name = "C语言中文网"
        self.add = "http://c.biancheng.net"
    # 下面定义了一个say实例方法
    def say(self):
        print("正在调用 say() 实例方法")
```

实例方法最大的特点就是，它最少也要包含一个 self 参数，用于绑定调用此方法的实例对象（Python 会自动完成绑定）。实例方法通常会用类对象直接调用，例如：

```python
clang = CLanguage()
clang.say()
```

输出结果

```python
正在调用 say() 实例方法
```

> 有关使用类名直接调用实例方法的更多介绍，可阅读《[Python类调用实例方法](http://c.biancheng.net/view/2267.html)》一节。

##### (2) 类方法

Python 类方法和实例方法相似，它最少也要包含一个参数，只不过类方法中通常将其命名为 cls，Python 会自动将类本身绑定给 cls 参数（注意，绑定的不是类对象）。也就是说，我们在调用类方法时，无需显式为 cls 参数传参。

> 和 self 一样，cls 参数的命名也不是规定的（可以随意命名），只是 Python 程序员约定俗称的习惯而已。

```python
class CLanguage:
    #类构造方法，也属于实例方法
    def __init__(self):
        self.name = "C语言中文网"
        self.add = "http://c.biancheng.net"
    #下面定义了一个类方法
    @classmethod
    def info(cls):
        print("正在调用类方法",cls)
```

> 注意，如果没有 ＠classmethod，则 Python 解释器会将 fly() 方法认定为实例方法，而不是类方法。

类方法推荐使用类名直接调用，当然也可以使用实例对象来调用（**不推荐**）。例如，在上面 CLanguage 类的基础上，在该类外部添加如下代码：

```python
#使用类名直接调用类方法
CLanguage.info()
#使用类对象调用类方法
clang = CLanguage()
clang.info()
```

输出结果

```python
正在调用类方法 <class '__main__.CLanguage'>
正在调用类方法 <class '__main__.CLanguage'>
```

##### (3) 静态方法

静态方法，其实就是我们学过的函数，和函数唯一的区别是，静态方法定义在类这个空间（类命名空间）中，而函数则定义在程序所在的空间（全局命名空间）中。

静态方法没有类似 self、cls 这样的特殊参数，因此 Python 解释器不会对它包含的参数做任何类或对象的绑定。也正因为如此，类的静态方法中无法调用任何类属性和类方法。

静态方法需要使用`＠staticmethod`修饰，例如：

```python
class CLanguage:
    @staticmethod
    def info(name,add):
        print(name,add)
```

静态方法的调用，既可以使用类名，也可以使用类对象，例如：

```python
#使用类名直接调用静态方法  
CLanguage.info("Hello","Kylin")  
  
#使用类对象调用静态方法  
clang = CLanguage()  
clang.info("Hello","Python")
```

输出结果

```python
Hello Kylin
Hello Python
```

在实际编程中，几乎不会用到类方法和静态方法，因为我们完全可以使用函数代替它们实现想要的功能，但在一些特殊的场景中（例如工厂模式中），使用类方法和静态方法也是很不错的选择。

##### (4) 类的专有方法

- `__init__` : 构造函数，在生成对象时调用
- `__del__` : 析构函数，释放对象时使用
- `__repr__` : 打印，转换
- `__setitem__` : 按照索引赋值
- `__getitem__`: 按照索引获取值
- `__len__`: 获得长度
- `__cmp__`: 比较运算
- `__call__`: 函数调用
- `__add__`: 加运算
- `__sub__`: 减运算
- `__mul__`: 乘运算
- `__truediv__`: 除运算
- `__mod__`: 求余运算
- `__pow__`: 乘方

类的专有方法可能会运用在 [[6. Python 面向对象#3 运算符重载]]

##### (5) 方法小结

- 相关链接
	- [Python系列教程（四十）：类的多种方法和属性访问控制 – Jimmy's Blog](https://www.xjimmy.com/python-40-class2.html)

1、实例方法: 它的第一个参数必然是self，由实例对象调用的方法，用的是最多也是这种方法。

2、类方法: 不同于普通方法，有一定的应用场景，具体有如下的特点：

- 类方法需要使用@classmethod装饰器装饰
- 类方法的第一个参数是cls，cls指示的是类对象自身
- 通过类调用，会自动把类对象传入给cls，如果是对象调用，则会先找到所属的类，然后再传入给cls。

3、静态方法: 跟self和cls都没有关系，也可以理解为跟类和实例对象都没有关系，可以看做是一个放在类中的普通函数，使用的比较少，具体有如下的特点：

- 静态方法需要使用@staticmethod装饰器装饰
- 静态方法没有要求第一个参数是self或者cls，不会隐式的传入参数
- 可以通过类或者实例对象调用，静态方法只是一个声明在类中的普通方法，由类这个名词空间管理，其他毫无作用。

```python
class Person:
    name = 'Wu Ming'
     
    #定义一个普通方法，第一个参数必须是self
    def method(self):
        self.name = 'Wei xiaobao'
        print(self.name)
     
    #定义一个类方法，第一个参数必须是cls
    @classmethod
    def class_method(cls):
        cls.name = 'Zhang Wuji'
        print(cls.name)
         
    #定义一个静态方法
    @staticmethod
    def static_method():
        print(Person.name)

>>> A = Person()
 
#调用类的方法，把A这个实例对象传入给self
>>> A.method()    
Wei xiaobao
>>> Person.method()
TypeError: method() missing 1 required positional argument: 'self'

#调用类方法，把Persion这个类对象传入给cls
>>> Person.class_method()
Zhang Wuji
>>> A.class_method()
Zhang Wuji

#调用类的静态方法,可以通过类或者实例对象调用静态方法
>>> Person.static_method()
Zhang Wuji
>>> A.static_method()
Zhang Wuji
```

#### 2.1.4 访问控制

 - 相关链接
	 - [Python系列教程（四十）：类的多种方法和属性访问控制 – Jimmy's Blog](https://www.xjimmy.com/python-40-class2.html)
- 拓展链接
	- [【python】详解类class的访问控制：单下划线_与双下划线__（四）_brucewong0516的博客-CSDN博客](https://blog.csdn.net/brucewong0516/article/details/79120841)

> 疑问1: 在使用保护属性 `_` 单个下划线时, from module import * 依然会导入保护属性

类的第一特性就是封装，为了更好的保护内部代码，大多数情况不会直接暴露类中定义的代码，而是通过提供的接口进行调用，而为了避免在类的外部直接访问甚至是直接修改类的属性，Python提供了两种方法来控制类属性的访问。


##### (1) 私有属性

  在Python定义类属性的时候，使用双下划线 "`__`" 开头的属性，都是私有属性（私有变量和私有方法）。

下面是文件 Person.py

```python
class Person:
    def __init__(self, name, age):
        self.__name = name        #私有变量
        self.age = age
        self.__inner()
     
    def __inner(self):            #私有方法
        print(self.__name)
        print(self.age)
```

在 Person.py 同级目录下使用命令行调用

```python
>>> from person import Person
>>> A = Person('jimmy',29)
jimmy
29
  
#在外部直接调用私有属性，抛出异常        
>>> A.__name
AttributeError: 'Person' object has no attribute '__name'
>>> A.__inner()
AttributeError: 'Person' object has no attribute '__inner'
 
#在外部直接调用普通属性，正常访问
>>> A.age
29
```

从上面的示例中可以看出，`__name` 已经是私有属性，无法在外部访问了，而在内部可以正常使用。

看一下实例对象和类对象的属性字典，你就明白了，对，它就是把属性名称改名了而已，仅此而已，所以你在外部无法直接使用原来的属性名称进行访问了。

```python
>>> A.__dict__
{'_Person__name': 'jimmy', 'age': 29}

>>> Person.__dict__
mappingproxy(
			 {'__module__': 'person', '__init__': 
			 <function Person.__init__ at 0x10476b4c0>, '_Person__inner':
			  <function Person.__inner at 0x10476b550>, '__dict__': 
			  <attribute '__dict__' of 'Person' objects>, '__weakref__': 
			  <attribute '__weakref__' of 'Person' objects>, '__doc__': None}
)
```

既然只是改了个名字，但是终究还是可以通过外部访问，那么我们是否可以访问或者修改呢？

```python
>>> A._Person__name
'jimmy'
 
#通过实际属性名称修改__name变量的值
>>> A._Person__name = 'Jimmy'
>>> A.__dict__
{'_Person__name': 'Jimmy', 'age': 29}
 
#通过实际属性名称访问__inner方法
>>> A._Person__inner()
jimmy
29
```

可以看到，我们仍然可以通过实际的属性名称去访问甚至是修改。

私有属性的总结：

- 在属性名称前面加上双下划线“`__`”。
- 私有属性在外部无法直接访问和修改。
- 私有属性的本质只是修改了属性名字，在原来的属性名字前面加上“`_classname`”，可以通过实际的名称进行访问和修改。
- 只有类对象自己可以访问, 子类对象不允许访问

##### (2) 保护属性

在Python定义类属性的时候，使用一个下划线“_”开头的属性，就是保护属性。

保护属性的访问控制强度还没有私有属性的高，连私有属性都可以绕过访问和修改，保护属性就更不要说限制了，这里的保护更多的是一种约定，因为保护属性和普通属性一样，只是说我用了保护属性，你在外部就不要随便访问和修改了。

- 保护属性在通过 `from module import *` 时, 默认不会导入
- 保护属性是只有类实例和子类实例可以访问的变量

##### (3-拓展) 单下划线"`_`"

Python中没有访问控制的关键字，例如private、protected等等。但是，在Python编码中，有一些约定来进行访问控制。

在Python中，通过单下划线 "`_`", "来实现模块级别的私有化，变量除外。一般约定以单下划线 "`_`" 开头的函数为模块私有的，也就是说"from moduleName import * “将不会引入以单下划线”_"开头的函数。

现在有一个模块 **example_example.py**，内容用如下，模块中一个变量名和一个函数名分别以"`_`"开头：

```python
name = 'bruce'
_tall = 180

def call_for():
    print('name is :',name)
    print('_tall is',_tall)
    
def _call_for():
    print('name is :',name)
    
#_call_for = _call_for()    
print()
print('_tall is',_tall)
```

运行结果

```python

_tall is 180
```

再次调用该脚本

```python
#调用脚本模块example_example
import example_example
#调用不带下划线变量
example_example.name
Out[12]: 'bruce'
#调用带下划线变量
example_example._tall     #对于变量单下划线不会影响调用
Out[13]: 180
#调用不带下划线函数
example_example.call_for()
name is : bruce
_tall is 180
#调用不带下划线函数会报错
example_example._call_for()
Traceback (most recent call last):

  File "<ipython-input-15-e642b1386946>", line 1, in <module>
    example_example._call_for()

TypeError: 'NoneType' object is not callable
```

##### (4-拓展) 双下划线"`__`"

对于Python中的类属性，可以通过双下划线 "`__`" 来实现一定程度的私有化，因为双下划线开头的属性在运行时会被"混淆”（mangling）。

```python
class person(object):
    
    tall = 180
    hobbies = []
    def __init__(self, name, age,weight):
        self.name = name
        self.age = age
        self.weight = weight
        self.__Id = 430
    @staticmethod
    def infoma():
        print(person.tall)
        print(person.hobbies)
#person.infoma()
Bruce = person("Bruce", 25,180)
print(Bruce.__Id)
#Bruce.infoma() 
```

输出结果

```python
Traceback (most recent call last):
  File "[Path]", line 19, in <module>
    print(Bruce.__Id)
AttributeError: 'person' object has no attribute '__Id'
```

其实，通过内建函数dir()就可以看到其中的一些原由，"`__Id`"属性在运行时，属性名被改为了"_person__Id"（属性名前增加了单下划线和类名）

通过命令行查看

```python
>>> class person(object):
...     
...     tall = 180
...     hobbies = []
...     def __init__(self, name, age,weight):
...         self.name = name
...         self.age = age
...         self.weight = weight
...         self.__Id = 430
...     @staticmethod
...     def infoma():
...         print(person.tall)
...         print(person.hobbies)
>>> A = person('a', '1', '2')
>>> A.__dict__
{'name': 'a', 'age': '1', 'weight': '2', '_person__Id': 430}
```

所以说，即使是双下划线，也没有实现属性的私有化，因为通过下面的方式还是可以直接访问"`__Id`"属性：

```python
>>> A._person__Id
430
```

双下划线的另一个重要的目地是，避免子类对父类同名属性的冲突

```python
class A(object):
    def __init__(self):
        self.__private()
        self.public()
    
    def __private(self):
        print('A.__private()')
    
    def public(self):
        print('A.public()')

class B(A):
    def __private(self):
        print('B.__private()')
    
    def public(self):
        print('B.public()')
    
b = B()
```

输出结果

```python
A.__private()
B.public()
```

当实例化B的时候，由于没有定义 `__init__` 函数，将调用父类的 `__init__`，但是由于双下划线的"混淆"效果，"`self.__private()`"将变成 “`self._A__private()`”。

"`_`" 和 "`__`" 的使用 更多的是一种规范/约定，并没有真正达到限制的目的：

- `_`：以单下划线开头的表示的是protected类型的变量，即只能允许其本身与子类进行访问；同时表示弱内部变量标示，如，当使用"from moduleNmae import *"时，不会将以一个下划线开头的对象引入。
- `__`：双下划线的表示的是私有类型的变量。只能是允许这个类本身进行访问了，连子类也不可以，这类属性在运行时属性名会加上单下划线和类名。



### 2.2 继承

#### 2.2.1 单继承

 继承作为类的三大特性之一，其重要性不言而喻，在一些大型项目中，构造错综复杂的类关系的时候，用的非常广泛。继承可以最大程度上体现类与类之间的关系，利用这种关系，可以做到代码复用，简化代码的作用。

而怎么去认识继承这个特性呢，其实也非常好理解，它跟我们人类社会中的继承特性非常类似，比如人类的继承，可以继承父母的一部分特征，但是也可以有自己的特征，体现在python中类的继承，就是子类继承父类的属性和方法，而子类也可以拥有属于自己的属性和方法。

所以，类的继承指的是：属性和方法的继承。所以，如果当某个类是从其他类继承而来的话，那么这个类它天生就拥有父类的属性和方法。

继承的类叫做父类，也称为基类、超类，而被继承的叫做子类，也称为派生类。

比如，我们已经编写了一个名为Animal的class，有一个run()方法可以直接打印：

```python
class Animal(object):
    def run(self):
        print('Animal is running...')
```

当我们需要编写`Dog`和`Cat`类时，就可以直接从`Animal`类继承：

```python
class Dog(Animal):
    pass

class Cat(Animal):
    pass
```

对于`Dog`来说，`Animal`就是它的父类，对于`Animal`来说，`Dog`就是它的子类。`Cat`和`Dog`类似。

继承有什么好处？最大的好处是子类获得了父类的全部功能。由于`Animial`实现了`run()`方法，因此，`Dog`和`Cat`作为它的子类，什么事也没干，就自动拥有了`run()`方法：

```python
dog = Dog()
dog.run()

cat = Cat()
cat.run()
```

输出结果

```python
Animal is running...
Animal is running...
```

当然，也可以对子类增加一些方法，比如Dog类：

```python
class Dog(Animal):

    def run(self):
        print('Dog is running...')

    def eat(self):
        print('Eating meat...')
```

继承的第二个好处需要我们对代码做一点改进。你看到了，无论是`Dog`还是`Cat`，它们`run()`的时候，显示的都是`Animal is running...`，符合逻辑的做法是分别显示`Dog is running...`和`Cat is running...`，因此，对`Dog`和`Cat`类改进如下：

```python
class Dog(Animal):

    def run(self):
        print('Dog is running...')

class Cat(Animal):

    def run(self):
        print('Cat is running...')
```

输出结果

```python
Dog is running...
Cat is running...
```

当子类和父类都存在相同的`run()`方法时，我们说，子类的`run()`覆盖了父类的`run()`，在代码运行的时候，总是会调用子类的`run()`。这样，我们就获得了继承的另一个好处：多态。

要理解什么是多态，我们首先要对数据类型再作一点说明。当我们定义一个class的时候，我们实际上就定义了一种数据类型。我们定义的数据类型和Python自带的数据类型，比如str、list、dict没什么两样：

判断一个变量是否是某个类型可以用`isinstance()`判断：

```python
>>> isinstance(a, list)
True
>>> isinstance(b, Animal)
True
>>> isinstance(c, Dog)
True
```

看来`a`、`b`、`c`确实对应着`list`、`Animal`、`Dog`这3种类型。

再来试试下面的代码

```python
class Animal(object):
    def run(self):
        print('Animal is running...')

class Dog(Animal):
    def run(self):
        print('Dog is running...')

class Cat(Animal):
    def run(self):
        print('Cat is running...')

c = Dog()

print(isinstance(c, Animal))
```

输出结果

```python
True
```

不难发现, 由 Animal 继承的 Dog, 同样属于 Animal 类, 当我们创建了一个 Dog 的实例 c 时, 此时 c 的数据类型是 Dog, Dog 本身就是 Animal 的一种, 所以 c 的数据类型也同样是 Animal

所以，在继承关系中，如果一个实例的数据类型是某个子类，那它的数据类型也可以被看做是父类。但是，反过来就不行：

修改最后几行代码

```python
c = Dog()

print(isinstance(c, Animal))
```

输出结果

```python
Flase
```

`Dog`可以看成`Animal`，但`Animal`不可以看成`Dog`。

#### 2.2.2 多继承

事实上，大部分面向对象的编程语言，都只支持单继承，即子类有且只能有一个父类。而 Python 却支持多继承（C++也支持多继承）。  
和单继承相比，多继承容易让代码逻辑复杂、思路混乱，一直备受争议，中小型项目中较少使用，后来的 Java、C#、PHP 等干脆取消了多继承。  
  
使用多继承经常需要面临的问题是，多个父类中包含同名的类方法。对于这种情况，Python 的处置措施是：根据子类继承多个父类时这些父类的**前后次序**决定，即排在前面父类中的类方法会覆盖排在后面父类中的同名类方法。

```python
class People:  
    def __init__(self):  
        self.name = People  
  
    def say(self):  
        print("People类", self.name)
        
class Animal:  
    def __init__(self):  
        self.name = Animal  
  
    def say(self):  
        print("Animal类", self.name)  
  
#People中的 name 属性和 say() 会遮蔽 Animal 类中的  
class Person(People, Animal):  
    pass
    
zhangsan = Person()  
zhangsan.name = "张三"  
zhangsan.say()
```

输出结果

```python
People类 张三
```

### 2.3 多态

要理解多态的好处，我们还需要再编写一个函数，这个函数接受一个`Animal`类型的变量：

```python
class Animal(object):
    def run(self):
        print('Animal is running...')

class Dog(Animal):
    def run(self):
        print('Dog is running...')

class Cat(Animal):
    def run(self):
        print('Cat is running...')

def run_twice(animal):
    animal.run()
run_twice(Animal())
run_twice(Dog())
run_twice(Cat())
```

输出结果

```python
Animal is running...
Dog is running...
Cat is running...
```

看上去没啥意思，但是仔细想想，现在，如果我们再定义一个`Tortoise`类型，也从`Animal`派生：

```python
class Animal(object):  
    def run(self):  
        print('Animal is running...')  
  
class Dog(Animal):  
    def run(self):  
        print('Dog is running...')  
  
class Cat(Animal):  
    def run(self):  
        print('Cat is running...')  
  
def run_twice(animal):  
    animal.run()  
  
run_twice(Animal())  
run_twice(Dog())  
run_twice(Cat())  
  
class Tortoise(Animal):  
    def run(self):  
        print('Tortoise is running slowly...')  
  
run_twice(Tortoise())
```

输出结果

```python
Animal is running...
Dog is running...
Cat is running...
Tortoise is running slowly...
```

你会发现，新增一个 `Animal` 的子类，不必对 `run_twice()` 做任何修改，实际上，任何依赖 `Animal` 作为参数的函数或者方法都可以不加修改地正常运行，原因就在于多态。

多态的好处就是，当我们需要传入 `Dog`、`Cat`、`Tortoise`……时，我们只需要接收 `Animal` 类型就可以了，因为 `Dog`、`Cat`、`Tortoise` ……都是 `Animal` 类型，然后，按照`Animal`类型进行操作即可。由于 `Animal` 类型有 `run()` 方法，因此，传入的任意类型，只要是 `Animal` 类或者子类，就会自动调用实际类型的 `run()` 方法，这就是多态的意思：

对于一个变量，我们只需要知道它是 `Animal` 类型，无需确切地知道它的子类型，就可以放心地调用 `run()` 方法，而具体调用的 `run()` 方法是作用在 `Animal`、`Dog`、`Cat` 还是 `Tortoise` 对象上，由运行时该对象的确切类型决定，这就是多态真正的威力：调用方只管调用，不管细节，而当我们新增一种 `Animal` 的子类时，只要确保 `run()` 方法编写正确，不用管原来的代码是如何调用的。这就是著名的“开闭”原则：

- 对扩展开放：允许新增 `Animal` 子类；
- 对修改封闭：不需要修改依赖 `Animal` 类型的 `run_twice()` 等函数。

继承还可以一级一级地继承下来，就好比从爷爷到爸爸、再到儿子这样的关系。而任何类，最终都可以追溯到根类object，这些继承关系看上去就像一颗倒着的树。

#### 2.3.1 方法重写

前面讲过在 Python 中，子类继承了父类，那么子类就拥有了父类所有的类属性和类方法。通常情况下，子类会在此基础上，扩展一些新的类属性和类方法。  
  
但凡事都有例外，我们可能会遇到这样一种情况，即子类从父类继承得来的类方法中，大部分是适合子类使用的，但有个别的类方法，并不能直接照搬父类的，如果不对这部分类方法进行修改，子类对象无法使用。针对这种情况，我们就需要在子类中重复父类的方法。  
  
举个例子，鸟通常是有翅膀的，也会飞，因此我们可以像如下这样定义个和鸟相关的类：

```python
class Bird:
    #鸟有翅膀
    def isWing(self):
        print("鸟有翅膀")
    #鸟会飞
    def fly(self):
        print("鸟会飞")
```

但是，对于鸵鸟来说，它虽然也属于鸟类，也有翅膀，但是它只会奔跑，并不会飞。针对这种情况，可以这样定义鸵鸟类：

```python
class Ostrich(Bird):
    # 重写Bird类的fly()方法
    def fly(self):
        print("鸵鸟不会飞")
```

可以看到，因为 Ostrich 继承自 Bird，因此 Ostrich 类拥有 Bird 类的 isWing() 和 fly() 方法。其中，isWing() 方法同样适合 Ostrich，但 fly() 明显不适合，因此我们在 Ostrich 类中对 fly() 方法进行重写。

> 重写，有时又称覆盖，是一个意思，指的是对类中已有方法的内部实现进行修改。

在上面 2 段代码的基础上，添加如下代码并运行：

```python
class Bird:
    #鸟有翅膀
    def isWing(self):
        print("鸟有翅膀")
        
    #鸟会飞
    def fly(self):
        print("鸟会飞")
        
class Ostrich(Bird):
    # 重写Bird类的fly()方法
    def fly(self):
        print("鸵鸟不会飞")
        
# 创建Ostrich对象
ostrich = Ostrich()
#调用 Ostrich 类中重写的 fly() 类方法
ostrich.fly()
```

输出结果

```python
鸵鸟不会飞
```

显然，ostrich 调用的是重写之后的 fly() 类方法。

#### 2.3.2 调用重写后方法

事实上，如果我们在子类中重写了从父类继承来的类方法，那么当在类的外部通过子类对象调用该方法时，Python 总是会执行子类中重写的方法。

这就产生一个新的问题，即如果想调用父类中被重写的这个方法，该怎么办呢？

很简单，前面讲过，Python 中的类可以看做是一个独立空间，而类方法其实就是出于该空间中的一个函数。而如果想要全局空间中，调用类空间中的函数，只需要在调用该函数是备注类名即可。举个例子：

```python
class Bird:
    #鸟有翅膀
    def isWing(self):
        print("鸟有翅膀")
    #鸟会飞
    def fly(self):
        print("鸟会飞")
class Ostrich(Bird):
    # 重写Bird类的fly()方法
    def fly(self):
        print("鸵鸟不会飞")
# 创建Ostrich对象
ostrich = Ostrich()
#调用 Bird 类中的 fly() 方法
Bird.fly(ostrich)
```

输出结果

```python
鸟会飞
```

此程序中，需要大家注意的一点是，使用类名调用其类方法，Python 不会为该方法的第一个 self 参数自定绑定值，因此采用这种调用方法，需要手动为 self 参数赋值。

> 通过类名调用实例方法的这种方式，又被称为未绑定方法。

## 3. 运算符重载

Python语言本身提供了很多魔法方法，它的运算符重载就是通过重写这些Python内置魔法方法实现的。这些魔法方法都是以双下划线开头和结尾的，类似于__X__的形式，python通过这种特殊的命名方式来拦截操作符，以实现重载。

当Python的内置操作运用于类对象时，Python会去搜索并调用对象中指定的方法完成操作。

类可以重载加减运算、打印、函数调用、索引等内置运算，运算符重载使我们的对象的行为与内置对象的一样。Python在调用操作符时会自动调用这样的方法，例如，如果类实现了__add__方法，当类的对象出现在+运算符中时会调用这个方法。

更多方法参考 [[6. Python 面向对象#4 类的专有方法]]

下面对常用的运算符方法的使用进行一下介绍。

#### 3.1 构造函数和析构函数：`__init__` 和 `__del__`

它们的主要作用是进行对象的创建和回收，当实例创建时，就会调用__init__构造方法。当实例对象被收回时，析构函数__del__会自动执行。

```python
class Human():
	def __init__(self, n):
		self.name = n
		print("__init__ ",self.name)

	def __del__(self):
		print("__del__")

h = Human('Tim')

h = 'a'
```

输出结果

```python
# h = Human('Tim') 时输出
__init__  Tim

# h = 'a' 时输出
__del__
```

#### 3.2 加减运算：`__add__` 和 `__sub__`

重载这两个方法就可以在普通的对象上添加＋－运算符操作。下面的代码演示了如何使用＋－运算符，如果将代码中的__sub__方法去掉，再调用减号运算符就会出错。

```python
class Computation():
	def __init__(self,value):
		self.value = value
		
	def __add__(self,other):
		return self.value + other
		
	def __sub__(self,other):
		return self.value - other

c = Computation(5)
print(c + 5)
print(c - 3)
```

输出结果

```python
10
2
```

#### 3.3 对象的字符串表达形式：`__repr__` 和 `__str__`
       
这两个方法都是用来表示对象的字符串表达形式：print()、str()方法会调用到__str__方法，print()、str()和repr()方法会调用__repr__方法。从下面的例子可以看出，当两个方法同时定义时，Python会优先搜索并调用__str__方法。

```python
class Str(object):
    def __str__(self):
        return "__str__ called"

    def __repr__(self):
        return "__repr__ called"

s = Str()
print(s)
# 输出 repr(s) 的结果
print(repr(s))
# 输出 str(s) 的结果
print(str(s))
```

输出结果

```python
__str__ called
__repr__ called
__str__ called
```

#### 3.4 索引取值和赋值：`__getitem__` , `__setitem__`

通过实现这两个方法，可以通过诸如 X[i] 的形式对对象进行取值和赋值，还可以对对象使用切片操作

```python
class Indexer:
    data = [1, 2, 3, 4, 5, 6]

    def __getitem__(self, index):
        return self.data[index]

    def __setitem__(self, k, v):
        self.data[k] = v
        print(self.data)


i = Indexer()
print(i[0])
print(i[1:4])
i[0] = 10
```

输出结果

```python
1
[2, 3, 4]
[10, 2, 3, 4, 5, 6]
```

#### 3.5 设置和访问属性：`__getattr__`、`__setattr__`

我们可以通过重载 `__getattr__` 和 `__setattr__` 来拦截对对象成员的访问。

`__getattr__` 在访问对象中不存在的成员时会自动调用。

`__setattr__` 方法用于在初始化对象成员的时候调用，即在设置 `__dict__` 的item时就会调用 `__setattr__` 方法。

具体例子如下：

```python
class A():
    def __init__(self,ax,bx):
        self.a = ax
        self.b = bx
    def f(self):
        print (self.__dict__)
    def __getattr__(self,name):
        print ("__getattr__")
    def __setattr__(self,name,value):
        print ("__setattr__")
        self.__dict__[name] = value
 
print('== 1 号分割线 ==')  
a = A(1, 2)  
print('== 2 号分割线 ==')  
a.f()  
print('== 3 号分割线 ==')  
a.x  
print('== 4 号分割线 ==')  
a.x = 3  
print('== 5 号分割线 ==')  
a.f()
```

输出结果

```python
== 1 号分割线 ==
__setattr__
__setattr__
== 2 号分割线 ==
{'a': 1, 'b': 2}
== 3 号分割线 ==
__getattr__
== 4 号分割线 ==
__setattr__
== 5 号分割线 ==
{'a': 1, 'b': 2, 'x': 3}
```

从结果可以看出，访问不存在的变量 x 时会调用__getattr__方法；当__init__被调用的时候，赋值运算也会调用__setattr__方法。

#### 3.6 迭代器对象: `__iter__`,  `__next__`

Python中的迭代，可以直接通过重载__getitem__方法来实现，看下面的例子。

```python
class Indexer:
	data = [1,2,3,4]
	def __getitem__(self,index):
		return self.data[index]

x = Indexer()
for item in x:
	print(item)
```

输出结果

```python
1
2
3
4
```

通过上面的方法是可以实现迭代，但并不是最好的方式。

Python的迭代操作会优先尝试调用__iter__方法，再尝试__getitem__。

迭代环境是通过 iter 去尝试寻找__iter__方法来实现，而这种方法返回一个迭代器对象。如果这个方法已经提供，Python会重复调用迭代器对象的next()方法，直到发生StopIteration异常。

如果没有找到__iter__，Python才会尝试使用__getitem__机制。下面看一下迭代器的例子。

```python
class Next(object):  
    def __init__(self, data=1):  
        self.data = data  
  
    def __iter__(self):  
        return self  
  
    def __next__(self):  
        print("__next__ called")  
        if self.data > 5:  
            raise StopIteration  
        else:  
            self.data += 1  
            return self.data  
  
  
for i in Next(3):  
    print(i)  
print("-----------")  
n = Next(3)  
i = iter(n)  
while True:  
    try:  
        print(next(i))  
    except Exception as e:  
        break
```

输出结果

```python
__next__ called
4
__next__ called
5
__next__ called
6
__next__ called
-----------
__next__ called
4
__next__ called
5
__next__ called
6
__next__ called
```

可见实现了__iter__和__next__方法后，可以通过for in的方式迭代遍历对象，也可以通过iter()和next()方法迭代遍历对象。

## 4. 装饰器

在绑定属性时，如果我们直接把属性暴露出去，虽然写起来很简单，但是，没办法检查参数，导致可以把成绩随便改：

```python
class Student():  
    name = "ming"  
    age = "11"  
  
  
s = Student()  
s.score = 9999  
  
print(s.name)  
print(s.age)  
print(s.score)
```

这显然不合逻辑。为了限制score的范围，可以通过一个`set_score()`方法来设置成绩，再通过一个`get_score()`来获取成绩，这样，在`set_score()`方法里，就可以检查参数：

文件名称为 example.py

```python
class Student(object):

    def get_score(self):
         return self._score

    def set_score(self, value):
        if not isinstance(value, int):
            raise ValueError('score must be an integer!')
        if value < 0 or value > 100:
            raise ValueError('score must between 0 ~ 100!')
        self._score = value

>>> from example import *
>>> s = Student()
>>> s.set_score(60)
>>> s.get_score()
60
>>> s.set_score(9999)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  File "[Path]", line 10, in set_score
    raise ValueError('score must between 0 ~ 100!')
ValueError: score must between 0 ~ 100!
```

但是，上面的调用方法又略显复杂，没有直接用属性这么直接简单。

有没有既能检查参数，又可以用类似属性这样简单的方式来访问类的变量呢？对于追求完美的Python程序员来说，这是必须要做到的！

还记得装饰器（decorator）可以给函数动态加上功能吗？对于类的方法，装饰器一样起作用。Python内置的@property装饰器就是负责把一个方法变成属性调用的：

```python
class Student(object):

    @property
    def score(self):
        return self._score

    @score.setter
    def score(self, value):
        if not isinstance(value, int):
            raise ValueError('score must be an integer!')
        if value < 0 or value > 100:
            raise ValueError('score must between 0 ~ 100!')
        self._score = value
```

`@property` 的实现比较复杂，我们先考察如何使用。把一个getter 方法变成属性，只需要加上 `@property` 就可以了，此时，`@property` 本身又创建了另一个装饰器 `@score.setter`， 负责把一个setter方法变成属性赋值，于是，我们就拥有一个可控的属性操作：

```python
>>> s = Student()
>>> s.score = 60 # OK，实际转化为 s.set_score(60)
>>> s.score # OK，实际转化为s.get_score()
60
>>> s.score = 9999
Traceback (most recent call last):
  ...
ValueError: score must between 0 ~ 100!
```

注意到这个神奇的`@property`，我们在对实例属性操作的时候，就知道该属性很可能不是直接暴露的，而是通过getter和setter方法来实现的。

还可以定义只读属性，只定义getter方法，不定义setter方法就是一个只读属性：

```python
class Student(object):

    @property
    def birth(self):
        return self._birth

    @birth.setter
    def birth(self, value):
        self._birth = value

    @property
    def age(self):
        return 2015 - self._birth
```

上面的`birth`是可读写属性，而`age`就是一个_只读_属性，因为`age`可以根据`birth`和当前时间计算出来。

要特别注意：属性的方法名不要和实例变量重名。例如，以下的代码是错误的：

```python
class Student(object):

    # 方法名称和实例变量均为birth:
    @property
    def birth(self):
        return self.birth
```

这是因为调用`s.birth`时，首先转换为方法调用，在执行`return self.birth`时，又视为访问`self`的属性，于是又转换为方法调用，造成无限递归，最终导致栈溢出报错`RecursionError`。

`@property`广泛应用在类的定义中，可以让调用者写出简短的代码，同时保证对参数进行必要的检查，这样，程序运行时就减少了出错的可能性。

小练习:

请利用`@property`给一个`Screen`对象加上`width`和`height`属性，以及一个只读属性`resolution`：

注释内容复制完就删掉, 做十分钟做不出来再来看答案

```python
# -*- coding: utf-8 -*-  
class Screen(object):  

'''
    @property  
    def width(self):  
        return self._width  
  
    @width.setter  
    def width(self, value):  
        self._width = value  
  
    @property  
    def height(self):  
        return self._height  
  
    @height.setter  
    def height(self, value):  
        self._height = value  
  
    @property  
    def resolution(self):  
        return self.height*self.width  
'''

# 测试:  
s = Screen()  
s.width = 1024  
s.height = 768  
print('resolution =', s.resolution)  
if s.resolution == 786432:  
    print('测试通过!')  
else:  
    print('测试失败!')
```

## 5. 反射

python中的反射功能是由以下四个内置函数提供：hasattr、getattr、setattr、delattr，改四个函数分别用于对对象内部执行：检查是否含有某成员、获取成员、设置成员、删除成员。

```python
class Foo(object):

    def __init__(self):
        self.name = 'kylin'

    def func(self):
        return 'func'


obj = Foo()

print('#### 检查是否含有成员 ####')
print(hasattr(obj, 'name'))
print(hasattr(obj, 'func'))

print('# #### 获取成员 ####')
print(getattr(obj, 'name'))
print(getattr(obj, 'func'))

print('#### 设置成员 ####')
print(setattr(obj, 'age', 18))
print(setattr(obj, 'show', lambda num: num + 1))
print(obj.age)

print('#### 删除成员 ####')
delattr(obj, 'name')
delattr(obj, 'func')
```

输出结果

```python
#### 检查是否含有成员 ####
True
True
# #### 获取成员 ####
kylin
<bound method Foo.func of <__main__.Foo object at 0x10068b310>>
#### 设置成员 ####
None
None
18
#### 删除成员 ####
```

反射的概念是由 Smith 在 1982 年首次提出的，主要是指程序可以访问、检测和修改它本身状态或行为的一种能力（自省）

反射就是通过字符串的形式，导入模块；通过字符串的形式，去模块寻找指定函数，并执行。利用字符串的形式去对象（模块）中操作（查找/获取/删除/添加）成员，一种基于字符串的事件驱动！

python 里的反射有下面四种方法

- hasattr(obj,name_str)：判断一个对象 obj 里是否有对应的 name_str 字符串的方法
- getattr(obj,name_str)：根据字符串去获取 obj 对象里的对应方法的内存地址
- setattr(obj,"y",z)：相当于 obj.y=z
- delattr(obj,name_str)：删除属性

命名空间.XXX == getattr(命名空间，"XXX")

类名.名字   

- getattr(类名，"名字")

对象名.名字

- getattr(对象，"名字")

模块名.名字

- import 模块
- getattr(模块，”名字“)

自己文件.名字

- import sys
- getattr(sys.modules['__main__']，"名字")

类，静态属性，类方法，静态方法都可以反射

```python
class Student:  
    ROLE = 'STUDENT'  
  
    @classmethod  
    def register(cls):  
        print('getattr-类方法:注册')  
  
    @staticmethod  
    def login():  
        print('getattr-静态方法:登录')  
  
  
print("直接查看属性: ",Student.ROLE)  
print("getattr-反射查看属性: ",getattr(Student, 'ROLE'))  
  
#  反射调用方法  
getattr(Student, 'register')()  # 类方法  
getattr(Student, 'login')()  # 静态方法
```

输出结果

```python
直接查看属性:  STUDENT
getattr-反射查看属性:  STUDENT
getattr-类方法:注册
getattr-静态方法:登录
```

### 5.1 hasattr 和 getattr

```python
class Dog(object):  
  
    def __init__(self, name):  
        self.name = name  
  
    def eat(self, food):  
        print('让我看看 %s 在吃什么, 噢...' % self.name, food)  
  
  
obj = Dog('白色修勾')  
  
choice = input('请输入>>:').strip()  
# 不能d.choice()   会报错,因为choice是字符串  
  
print(hasattr(obj, choice))  # 判断输入的在类里有没有这个方法，有返回True，否则False  
print(getattr(obj, choice))  # 返回了输入方法的内存对象  
getattr(obj, choice)('炸鸡!')  # 知道内存对象后加（）传参调用
```

用户输入 eat 时，因为 Dog 类下有 eat 方法, 输出结果如下

```python
请输入>>:eat
True
<bound method Dog.eat of <__main__.Dog object at 0x102d17310>>
让我看看 白色修勾 在吃什么, 噢... 炸鸡!
```

用户输入 sleep, 因为 Dog 类下没有 sleep 方法, 输出结果如下

```python
请输入>>:sleep
False
Traceback (most recent call last):
  File "[Path]", line 16, in <module>
    print(getattr(d, choice))  # 返回了输入方法的内存对象
AttributeError: 'Dog' object has no attribute 'sleep'
```

因为Dog下没有 game ，所以报错了

所以可以做个判断，如果  hasattr(d, choice) 返回为 True了，在执行  getattr(d, choice) 

改写后的如下

```python
class Dog(object):  
  
    def __init__(self, name):  
        self.name = name  
  
    def eat(self, food):  
        print('让我看看 %s 在吃什么, 噢...' % self.name, food)  
  
  
obj = Dog('白色修勾')  
  
choice = input('请输入>>:').strip()  
# 不能d.choice()   会报错,因为choice是字符串  
  
if hasattr(obj, choice):  
    func = getattr(obj, choice)  
    func('炸鸡!')  
else:  
    print("抱歉, 狗勾暂时不会", choice)
```

输入 eat 后输出结果如下

```python
请输入>>:eat
让我看看 白色修勾 在吃什么, 噢... 炸鸡!
```

输入 sleep 后输出结果如下

```python
请输入>>:sleep
抱歉, 狗勾暂时不会 sleep
```

**getattr例子**

```python
import time  
print(time.time(), getattr(time, 'time')())
```

输出结果

```python
1663899590.4877849
1663899590.4877949
```

### 5.2 setattr

```python
class Dog(object):  
  
    def __init__(self, name):  
        self.name = name  
  
    def eat(self, food):  
        print('%s 在吃...' % self.name, food)  
  
  
def die(self):  # 装到类里必须要有self  
    print('%s 睡着了...' % self.name)  
  
  
obj = Dog('黑色修勾')  
choice = input('请输入>>:').strip()  
  
# 判断输入的在类里有没有这个方法  
if hasattr(obj, choice):  
    # 有这个方法执行，获得输入的在类里方法的内存对象  
    func = getattr(obj, choice)  
  
    # 将参数传给func，相当于执行了obj.eat('火锅!')  
    func('火锅!')  
# 输入的类里面的方法如果不存在  
else:  
    # setattr(obj, choice, die) 等价于 obj.choice=die    # 动态添加 die 方法  
    setattr(obj, choice, die)  
    # 执行输入的方法 sleep 要把类对象传给，必须是 obj.输入的内容  
    obj.sleep(obj)
```

输入 eat 和 sleep 的结果如下

```python
请输入>>:eat
黑色修勾 在吃... 火锅!

请输入>>:sleep
黑色修勾 睡着了...
```

这时用户只能输入 eat 或者 talk ，输入其他会报错

如果想让输入 Dog类下不存在的方法，都执行 sleep 下的，修改 else 判断语句

```python
# 输入的类里面的方法如果不存在  
else:  
	# 动态添加 die 方法
    setattr(obj, choice, die)  
    func = getattr(obj, choice)
    # 调用新加的方法，不管输入什么，都执行的 sleep 函数
    func(obj)
```

### 5.3 delattr

setattr() 相关的函数。实参是一个对象和一个字符串。该字符串必须是对象的某个属性。如果对象允许，该函数将删除指定的属性。例如 delattr(x, ‘foobar’) 等价于 del x.foobar 。

Python中通过getattr、setattr、hasattr和delattr四个函数操作属性的机制就是反射。是通过字符串的形式操作对象属性和方法的机制。下面对p属性应用setattr、hasattr和delattr这三个函数看看效果：

判断p对象是否有say_bye属性和say_hi属性：

```python
class Person:  
    type = "mammal"  
  
    def __init__(self, name):  
        self.name = name  
  
    def say_hi(self):  
        print('Hello, my name is', self.name)  
  
    @staticmethod  
    def feed():  
        print("Three times per day.")  
  
    @classmethod  
    def sleep(cls):  
        print("8 hours!")  
  
  
p = Person('kylin')
# 给p对象增加 age 属性：
setattr(p, 'age', 18)
# 输出 age 的值
print("age 值为: ", getattr(p, 'age'))
# 删除age属性
delattr(p, 'age')  
print(hasattr(p, 'age'))  # 输出False
```

输出结果

```python
age 值为:  18
False
```

 ## Reference

- 类和对象
	- [python中类和对象的区别是什么-Python常见问题-Python学习网](https://m.py.cn/faq/python/14171.html)
- Self
	- [Python self用法详解](http://c.biancheng.net/view/2266.html)
- 方法
	- [一文看懂Python面向对象编程 | 大江狗的博客](https://pythondjango.cn/python/advanced/1-python-object-class-programming/)
	- [Python3 面向对象 | 菜鸟教程](https://www.runoob.com/python3/python3-class.html)
	- [Python实例方法、静态方法和类方法详解（包含区别和用法）](http://c.biancheng.net/view/4552.html)
- 封装
	- [Python 类和对象](https://www.w3schools.cn/python/python_classes.asp)
	- [Python 类的封装_张小凡vip的博客-CSDN博客_python 类封装](https://blog.csdn.net/zzq900503/article/details/80567089)
	- [一文看懂Python面向对象编程 | 大江狗的博客](https://pythondjango.cn/python/advanced/1-python-object-class-programming/)
	- [实例属性和类属性 - 廖雪峰的官方网站](https://www.liaoxuefeng.com/wiki/1016959663602400/1017594591051072)
- 继承
	- [Python系列教程（四十二）：类的继承 – Jimmy's Blog](https://www.xjimmy.com/python-42-inheritance.html)
	- [继承和多态 - 廖雪峰的官方网站](https://www.liaoxuefeng.com/wiki/1016959663602400/1017497232674368)
- 多态
	- [继承和多态 - 廖雪峰的官方网站](https://www.liaoxuefeng.com/wiki/1016959663602400/1017497232674368)
	- [Python父类方法重写（入门必读）](http://c.biancheng.net/view/2289.html)
- 运算符重载
	- [浅析Python运算符重载_viclee108的博客-CSDN博客_python 重载比较运算符](https://blog.csdn.net/goodlixueyong/article/details/52589979)
- 装饰器
	- [使用@property - 廖雪峰的官方网站](https://www.liaoxuefeng.com/wiki/1016959663602400/1017502538658208)
- 反射
	- [python--反射 - 邹邹很busy。 - 博客园](https://www.cnblogs.com/zouzou-busy/p/13236446.html)
	- [Python - 面向对象编程 - 反射 hasattr、getattr、getattr、delattr](https://cloud.tencent.com/developer/article/1877367)
	- [想用Python做自动化测试？Python反射机制的应用_普通网友的博客-CSDN博客_python 反射 自动化](https://blog.csdn.net/AI_Green/article/details/119893960)
- **拓展阅读**
	- [Python 面向对象（初级篇） - 武沛齐 - 博客园](https://www.cnblogs.com/wupeiqi/p/4493506.html)
	- [python 面向对象（进阶篇） - 武沛齐 - 博客园](https://www.cnblogs.com/wupeiqi/p/4766801.html)

# 第七章 Python 模块

使用 Python 进行编程时，有些功能没必须自己实现，可以借助 Python 现有的标准库或者其他人提供的第三方库。

它们位于 Python 标准库中的 math（或 cmath）模块中，只需要将此模块导入到当前程序，就可以直接拿来用。

前面章节中，已经看到使用 import 导入模块的语法，但实际上 import 还有更多详细的用法，主要有以下两种：

- `import 模块名1 [as 别名1], 模块名2 [as 别名2]，…`
	- 使用这种语法格式的 import 语句，会导入指定模块中的所有成员（包括变量、函数、类等）。不仅如此，当需要使用模块中的成员时，需用该模块名（或别名）作为前缀，否则 Python 解释器会报错。
- `from 模块名 import 成员名1 [as 别名1]，成员名2 [as 别名2]，…`
	- 使用这种语法格式的 import 语句，只会导入模块中指定的成员，而不是全部成员。同时，当程序中使用该成员时，无需附加任何前缀，直接使用成员名（或别名）即可。

注意，用 [] 括起来的部分，可以使用，也可以省略。

> 其中，第二种 import 语句也可以导入指定模块中的所有成员，即使用 form 模块名 import ＊，但此方式不推荐使用，具体原因本节后续会做详细说明。

## 1. 导入模块

### 1.1 import 模块名 as 别名

下面程序使用导入整个模块的最简单语法来导入指定模块：

```python
# 导入sys整个模块
import sys
# 使用sys模块名作为前缀来访问模块中的成员
print(sys.argv[0])
```

上面第 2 行代码使用最简单的方式导入了 sys 模块，因此在程序中使用 sys 模块内的成员时，必须添加模块名作为前缀。

运行上面程序，可以看到如下输出结果（sys 模块下的 argv 变量用于获取运行 Python 程序的命令行参数，其中 argv[0] 用于获取当前 Python 程序的存储路径）：

```python
/Users/kylin/Projects/Python/demo.py
```

导入整个模块时，也可以为模块指定别名。例如如下程序：

```python
import sys as s
print(s.argv[0])
```

第 2 行代码在导入 sys 模块时才指定了别名 s，因此在程序中使用 sys 模块内的成员时，必须添加模块别名 s 作为前缀。运行该程序，可以看到如下输出结果：

```python
/Users/kylin/Projects/Python/demo.py
```

也可以一次导入多个模块，多个模块之间用逗号隔开。例如如下程序：

```python
# 导入sys、os两个模块  
import sys,os  
# 使用模块名作为前缀来访问模块中的成员  
print(sys.argv[0])  
# os 执行系统命令 whoami
os.system('whoami')
```

输出结果

```python
/Users/kylin/Projects/Python/pHunter/test.py
kylin
```

在导入多个模块的同时，也可以为模块指定别名，例如如下程序：

```python
# 导入sys、os两个模块，并为sys指定别名s，为os指定别名o  
import sys as s,os as o  
# 使用模块别名作为前缀来访问模块中的成员  
print(s.argv[0])  
o.system('whoami')
```

上面第 2 行代码一次导入了sys 和 os 两个模块，并分别为它们指定别名为 s、o，因此程序可以通过 s、o 两个前缀来使用 sys、os 两个模块内的成员。输出结果同上

### 1.2 from 模块名 import 成员名 as 别名

下面程序使用了 from...import 最简单的语法来导入指定成员：

```python
# 导入sys模块的argv成员
from sys import argv
# 使用导入成员的语法，直接使用成员名访问
print(argv[0])
```

输出结果

```python
/Users/kylin/Projects/Python/demo.py
```

导入模块成员时，也可以为成员指定别名，例如如下程序：

```python
# 导入sys模块的argv成员，并为其指定别名v
from sys import argv as v
# 使用导入成员（并指定别名）的语法，直接使用成员的别名访问
print(v[0])
```

输出结果

```python
/Users/kylin/Projects/Python/demo.py
```

form...import 导入模块成员时，支持一次导入多个成员，例如如下程序：

```python
# 导入os 模块的 system, getcwd 成员  
from os import system, getcwd  
# 使用导入成员的语法，直接使用成员名访问  
system('whoami')  
print(getcwd())
```

输出结果中 kylin 对应 whoami 的执行结果, `/User/kylin/Projects/Python` 对应当前文件所处的绝对路径

```python
kylin
/Users/kylin/Projects/Python
```

一次导入多个模块成员时，也可指定别名，同样使用 as 关键字为成员指定别名，例如如下程序：

```python
# 导入os 模块的 system, getcwd 成员, 并为其指定别名 shell, cwdfrom os import system as shell, getcwd as cwd  
# 使用导入成员（并指定别名）的语法，直接使用成员的别名访问  
shell('whoami')  
print(cwd())
```

输出结果同上

```python
kylin
/Users/kylin/Projects/Python
```

**不推荐使用 from import 导入模块所有成员**

在使用 from...import 语法时，可以一次导入指定模块内的所有成员（**此方式不推荐**），例如如下程序：

```python
#导入 os 棋块内的所有成员
from os import *

# 使用导入成员的语法，直接使用成员的别名访问
system('whoami')  
print(getcwd())
```

上面代码一次导入了 sys 模块中的所有成员，这样程序即可通过成员名来使用该模块内的所有成员。该程序的输出结果和前面程序的输出结果完全相同。

需要说明的是，一般不推荐使用 `from 模块 import *` 这种语法导入指定模块内的所有成员，因为它存在潜在的风险。比如同时导入 module1 和 module2 内的所有成员，假如这两个模块内都有一个 foo() 函数，那么当在程序中执行如下代码时：

```python
foo()
```

上面调用的这个 foo() 函数到底是 module1 模块中的还是 module2 模块中的？因此，这种导入指定模块内所有成员的用法是有风险的。

但如果换成如下两种导入方式：

```python
import module1  
import module2 as m2
```

接下来要分别调用这两个模块中的 foo() 函数就非常清晰。程序可使用如下代码：

```python
#使用模块module1 的模块名作为前缀调用foo()函数
module1.foo()
#使用module2 的模块别名作为前缀调用foo()函数
m2.foo()
```

或者使用 from...import 语句也是可以的：

```python
#导入module1 中的foo 成员，并指定其别名为foo1
from module1 import foo as foo1
#导入module2 中的foo 成员，并指定其别名为foo2
from module2 import foo as foo2
```

此时通过别名将 module1 和 module2 两个模块中的 foo 函数很好地进行了区分，接下来分别调用两个模块中 foo() 函数就很清晰：

```python
foo1() #调用module1 中的foo()函数
foo2() #调用module2 中的foo()函数
```

## 2. 常用模块

### 2.1 文件处理

#### 2.1.1 os 模块

os模块是Python中一个内置的用来操作文件的模块

| 方法                        | 功能                                     |
|---------------------------|----------------------------------------|
| os.listdir(‘路径，默认文件所在路径’) | 读取指定路径目录结构并作为返回值返回                     |
| os.getcwd()               | 读取当前文件所在目录并作为返回值返回                     |
| os.chdir （'路径‘’）          | 用来改变文件当前所在路径                           |
| os.mkdir（‘目录名’）           | 创建目录                                   |
| os.rmdir（‘目录名’）           | 删除目录（只能删除空目录，非空目录会报错）                  |
| os.makedirs（'目录名’）        | 生成多层目录                                 |
| os.removedirs（'目录名’）      | 删除多层空目录（只能删除空目录，非空目录会报错）               |
| os.rename（'原目录名‘,'新目录名’）  | 目录重命名                                  |
| os.stat(‘目录名或文件名’)        | 读取目录或文件信息                              |
| os.name                   | 判断当前系统信息，如果是Windows则返回nt，Linux则返回posix |
| os.environ                | 获取系统变量                                 |
| os.system（'命令语句’）         | 运行shell命令                              |

##### (1) 读取目录/结构

```python
import os
# listdir读取指定路径目录结构
data = os.listdir('.')
print(data)

# getcwd读取当前文件所在目录
data = os.getcwd()
print(data)
```

运行结果

```python
['file.txt', 'file.py']
/User/kylin/Projects/Python
```

##### (2) 创建目录

```python
import os    
# mkdir创建目录  
os.mkdir('我是os模块创建的目录')  
  
# chdir用来改变文件当前所在路径  
os.chdir('./我是os模块创建的目录')  
data = os.getcwd()  
print(data)  
  
# listdir 读取上级目录目录结构  
data = os.listdir('../')  
print(data)
```

运行结果

```python
/Users/kylin/Projects/Python/我是os模块创建的目录
['file.py', 'file.txt', '我是os模块创建的目录']
```

##### (3) 删除目录

```python
import os
# rmdir删除一层目录
os.rmdir('我是os模块创建的目录')

# listdir 读取当前目录结构  
data = os.listdir('./')  
print(data)
```

运行结果

```python
['file.py', 'file.txt']
```

##### (4) 生成多级目录

```python
import os
# mkdir创建目录  
os.mkdir('我是os创建的多层目录')  
  
# makedirs生成多层目录  
os.makedirs('我是os创建的多层目录//第二层')  
  
# listdir 读取当前目录结构  
data = os.listdir('./')  
print(data)  
  
# listdir 读取 makeedirs 创建目录下的目录结构  
data = os.listdir('我是os创建的多层目录')  
print(data)
```

运行结果

```python
['file.txt', 'file.py', '我是os创建的多层目录']
['第二层']
```

##### (5) 删除多级目录

直接使用 `rmdir()` 删除目录只能删除一层

这里使用 `removeedirs()` 递归删除

```python
import os
# removedirs删除多层空目录
os.removedirs('我是os创建的多层目录/第二层')
```

##### (6) 重命名文件

```python
# mkdir 创建目录  
os.mkdir('我是os模块创建的目录')  

# rename 重命名文件
os.rename('我是os模块创建的目录', '我是经过重命名的文件')

# listdir 读取当前目录下的目录结构  
data = os.listdir('我是os创建的多层目录')  
print(data)
```

运行结果

```python
['file.py', 'file.py', '我是经过重命名的文件']
```

##### (7) 获取文件或目录信息

```python
import os
# mkdir 创建目录  
os.mkdir('我是os模块创建的目录')

# stat获取文件或目录信息
data1 = os.stat('我是os模块创建的目录')
data2 = os.stat('file.py')
print(data1, data2)
```

运行结果

```python
os.stat_result(st_mode=16877, st_ino=4051974, st_dev=16777229, st_nlink=2, st_uid=501, st_gid=20, st_size=64, st_atime=1663914020, st_mtime=1663914020, st_ctime=1663914020)
os.stat_result(st_mode=33188, st_ino=3979761, st_dev=16777229, st_nlink=1, st_uid=501, st_gid=20, st_size=208, st_atime=1663914007, st_mtime=1663914007, st_ctime=1663914007)
```

##### (8) 系统相关

```python
import os
# name输出当前运行系统环境Windows为nt，Linux为posix
system_name = os.name
print(system_name)

# environ获取系统变量
system_environ = os.environ
print(system_environ)

# system运行shell命令
os.system('whoami')
os.system('date')
```

运行结果

```python
posix
environ({'PATH':......'})
kylin
Fri Sep 23 14:22:54 CST 2022
```

### 2.2 时间日期

#### 2.2.1 time模块

##### (1) 获取时间戳

```python
>>> import time
>>> # 输出时间戳
>>> print(time.time())
1663914295.8337312
```

时间戳单位最适于做日期运算。但是1970年之前的日期就无法以此表示了。太遥远的日期也不行，UNIX和Windows只支持到2038年。

##### (2) 获取本地时间

```python
import time
 
localtime = time.localtime(time.time())
print("本地时间为 :", localtime)
```

运行结果

```python
本地时间为 : time.struct_time(tm_year=2022, tm_mon=9, tm_mday=23, tm_hour=14, tm_min=27, tm_sec=46, tm_wday=4, tm_yday=266, tm_isdst=0)
```

##### (3) 获取格式化时间

```python
import time
 
localtime = time.asctime( time.localtime(time.time()) )
print("当前本地时间 :", localtime)
```

运行结果

```python
当前本地时间 : Fri Sep 23 14:27:29 2022
```

##### (4) 格式化日期

我们可以使用 time 模块的 strftime 方法来格式化日期，：

```python
time.strftime(format[, t])
```

```python
import time
 
# 格式化成2016-03-20 11:45:39形式
print(time.strftime("%Y-%m-%d %H:%M:%S", time.localtime()))
 
# 格式化成Sat Mar 28 22:24:24 2016形式
print(time.strftime("%a %b %d %H:%M:%S %Y", time.localtime()))
  
# 将格式字符串转换为时间戳
a = "Sat Mar 28 22:24:24 2016"
print(time.mktime(time.strptime(a,"%a %b %d %H:%M:%S %Y")))
```

输出结果

```python
2022-09-23 14:28:41
Fri Sep 23 14:28:41 2022
1459175064.0
```

#### 2.2.2 calendar模块

##### (1) 获取日历

```python
import calendar  
  
cal = calendar.month(202, 11)  
print("以下输出2022年11月份的日历:")  
print(cal)
```

运行结果

```python
以下输出2022年11月份的日历:
    November 202
Mo Tu We Th Fr Sa Su
 1  2  3  4  5  6  7
 8  9 10 11 12 13 14
15 16 17 18 19 20 21
22 23 24 25 26 27 28
29 30
```

## Reference

- 模块
	- [Python导入模块，Python import用法（超级详细）](http://c.biancheng.net/view/2397.html)
- 文件处理
	- [Python文件处理os模块介绍](https://blog.csdn.net/qq_39611230/article/details/102811367)
- 时间日期
	- [Python 日期和时间 | 菜鸟教程](https://www.runoob.com/python/python-date-time.html)

# 第八章 Python 包

实际开发中，一个大型的项目往往需要使用成百上千的 Python 模块，如果将这些模块都堆放在一起，势必不好管理。而且，使用模块可以有效避免变量名或函数名重名引发的冲突，但是如果模块名重复怎么办呢？因此，Python提出了包（Package）的概念。

什么是包呢？简单理解，包就是文件夹，只不过在该文件夹下必须存在一个名为`__init__.py` 的文件。

> 注意，这是 Python 2.x 的规定，而在 Python 3.x 中，__init__.py 对包来说，并不是必须的。

每个包的目录下都必须建立一个 `__init__.py` 的模块，可以是一个空模块，可以写一些初始化代码，其作用就是告诉 Python 要将该目录当成包来处理。

> 注意，__init__.py 不同于其他模块文件，此模块的模块名不是 __init__，而是它所在的包名。例如，在 settings 包中的 __init__.py 文件，其模块名就是 settings。

包是一个包含多个模块的文件夹，它的本质依然是模块，因此包中也可以包含包

### 1. 创建包

创建包分为以下两步骤

1.  新建一个文件夹，文件夹的名称就是新建包的包名；
2.  在该文件夹中，创建一个 `__init__.py` 文件（前后各有 2 个下划线‘`_`’），该文件中可以不编写任何代码。当然，也可以编写一些 [Python](http://c.biancheng.net/python/) 初始化代码，则当有其它程序文件导入包时，会自动执行该文件中的代码（本节后续会有实例）。

如下操作, 创建一个文件名为 `first_pack`, 文件夹内新建文件 `__init__.py` 内容如下

```python
'''  
创建的第一个 python 包  
'''  
print('打印输出 first_pack')
```

可以看到，`__init__.py` 文件中，包含了 2 部分信息，分别是此包的说明信息和一条 print 输出语句。

由此，我们就成功创建好了一个 Python 包。

创建好包之后，我们就可以向包中添加模块（也可以添加包）。这里给 firstPack 包添加 2 个模块，分别是 module1.py、module2.py，各自包含的代码分别如下所示：

module1.py

```python
def display(arc):
    print(arc)
```

module2.py

```python
class CLanguage:
    def display(self):
        print("module2 output content")
```

当前目录结构也就是

firstPack
     ┠── `__init__.py`
     ┠── module1.py
     ┗━━ module2.py

### 2. 导入包

通过前面的学习我们知道，包其实本质上还是模块，因此导入模块的语法同样也适用于导入包。无论导入我们自定义的包，还是导入从他处下载的第三方包，导入方法可归结为以下 3 种：

1.  `import 包名[.模块名 [as 别名]]`
2.  `from 包名 import 模块名 [as 别名]`
3.  `from 包名.模块名 import 成员名 [as 别名]`

用 [] 括起来的部分，是可选部分，即可以使用，也可以直接忽略

> 注意，导入包的同时，会在包目录下生成一个含有 `__init__.cpython-36.pyc` 文件的 `__pycache__` 文件夹。

#### 2.1 import 包名[.模块名 [as 别名]]

接下来, 在项目目录创建 pack.py , 内容如下

```python
import first_pack.module1  
first_pack.module1.display("module1! 输出吧!")
```

输出结果

```python
打印输出 first_pack
module1! 输出吧!
```

可以看到，通过此语法格式导入包中的指定模块后，在使用该模块中的成员（变量、函数、类）时，需添加“包名.模块名”为前缀。

当然，如果使用 as 给包名.模块名”起一个别名的话，就使用直接使用这个别名作为前缀使用该模块中的方法了，例如：

```python
import first_pack.module1 as a
a.display("module1! 输出吧!")
```

另外，当直接导入指定包时，程序会自动执行该包所对应文件夹下的 `__init__.py` 文件中的代码。例如：

```python
import first_pack
first_pack.module1.display(" 看看__init__.py 的输入结果")
```

直接导入包名，并不会将包中所有模块全部导入到程序中，它的作用仅仅是导入并执行包下的 `__init__.py` 文件，因此，运行该程序，在执行 `__init__.py` 文件中代码的同时，还会抛出 AttributeError 异常（访问的对象不存在）：

```python
AttributeError: module 'firstPack' has no attribute 'module1'
打印输出 first_pack
```

我们知道，包的本质就是模块，导入模块时，当前程序中会包含一个和模块名同名且类型为 module 的变量，导入包也是如此：

```python
import first_pack
print(first_pack)  
print(first_pack.__doc__)  
print(type(first_pack))
```

输出结果

```python
打印输出 first_pack
<module 'first_pack' from '/Users/kylin/Projects/Python/first_pack/__init__.py'>

创建的第一个 python 包

<class 'module'>
```

####  2.2 from 包名 import 模块名 [as 别名]

仍以导入 first_pack 包中的 module1 模块为例，使用此语法格式的实现代码如下：

```python
from first_pack import module1
module1.display('输出把! module1!')
```

输出结果

```python
打印输出 first_pack
输出把! module1!
```

可以看到，使用此语法格式导入包中模块后，在使用其成员时不需要带包名前缀，但需要带模块名前缀。

当然，我们也可以使用 as 为导入的指定模块定义别名，例如：

```python
from first_pack import module1 as m1
m1.display('输出把! module1!')
```

输出结果同上

```python
打印输出 first_pack
输出把! module1!
```

同样，既然包也是模块，那么这种语法格式自然也支持 `from 包名 import *` 这种写法，它和 import 包名 的作用一样，都只是将该包的 `__init__.py` 文件导入并执行。

#### 2.3 from 包名.模块名 import 成员名 [as 别名]

此语法格式用于向程序中导入“包.模块”中的指定成员（变量、函数或类）。通过该方式导入的变量（函数、类），在使用时可以直接使用变量名（函数名、类名）调用，例如：

```python
from first_pack.module1 import display  
display("精简的输出 module!")
```

输出结果

```python
打印输出 first_pack
精简的输出 module!
```

当然，也可以使用 as 为导入的成员起一个别名，例如：

```python
from first_pack.module1 import display  as d
d("精简的输出 module!")
```

输出结果依然同上

```python
打印输出 first_pack
精简的输出 module!
```

另外，在使用此种语法格式加载指定包的指定模块时，可以使用 * 代替成员名，表示加载该模块下的所有成员。例如：

```python
from first_pack.module1 import *
display("导入所有模块时候输 module1!")
```

运行结果

```python
打印输出 first_pack
导入所有模块时候输 module1!
```

## Reference

[Python包（存放多个模块的文件夹）](http://c.biancheng.net/view/4667.html)

# 第九章 Python 异常处理

## 0. 异常处理概述

### 0.1 Python语法错误

语法错误，也就是解析代码时出现的错误。当代码不符合 Python 语法规则时，Python解释器在解析时就会报出 SyntaxError 语法错误，与此同时还会明确指出最早探测到错误的语句。例如：

```python
print "Hello,World!"
```

我们知道，Python 3 已不再支持上面这种写法，所以在运行时，解释器会报如下错误：

```python
SyntaxError: Missing parentheses in call to 'print'. Did you mean print(...)?
```

语法错误多是开发者疏忽导致的，属于真正意义上的错误，是解释器无法容忍的，因此，只有将程序中的所有语法错误全部纠正，程序才能执行。

### 0.2 Python运行时错误

运行时错误，即程序在语法上都是正确的，但在运行时发生了错误。例如：

```python
a = 1/0
```

上面这句代码的意思是“用 1 除以 0，并赋值给 a 。因为 0 作除数是没有意义的，所以运行后会产生如下错误：

```python
>>> a = 1/0  
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero
```

以上运行输出结果中，前两段指明了错误的位置，最后一句表示出错的类型。在 Python 中，把这种运行时产生错误的情况叫做**异常（Exceptions）**。这种异常情况还有很多，常见的几种异常情况参考 [什么是异常处理，Python常见异常类型（入门必读）](http://c.biancheng.net/view/4593.html)

> 提示：表中的异常类型不需要记住，只需简单了解即可。

当一个程序发生异常时，代表该程序在执行时出现了非正常的情况，无法再执行下去。默认情况下，程序是要终止的。如果要避免程序退出，可以使用捕获异常的方式获取这个异常的名称，再通过其他的逻辑代码让程序继续运行，这种根据异常做出的逻辑处理叫作异常处理。

开发者可以使用异常处理全面地控制自己的程序。异常处理不仅仅能够管理正常的流程运行，还能够在程序出错时对程序进行必的处理。大大提高了程序的健壮性和人机交互的友好性。

那么，应该如何捕获和处理异常呢？可以使用 try 语句来实现。有关 try 语句的语法和用法，会在后续章节继续详解。

## 1. 捕获异常

### 1.1 try except 捕获异常

Python 中，用try except语句块捕获并处理异常，其基本语法结构如下所示：

```python
try:  
    可能产生异常的代码块  
except [ (Error1, Error2, ... ) [as e] ]:  
    处理异常的代码块1  
except [ (Error3, Error4, ... ) [as e] ]:  
    处理异常的代码块2  
except  [Exception]:  
    处理其它异常
```

该格式中，[] 括起来的部分可以使用，也可以省略。其中各部分的含义如下：

-   (Error1, Error2,...) 、(Error3, Error4,...)：其中，Error1、Error2、Error3 和 Error4 都是具体的异常类型。显然，一个 except 块可以同时处理多种异常。
-   [as e]：作为可选参数，表示给异常类型起一个别名 e，这样做的好处是方便在 except 块中调用异常类型（后续会用到）。
-   [Exception]：作为可选参数，可以代指程序可能发生的所有异常情况，其通常用在最后一个 except 块。

从`try except`的基本语法格式可以看出，try 块有且仅有一个，但 except 代码块可以有多个，且每个 except 块都可以同时处理多种异常。

> 当程序发生不同的意外情况时，会对应特定的异常类型，Python 解释器会根据该异常类型选择对应的 except 块来处理该异常。

try except 语句的执行流程如下：

1.  首先执行 `try` 中的代码块，如果执行过程中出现异常，系统会自动生成一个异常类型，并将该异常提交给 Python 解释器，此过程称为捕获异常。
2.  当 Python 解释器收到异常对象时，会寻找能处理该异常对象的 `except` 块，如果找到合适的 except 块，则把该异常对象交给该 except 块处理，这个过程被称为处理异常。如果 Python 解释器找不到处理异常的 except 块，则程序运行终止，Python 解释器也将退出。

事实上，不管程序代码块是否处于 try 块中，甚至包括 except 块中的代码，只要执行该代码块时出现了异常，系统都会自动生成对应类型的异常。但是，如果此段程序没有用 try 包裹，又或者没有为该异常配置处理它的 except 块，则 Python 解释器将无法处理，程序就会停止运行；反之，如果程序发生的异常经 try 捕获并由 except 处理完成，则程序可以继续执行。

示例

```python
try:  
    a = int(input("输入被除数："))  
    b = int(input("输入除数："))  
    c = a / b  
    print("您输入的两个数相除的结果是：", c)  
except (ValueError, ArithmeticError):  
    print("程序发生了数字格式异常、算术异常之一")  
except:  
    print("未知异常")  
print("程序继续运行")
```

输入字母后输出结果

```python
输入被除数：a
程序发生了数字格式异常、算术异常之一
程序继续运行
```

上面程序中，第 6 行代码使用了 `(ValueError, ArithmeticError)` 来指定所捕获的异常类型，这就表明该 except 块可以同时捕获这 2 种类型的异常；第 8 行代码只有 except 关键字，并未指定具体要捕获的异常类型，这种省略异常类的 except 语句也是合法的，它表示可捕获所有类型的异常，一般会作为异常捕获的最后一个 except 块。

除此之外，由于 try 块中引发了异常，并被 except 块成功捕获，因此程序才可以继续执行，才有了“程序继续运行”的输出结果。

### 1.2 获取特定异常的有关信息

通过前面的学习，我们已经可以捕获程序中可能发生的异常，并对其进行处理。但是，由于一个 except 可以同时处理多个异常，那么我们如何知道当前处理的到底是哪种异常呢？

其实，每种异常类型都提供了如下几个属性和方法，通过调用它们，就可以获取当前处理异常类型的相关信息：  

-   args：返回异常的错误编号和描述字符串；
-   str(e)：返回异常信息，但不包括异常信息的类型；
-   repr(e)：返回较全的异常信息，包括异常信息的类型。

示例

```python
try:
    1/0
except Exception as e:
    # 访问异常的错误编号和详细信息
    print(e.args)
    print(str(e))
    print(repr(e))
```

输出结果

```python
('division by zero',)
division by zero
ZeroDivisionError('division by zero')
```

> 除此之外，如果想要更加详细的异常信息，可以使用 traceback 模块。有兴趣的读者，可自行查阅资料学习。

从程序中可以看到，由于 except 可能接收多种异常，因此为了操作方便，可以直接给每一个进入到此 except 块的异常，起一个统一的别名 e。

在 Python 2.x 的早期版本中，除了使用 as e 这个格式，还可以将其中的 as 用逗号（，）代替。

## 2. try...else...finaly 结构

### 2.1 try except else

在原本的 `try except` 结构的基础上，Python 异常处理机制还提供了一个 else 块，也就是原有 try except 语句的基础上再添加一个 else 块，即 `try except else` 结构。

使用 else 包裹的代码，只有当 try 块没有捕获到任何异常时，才会得到执行；反之，如果 try 块捕获到异常，即便调用对应的 except 处理完异常，else 块中的代码也不会得到执行。

示例

```python
try:
    result = 20 / int(input('请输入除数:'))
    print(result)
except ValueError:
    print('必须输入整数')
except ArithmeticError:
    print('算术错误，除数不能为 0')
else:
    print('没有出现异常')
print("继续执行")
```

输出结果

```python
# 输入 0
请输入除数:0
算术错误，除数不能为 0
继续执行

# 输入字母
请输入除数:a
必须输入整数
继续执行

# 输入正常除数
请输入除数:5
4.0
没有出现异常
继续执行
```

如上所示，当我们输入正确的数据时，try 块中的程序正常执行，Python 解释器执行完 try 块中的程序之后，会继续执行 else 块中的程序，继而执行后续的程序。

既然 Python 解释器按照顺序执行代码，那么 else 块有什么存在的必要呢？直接将 else 块中的代码编写在 try except 块的后面，不是一样吗？

当然不一样，现在再次执行上面的代码：

```python
请输入除数:a  
必须输入整数  
继续执行
```

可以看到，当我们试图进行非法输入时，程序会发生异常并被 try 捕获，Python 解释器会调用相应的 except 块处理该异常。但是异常处理完毕之后，Python 解释器并没有接着执行 else 块中的代码，而是跳过 else，去执行后续的代码。

也就是说，else 的功能，只有当 try 块捕获到异常时才能显现出来。在这种情况下，else 块中的代码不会得到执行的机会。而如果我们直接把 else 块去掉，将其中的代码编写到 try except 的后面：

```python
try:  
    result = 20 / int(input('请输入除数:'))  
    print(result)  
except ValueError:  
    print('必须输入整数')  
except ArithmeticError:  
    print('算术错误，除数不能为 0')  
print('没有出现异常')  
print("继续执行")
```

输出结果

```python
请输入除数:a
必须输入整数
没有出现异常
继续执行
```

可以看到，如果不使用 else 块，try 块捕获到异常并通过 except 成功处理，后续所有程序都会依次被执行。

### 2.2 try except finaly 资源回收

Python 异常处理机制还提供了一个 `finally` 语句，通常用来为 try 块中的程序做扫尾清理工作。

> 注意，和 else 语句不同，finally 只要求和 try 搭配使用，而至于该结构中是否包含 except 以及 else，对于 finally 不是必须的（else 必须和 try except 搭配使用）。

在整个异常处理机制中，finally 语句的功能是：**无论 try 块是否发生异常，最终都要进入 finally 语句，并执行其中的代码块。**

基于 finally 语句的这种特性，在某些情况下，当 try 块中的程序打开了一些物理资源（文件、数据库连接等）时，由于这些资源必须手动回收，而回收工作通常就放在 finally 块中。

> Python 垃圾回收机制，只能帮我们回收变量、类对象占用的内存，而无法自动完成类似关闭文件、数据库连接等这些的工作。

回收这些物理资源，并非必须使用 finally 块, 但使用 finally 块是比较好的选择。

首先，try 块不适合做资源回收工作，因为一旦 try 块中的某行代码发生异常，则其后续的代码将不会得到执行；

其次 except 和 else 也不适合，它们都可能不会得到执行。而 finally 块中的代码，无论 try 块是否发生异常，该块中的代码都会被执行。

示例

```python
try:
    a = int(input("请输入 a 的值:"))
    print(20/a)
except:
    print("发生异常！")
else:
    print("执行 else 块中的代码")   
finally :
    print("执行 finally 块中的代码")
```

输入正常整除数的输出结果

```python
# 输入整除数
请输入 a 的值:5
4.0
执行 else 块中的代码
执行 finally 块中的代码
```

可以看到，当 try 块中代码未发生异常时，except 块不会执行，else 块和 finally 块中的代码会被执行。

输入 a 或 0 的结果

```python
请输入 a 的值:a
发生异常！
执行 finally 块中的代码

请输入 a 的值:0
发生异常！
执行 finally 块中的代码
```

可以看到，当 try 块中代码发生异常时，except 块得到执行，而 else 块中的代码将不执行，finally 块中的代码仍然会被执行。

finally 块的强大还远不止此，即便当 try 块发生异常，且没有合适和 except 处理异常时，finally 块中的代码也会得到执行。例如：

```python
try:
    #发生异常
    print(20/0)
finally :
    print("执行 finally 块中的代码")
```

输出结果

```python
Traceback (most recent call last):
  File "/Users/kylin/Projects/Python/tru.py", line 3, in <module>
    print(20/0)
ZeroDivisionError: division by zero
执行 finally 块中的代码
```

可以看到，当 try 块中代码发生异常，导致程序崩溃时，在崩溃前 Python 解释器也会执行 finally 块中的代码。

## 3. 自定义异常

实际开发中，有时候系统提供的异常类型不能满足开发的需求。这时候你可以通过创建一个新的异常类来拥有自己的异常。异常类继承自 Exception 类，可以直接继承，或者间接继承。

### 3.1 自定义异常类型

```python
# 1. 用户自定义异常类型
class TooLongException(Exception):  
    "this is user's Exception for check the length of name "  
  
    def __init__(self, length):  
        self.length = length  
  
    def __str__(self):  
        print("姓名长度是" + str(self.length) + "，超过长度了")
```


### 3.2 如何手动抛出异常：raise

```python
# 2.手动抛出用户自定义类型异常  
def input_name():  
    name = input("请输入你的名字:")  
    if len(name) > 6:  
        raise TooLongException(len(name))  # 抛出异常很简单，使用raise即可,但是没有处理，即捕捉  
    else:  
        print("Hello", name)
```

合并后执行代码如下

```python
#1.用户自定义异常类型
class TooLongExceptin(Exception):
    "this is user's Exception for check the length of name "
    def __init__(self,leng):
        self.leng = leng
    def __str__(self):
        print("姓名长度是"+str(self.leng)+"，超过长度了")
 
#2.手动抛出用户自定义类型异常
def name_Test():
        name = input("enter your naem:")
        if len(name)>4:
            raise TooLongExceptin(len(name))  #抛出异常很简单，使用raise即可,但是没有处理，即捕捉
        else :
            print(name)
 
#调用函数，执行
name_Test()
```

输出结果

```python
请输入你的名字:Kylinaaa
姓名长度是8，超过长度了
Traceback (most recent call last):
  File "/Users/kylin/Projects/Python/except.py", line 19, in <module>
    input_name()
  File "/Users/kylin/Projects/Python/except.py", line 15, in input_name
    raise TooLongException(len(name))  # 抛出异常很简单，使用raise即可,但是没有处理，即捕捉
__main__.TooLongException: <exception str() failed>
```

### 3.3 捕捉用户手动抛出的异常

```python
class TooLongException(Exception):  
    """ this is user's Exception for check the length of name """  
  
    def __init__(self, length):  
        self.length = length  
  
    def __str__(self):  
        print("姓名长度是" + str(self.length) + "，超过长度了")  
  
  
def input_name():  
    try:  
        name = input("请输入你的名字:")  
        if len(name) > 7:  
            raise TooLongException(len(name))  
        else:  
            print(name)  
  
    except TooLongException as e_result:  # 这里异常类型是用户自定义的  
        print("捕捉到异常了")  
        print("打印异常信息：", e_result)  
  
  
# 调用函数，执行  
input_name()
```

输出结果

```python
请输入你的名字:88888888
捕捉到异常了
Traceback (most recent call last):
  File "/Users/kylin/Projects/Python/tru.py", line 15, in input_name
    raise TooLongException(len(name))
__main__.TooLongException: <exception str() failed>

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "/Users/kylin/Projects/Python/except.py", line 25, in <module>
    input_name()
  File "/Users/kylin/Projects/Python/except.py", line 21, in input_name
    print("打印异常信息：", e_result)
TypeError: __str__ returned non-string (type NoneType)
打印异常信息： 姓名长度是8，超过长度了
姓名长度是8，超过长度了
```

## Reference

- [什么是异常处理，Python常见异常类型（入门必读）](http://c.biancheng.net/view/4593.html)
- [Python try except异常处理详解（入门必读）](http://c.biancheng.net/view/4599.html)
- [python自定义异常类型和raise抛出异常](https://blog.csdn.net/qq_26442553/article/details/81783223)

# 第十章 Python 文件操作

首先在当前目录新建 file.txt, 文件内容如下

```txt
1. 第一行的内容
2. 第二行的内容
3. 第三的内容格外的长
4. (短)
```

## 1. 打开文件

### 1.1 open

语法：`open(file, mode=‘r’, buffering=-1, encoding=None, errors=None, newline=None, closefd=True, opener=None)`

open中参数众多，但是我们常用的参数也就只有file，mode和encoding，接下来我们就来介绍一下这几个参数的作用

**file**: 

文件名或路径，这是open的必填参数，如果调用open最少你要说清你要打开那个文件。

**mode**:

| 模式 | 功能                                    |
|----|---------------------------------------|
| r  | 只读模式（如果不填写，则默认就是此模式）                  |
| w  | 覆盖写入模式（如果存在和写入文件同名文件则覆盖，不存在则新建）       |
| x  | 新建文件写入模式（如果存在和写入文件同名文件则报错，不存在则新建）     |
| a  | 追加写入模式（如果存在和写入文件同名文件则在文件内容后追加，不存在则新建） |
| b  | 二进制读取模式，此模式可以读取除纯文本之外的其他文件            |
| t  | 文本模式（默认打开模式）                          |

- + 扩展模式，可以扩展上述的模式，但必须要配合使用，比如：r+就扩展了只读模式，让这个模式既可读又可写

打开文件示例

```python
f = open('file.txt', 'r')
```

**mode拓展知识点**:

- w 以写方式打开，
- a 以追加模式打开 (从 EOF 开始, 必要时创建新文件)
- r+ 以读写模式打开
- w+ 以读写模式打开 (参见 w )
- a+ 以读写模式打开 (参见 a )
- rb 以二进制读模式打开
- wb 以二进制写模式打开 (参见 w )
- ab 以二进制追加模式打开 (参见 a )
- rb+ 以二进制读写模式打开 (参见 r+ )
- wb+ 以二进制读写模式打开 (参见 w+ )
- ab+ 以二进制读写模式打开 (参见 a+ )

- w+是打开后，清空原有内容，成为一个新的空文件，对这个空文件具有读写权限。
- r+是打开后，可以读取文件内容，保存原有内容，追加写内容，写动作则是追加的新内容。其作用和a+基本相同。

**encoding**:

文件的编码格式，如果不填写就只能读取ASCII格式的文件，读取中文的文件就会报错，如果想要读取中文，一般常用UTF-8。

### 1.1 with...as...

使用这个函数打开文件使用完后会自动关闭，让代码变得更简洁  

**语法：with open（） as 变量：**

```python
with open('file.txt', 'w') as f:
    name = 'My name xun_mi'
    f.write(name)
```

## 2. 操作文件

### 2.1 逐个读取

**语法：文件对象.read(size = -1)**

- read（）默认值是-1，会自动读取到最后一个值
- 可以给read指定一个值，read每次读取都会从上次读取结束的位置开始。换行符也算一个字符。
- 如果read指定的读取数量大于实际数量，这会读取所有文件。如果没有内容，会返回一个‘’空串

```python
f = open('file.txt', mode='r')  
  
content = f.read()  
  
for i in content:  
    print(i)
```

输出结果

```python
1. 第一行的内容
2. 第二行的内容
3. 第三的内容格外的长
4. (短)
```

> 或许你可以尝试一下如下代码输出结果

```python
f = open('file.txt', mode='r')  
  
content = f.read()  
  
for i in content:  
    print(i)
```

### 2.2 逐行读取

**语法：文件对象.readline()**  

每次读取一行内容。  

```python
f = open('file.txt', mode='r')  
  
print(f.readline())
```

输出结果

```python
1. 第一行的内容
```

> 或许你可以尝试一下如下代码输出结果

```python
f = open('file.txt', mode='r'')  
  
content = f.readline()  
  
for i in content:  
    print(i)
```

**语法：文件对象.readlines()**  

一行一行读取，并且会把每行内容自动封装到列表中。

```python
f = open('file.txt', mode='r')  
  
print(f.readlines())
```

输出结果

```python
['1. 第一行的内容\n', '2. 第二行的内容\n', '3. 第三的内容格外的长\n', '4. (短)']
```

> 或许你可以尝试一下如下代码输出结果

```python
f = open('file.txt', mode='r')  
  
content = f.readlines()  
  
for i in content:  
    print(i)
```

### 2.3 读取文件位置

**tell() 可以用来返回当前读取到的位置**

```python
f = open('file.txt', mode='r')
  
pos = f.tell()
print("当前位置: %d" % (pos))
```

输出结果

```python
当前位置: 0
```

**seek(参数1,参数2) 可以修改当前读取的位置**

参数 1 用于指定读取位置。

参数 2 为从哪开始指定位置

- 0 从头开始计数（默认），1从当前位置开始计数，2从最后位置开始计数。
- 第二个参数只能在b模式下改变。在b模式下seek参数一代表的为字节，在utf-8中一个中文字符等于三个字节

```python
f = open("file.txt", "r")

line = f.readline()
print(line)

# 重新设置文件读取指针到开头
f.seek(2, 0)
line = f.readline()
print(line)
```

输出结果

```python
1. 第一行的内容

 第一行的内容
```

### 2.4 写入内容

**语法：文件对象.write('内容')**

当文档处于w、x、a等写入模式的情况下才能使用write，否则会报错

write写入内容时会将写入的字数作为返回值返回

```python
f = open("file.txt", mode="w+")  
  
print(f.readline())  
  
content = "hacked"  
  
f.write(content)  
  
print(f.readline())
```

运行后 file.txt 文件内容

```python
hacked
```

## 3. 关闭文件

**语法：文件对象.close**

将使用完的文件及时关闭，能有利于提升程序性能。

```python
f.close()
```

## Reference

- [python的w+到底是什么](https://blog.csdn.net/longshenlmj/article/details/9921665)
- [Python文件处理os模块介绍](https://blog.csdn.net/qq_39611230/article/details/102811367)
- 拓展阅读:
	- [Python文件操作，看这篇就足够 - 知乎](https://zhuanlan.zhihu.com/p/56909212)