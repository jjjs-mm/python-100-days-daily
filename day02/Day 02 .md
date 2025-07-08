# 🏷 Day 02 - Python 基础学习

## ✅ 今日目标

第一行代码的输入，变量以及运算符的学习

## 💡 学习内容

### ***知识点总结***

学习了输入输出，变量有关进制、浮点数、变量加减、变量类型和**强制转换**，还有运算符有关算术运算符、赋值运算符、逻辑运算符等等。

- 变量有关知识点
    
    浮点数科学计数法可以用e来表示，比如1.234e2=123.4；
    
    变量类型：int float str bool
    
    强制类型转换比较复杂，主要包括四种如int(),float(),chr(),ord()，其中chr()和ord()作用相反：`ord()：将（一个字符的）字符串转换成对应的整数（字符编码）`
    
- 运算符相关知识点
    
    算术运算符：/表示除法，//表示整除，**表示幂（比如r**2表示半径的平方）
    
    赋值运算符：`赋值运算构成的表达式本身不产生任何值,引入海象运算符:=`可以表示值
    
    逻辑运算符：and or not判断True和False
    
- 三个运算符相关应用
    
    易错点提醒：a = float(input('请输入华氏温度: '))，有input和print内是单引号’’
    
    pi有库，引用math库，用math.pi
    

### 难点、易错点

1. win和macos在终端输入的不一样，mac在终端上输入的是python3 --version
2. 强制类型转换的部分，`str`类型转`int`类型时可以通过`base`参数来指定进制，可以将字符串视为对应进制的整数进行转换。`str`类型转成`bool`类型时，只要字符串有内容，不是`''`或`""`，对应的布尔值都是`True`。`bool`类型转`int`类型时，`True`会变成`1`，`False`会变成`0`。在 ASCII 字符集和 Unicode 字符集中， 字符`'d'`对应的编码都是`100`。
3. 两个逻辑运算符 and和or的短路原理：and左侧布尔值是False则忽略右侧的布尔值，or左侧布尔值是True忽略右侧布尔值。

## ✍️ 代码/笔记

```python
"""Day 02 code
"""
print("Hello World")
print("Goodbye, World")
#第一行python代码,第一行注释
"""hhhhhh哇塞哇塞我来也"""

"""Day 03 code
"""
#进制
print("这几进制来着？")
print(0b100)   #2进制
print(0o100)   #8进制
print(100)     #10进制
print(0x100)   #16进制
#浮点数
print(123.45)
print(1.2345e2)#科学计数法
#变量使用
print("ohmy，这不是变量加减乘除嚒！")
a=34
b=5
print(a,b)
print(a+b)
print(a-b)
print(a*b)
print(a/b)
print(a%b)

#查看变量类型
print("阿嘞啊嘞，大小姐请查看一下变量类型！")
a=100
b=3.22
c="hello world"
d=True
print(type(a))
print(type(b))
print(type(c))
print(type(d))

#变量强制转换
print("¥变量强制爱环节¥")
a = 100
b = 123.45
c = '123'
d = '100'
e = '123.45'
f = 'hello, world'
g = True
print(float(a))
print(int(b))
print(int(c))
print(int(c,base=16))   # 这个我之前确实没见过，str类型的'123'按十六进制转成int，输出291
print(int(d,base=2))    # 二进制转化成int
print(float(e))
print(bool(f))
print(int(g))           # bool类型的True转成int，输出1
print(chr(a))           # int类型的100转成str，输出'd'
"""char不是字符么，应该是ASCII码的锅"""
print(ord('d'))         # str类型的'd'转成int，输出100
"""ord()：将（一个字符的）字符串转换成对应的整数（字符编码）
   chr()和ord刚好功能相反
"""

"""Day 04 code

"""
#算术运算符
print(321 / 12)     # 除法运算，输出26.75
print(321 // 12)    # 整除运算，输出26
"""这一部分和c++和java不太一样，/除法结果可以用小数表示"""

print("体验一下优先级")
print(123+4*3)
print((123+4)*3)

#赋值运算符
"""赋值运算构成的表达式本身不产生任何值,引入海象运算符"""
#print(a=10)  不注释掉会生成 SyntaxError: invalid syntax
print(a:=10)

#运算符应用
"""例子1：华氏温度转摄氏温度
   要求：输入华氏温度将其转换为摄氏温度，华氏温度到摄氏温度的转换公式为： C=(F−32)/1.8。"""

a = float(input('请输入华氏温度: '))
b=(a-32)/1.8
print(f'{a:.1f}华氏度 = {b:.1f}摄氏度')    #第二种格式化
print('%.1f华氏度 = %.1f摄氏度' % (a, b))  #格式化输出，用%。1f占位符表示一位小数输出

"""例子2：计算圆的周长和面积
要求：输入一个圆的半径（$\small{r}$），计算出它的周长（ 2πr ）和面积（ πr**2）。"""
import math
r=float(input("请输入一个圆的半径："))
C = 2 * math.pi * r
S = math.pi *(r**2)
print('半径为%.1f的圆周长为 %.2f ,面积为 %.2f '%(r,C,S))

"""例子3：判断闰年
要求：输入一个 1582 年以后的年份，判断该年份是不是闰年。"""
year=int(input('输入一个 1582 年以后的年份：'))
if(year % 4 == 0 and year % 100 != 0 or year % 400 == 0):
    print('%d是闰年'%year)
else:
    print('%d不是闰年'%year)

```