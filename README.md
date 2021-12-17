# Python_Notes
 
## 查看内置函数清单

> dir(\_\_builtins\_\_)

## 查看内置函数的帮助文档
> help()
> 
> 例如：
> 
> help(input)

## 查找本地文档
> 在IDLE环境按F1(英文文档)
> 
> [Python在线文档(有中文)](https://docs.python.org/zh-cn/3.10/index.html)


## 原始字符串
> 字符串前面加一个r，例如：
> 
> r'C:\Users\fg104\Documents\GitHub\Python_Notes'

## 判断变量类型
> isinstance(object, classinfo)
> 
> 例如：
> 
> isinstance('abc',str)

## 添加列表元素的三种方法
> listA.append()
> 
> listA.extend()
> 
> listA.insert()

## 删除列表元素的三种方法
> listA.remove()
> 
> del listA[2]
> 
> listA.pop()

## 列表切片
> listA = ['a', 'b', 'c', 'd']
> 
> listB = listA # 等号是引用的形式
> 
> listC = listA[:] # [:]是一个副本，所以这个等号是赋值的形式
> 
> del listA[2]
> 
> listA
> 
> ['a', 'b', 'd']
> 
> listB
> 
> ['a', 'b', 'd'] # listB引用的形式，所以listB也是跟着改变的
> 
> listC
> 
> ['a', 'b', 'c', 'd'] # listC是值的形式，不受影响

## 函数的文档属性
> func.\_\_doc\_\_

## 函数文档，会比直接调用__doc__属性更可读
> help(func)

## 全局变量无法在函数内修改，强制修改只会在函数内创建一个同名的局部变量

## 关于帮助
> **dir(timeit)**
> 
>['Timer', '\_\_all__', '\_\_builtins__', '\_\_cached__', '\_\_doc__', '\_\_file__', '\_\_loader__', '\_\_name__', '\_\_package__', '\_\_spec__', '_globals', 'default_number', 'default_repeat', 'default_timer', 'dummy_src_name', 'gc', 'itertools', 'main', 'reindent', 'repeat', 'sys', 'template', 'time', 'timeit']
>
> 显示模块的所有属性和方法

> **timeit.\_\_all__**
> 
>['Timer', 'timeit', 'repeat', 'default_timer']
>
>显示模块所有的对外成员

>**编写较规范的一个通用模块时，建议都需要定义\_\_all__属性**
>
>**timeit.\_\_file__**
>
>'C:\\Users\\fg104\\AppData\\Local\\Programs\\Python\\Python310\\lib\\timeit.py'
>
>显示模块的源代码地址
