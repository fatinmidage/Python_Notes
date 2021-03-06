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
> r'C:\Users\Documents\GitHub\Python_Notes'

### 常用函数
#### 查找
> - **str.count(sub)**：统计sub字符串的出现次数(可以设置开始和结束位置)
> 
> - **str.find(sub)**：查找sub字符串的索引，找不到返回-1
> 
> - **str.index(sub)**：查找sub字符串的索引，找不到报错

#### 替换
> - **str.expandtabs(4)**：用4个空格代替tab
> 
> - **str.replace(old,new,count=-1)**：

#### 截取
> - **str.lstrip(chars=None)**：删除左边的**字符**
> 
> - **str.rstrip(chars=None)**：删除右边的**字符**
> 
> - **str.strip(chars=None)**：删除左右的**字符**
> 
> 示例：
> 
> > \>\>\>"www.ilovefishc.com".lstrip(".w")
> >
> > \>\>\>'ilovefishc.com'
> >
> > \>\>\>"我爱中国".lstrip("爱我")
> >
> > \>\>\>'中国'
> 
> - **str.removeprefix(str)**：删除前缀指定**字符串**
> 
> - **str.removesuffix(str)**：删除后缀指定**字符串**

#### 分割
> - **str.split('.')**：分割字符串，str指定分割符

#### 拼接
> - **'.'.join(list[str])**：比“+”更有效率，与“+”结果一样

#### 判断
> - **str.startwith(suffix)**：判断字符串是否以suffix字符串开头
> 
> - **str.endwith(suffix)**：判断字符串是否以suffix字符串结尾
> 
> - **str.istitle()**：是否所有单词的首字母大写
> 
> - **str.isupper()**：是否所有字母都是大写
> 
> - **str.islower()**:是否所有字母都是小写
> 
> - **str.isalpha()**：字符串是否只有字母
> 
> - **str.isspace()**：字符串是否空表字符串(tab、\n也算是空白)
> 
> - **str.isprintable()**：字符串是否全都是可打印的字符
> 
> - **str.isdigit()**：是否是数字

#### 大小写处理
> - **str.capitalize()**：字符串首字母大写,其他字母小写
> 
> - **str.title()**：把字符串中的每个单词首字母改为大写
> 
> - **str.casefold()**：所有字母转为小写(不仅英语)
> 
> - **str.swapcase()**：大小写翻转
> 
> - **str.upper()**：所有的字母改为大写
> 
> - **str.lower()**：所有的字母改为小写(只针对英语)

#### 对齐
> - **str.center(width,fillchar='')**：居中
> 
> - **str.ljust(width,fillchar='')**:左对齐
> 
> - **str.rjust(width,fillchar='')**：右对齐
> 
> - **str.zfill(width)**：用0填充字符串的左侧

### 格式化字符串
> \>\>\>"1+2={},2的平方是{}".format(3,2\*2)
> 
> \>\>\>'1+2=3,2的平方是4'
> 
> \>\>\>'我叫{name},我爱{fav}'.format(name="小甲鱼",fav="小姐姐")
> 
> \>\>\>'我叫小甲鱼,我爱小姐姐'

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
> type(a)
> 
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

## 序列(元组、字符串和序列的统称)
### 常用方法(BIF)
> - **list()**：把一个序列转换成列表
> 
> - **tuple()**：把一个序列转换成元组
> 
> - **str()**：把一个序列转换成字符串
> 
> - **min()**：返回序列中最小的那个值
> 
> - **max()**：返回序列中最大的那个值
> 
> - **len()**：返回序列的个数
> 
> - **sum()**：求和
> 
> - **sorted()**：排序,返回新的列表
> 
> - **reversed()**：翻转，返回一个反向迭代器，需要用转换函数才能得到新序列，例如：
> 
> >\>\>\> list(reversed(listA))
> 
> - **all()**：是否所有元素均为真
> 
> - **any()**：是否有一个元素为真
> 
> - **enumerate()**：通过一个列表创建一个枚举对象(二维数组，默认从0开始)，需要用转换函数才能得到新序列，例如：
> 
> > \>\>\> list(enumerate(listA))
> 
> - **zip()**：将多个序列打包成多维序列
> 
> - **map()**：返回函数的结果打包成的一个迭代器，需要用转换函数才能得到新序列，例如：
> 
>> \>\>\> list(map(ord,'fish'))
>>
>> \>\>\> [102, 105, 115, 104]
>
> - **filter()**：过滤结果为真的元素，需要用转换函数才能得到新序列，例如：
> 
>> \>\>\> list(filter(str.islower,'Fish'))
>>
>> \>\>\> ['i', 's', 'h']

## 迭代器和可迭代对象
- 迭代器是一次性的
- 可迭代对象是可循环使用的
- next()

## 字典
### 常用方法
> - **dict.fromkeys(可迭代对象，值)**：用迭代对象生成字典
> 
> - **dictA.pop(key)**：弹出元素
> 
> - **dictA.popitem()**：弹出最新加进来的那个元素
> 
> - **del()**：删除对象
> 
> - **dictA.clear()**：清空字典
> 
> - **update()**：更新字典
> 
>> \>\>\> dictA.update({A:1,B:2})
>>
>> \>\>\> dictA.update(A=1,B=2)
>
> - **dictA.get(key,str)**：返回指定键的值，如果没有指定键，返回str
> 
> - **dictA.setdefault(key,default)**：返回指定键的值，如果没有，用default新建一个键值对，并返回default
> 
> - **dictA.keys()**：返回键
> 
> - **dictA.values()**：返回值
> 
> - **dictA.itmes()**：返回键值对

## 集合
### 常用函数，方法
> - **in 和 not in**
> - **因为是无序的，所以不能用下标访问**
> - **len(setA) == len(set(listA))**：用于判断列表是否有重复元素

## 条件分支和循环
### 条件表达式

> _ = a if a < b else b

## 函数
### 收集参数(打包参数)
> \>\>\> def myfun(**\*args**):
> 
> \>\>\> 　　print(f'有{len(args)}个参数，第二个参数是{args[1]}')
> \>\>\> 
> 
> \>\>\> myfun(1,'a',4)
> 
> \>\>\> 有3个参数，第二个参数是a
> 
> **收集参数实际上是将多个参数打包成一个元组传递给函数**
> 
> **此外，还可以用\*\*，将多个参数打包成字典给函数，例如：**
> 
> \>\>\> def myfun(**kwargs):
> 
> \>\>\> 　　return kwargs
>
> \>\>\>
> 
> \>\>\> myfun(a=1,b='2')
> 
> \>\>\> {'a': 1, 'b': '2'}

## 解包参数
> def myfun(a,b,c):
> 
> 　　pass
> 
> 
> args = ('a',2,'4')
> 
> myfun(*args)


### 多个返回值
> 函数可以具有多个返回值，但实际上函数是把它们打包成一个元组
> 
> \>\>\> def myfun():
> 
> \>\>\> 　　return 1,2,3
> 
> \>\>\>
> 
> \>\>\> x,y,z = myfun()


## 随机数
> import random
> 
> num = random.randint(1,10)