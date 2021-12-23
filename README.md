# Python_Notes
 
## 关于帮助
### 查看内置函数清单

> dir(\_\_builtins\_\_)

### 查看函数的帮助文档
> help()
> 
> 例如：
> 
> help(input)

### 查找本地文档
> 在IDLE环境按F1(英文文档)
> 
> [Python在线文档(有中文)](https://docs.python.org/zh-cn/3.10/index.html)

### 显示模块的所有属性和方法
> **dir(timeit)**
> 
> ['Timer', '\_\_all__', '\_\_builtins__', '\_\_cached__', '\_\_doc__', '\_\_file__', '\_\_loader__', '\_\_name__', '\_\_package__', '\_\_spec__', '_globals', 'default_number', 'default_repeat', 'default_timer', 'dummy_src_name', 'gc', 'itertools', 'main', 'reindent', 'repeat', 'sys', 'template', 'time', 'timeit']

### 打印该模块的帮助文档
> print(timeit.\_\_doc__)


### 显示模块所有的对外成员
> **timeit.\_\_all__**
> 
> ['Timer', 'timeit', 'repeat', 'default_timer']

> **编写较规范的一个通用模块时，建议都需要定义\_\_all__属性**

### 显示模块的源代码地址
> **timeit.\_\_file__**
> 
>'C:\\Users\\fg104\\AppData\\Local\\Programs\\Python\\Python310\\lib\\timeit.py'
>



## 关于字符串
### 原始字符串
> 字符串前面加一个r，例如：
> 
> r'C:\Users\fg104\Documents\GitHub\Python_Notes'

### 常用函数
#### 查找
> - **count(sub)**：统计sub字符串的出现次数(可以设置开始和结束位置)
> 
> - **find(sub)**：查找sub字符串的索引，找不到返回-1
> 
> - **index(sub)**：查找sub字符串的索引，找不到报错

#### 大小写处理
> - **capitalize()**：字符串首字母大写,其他字母小写
> 
> - **title()**：把字符串中的每个单词首字母改为大写
> 
> - **casefold()**：所有字母转为小写(不仅英语)
> 
> - **swapcase()**：大小写翻转
> 
> - **upper()**：所有的字母改为大写
> 
> - **lower()**：所有的字母改为小写(只针对英语)

#### 对齐
> - **center(width,fillchar='')**：居中
> 
> - **ljust(width,fillchar='')**:左对齐
> 
> - **rjust(width,fillchar='')**：右对齐
> 
> - **zfill(width)**：用0填充字符串的左侧

## 关于浮点数
> import decimal
> 
> a = decimal.Decimal('0.1')
> 
> b = decimal.Decimal('0.2')
> 
> a+b
> 
> Decimal('0.3')

## 关于变量

### 临时变量
> _
> 
> 只有当这个变量是临时的，一次性的，才建议用_

### 判断变量类型
> isinstance(object, classinfo)
> 
> 例如：
> 
> isinstance('abc',str)

### 全局变量无法在函数内修改

## 关于循环
> i = 1
> 
> while i < 5:
> 
> 　　print("循环内，i的值是",i)
> 
> 　　if i == 2:
> 
> 　　　　break
> 
> 　　i += 1
> 
> else:
> 
> 　　print("循环外，i的值是",i)
> 
> **当break出循环后，else语句将不会被执行**

## 列表list
### 增加元素
> listA.append()
> 
> listA.extend()
> 
> listA.insert()

### 删除元素
> listA.remove()
> 
> del listA[2]
> 
> listA.pop()

### 统计元素
> listA.count(item)

### 查元素的索引值
> listA.index(item)

### 排序以及反转
> listA.sort(reverse = False)
> 
> listA.reverse()

### 打包和解包
> _ = [4, '元素', 7]
> 
> a, b, c = _
> 
> a,b,c会分别等于_的三个元素

### 切片
> listA = ['a', 'b', 'c', 'd']
> 
> listB = listA # 等号是引用的形式
> 
> listC = listA[:] # [:]是一个副本，所以这个等号是赋值的形式

### 步进跨度
> a = [1,2,3,4,5]
> 
> a[0:5:2]
> 
> [1,3,5]

### 列表倒叙
> listA[::-1]

### 二维及以上的列表需要用深拷贝
> import copy
> 
> listB = copy.deepcopy(listA)

### 列表推导式
> **当需要对列表中的元素进行修改时**
> 
> listB = [i*2 for i in listA]
> 
> 新列表 = [(目标)表达式 for 目标 in 原列表]
> 
> 新列表 = [(目标)表达式 for 目标 in 原列表 if 表达式]

## 元组

元组中的列表是可以被修改的

## 条件分支和循环
### 条件表达式

> _ = a if a < b else b

## urllib.request常用操作
> import urllib.request
> 
> response = urllib.request.urlopen(urladdress)
> 
> html = response.read()
> 
> html = html.decode('utf-8')

## 随机数
> import random
> 
> num = random.randint(1,10)