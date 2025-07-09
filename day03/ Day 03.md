# 🏷 Day 03 - 条件判断与循环

# ✅ 今日目标

- 学习条件判断和循环的基础知识

# 💡 学习内容

## 知识点总结

- ***分支结构***
    
    if elif 最后一个才是else
    
    match-case常用形式：
    
    status_code = int(input('响应状态码: '))
    match status_code:
    case 400 | 405: description = 'Invalid Request'
    case 401 | 403 | 404: description = 'Not Allowed'
    case 418: description = 'I am a teapot'
    case 429: description = 'Too many requests'
    case _: description = 'Unknown Status Code'
    print('状态码描述:', description)
    
- ***循环结构***
    
    while True:             # 可一直循环
    
    for i in range(101)  # 0~100范围内整数，*注意range里左闭右开*
    
    range (1,100,2)       #1取到 100取不到 范围内奇数
    
    知道循环次数用for，不知道循环次数用while
    

## 难点、易错点

- continue和break的区别
    
    break可以直接跳出循环，而continue跳出这一次循环，直接进行下一次循环
    
- range使用
    
    左闭右开，且步幅可以是负数也可以是正数
    

# ✍️ 代码/笔记

```python
#Day 05小练习

""""example01:分段函数求值"""
print('这是一个分段函数求值的小问题')
x=float(input('请输入x值：'))
if x<-1:
    y = 5*x+3
elif x>1:
    y = 3*x-5
else:
    y = x+2
print('所得y值为：%.1f'%y)

"""example02:百分制成绩转换成等级"""
score=float(input('请输入你的成绩：'))
if score >= 90:
    print('A')
elif score >= 80:
    print('B')
elif score >= 70:
    print('C')
elif score >= 60:
    print('D')
else:
    print('E')

"""example03:计算三角形的周长和面积
"""
import math
print('请输入三条边判断三角形')
a=float(input('a='))
b=float(input('b='))
c=float(input('c='))
if a+b>c and a+c>b and b+c>a:
    C = a+b+c
    s = C/2
    area = math.sqrt(s*(s-a)*(s-b)*(s-c))
    print('该三条边能生成三角形，该三角形周长为%.1f，面积为%.2f'%(C,area))
else:
    print('该三条边不能生成三角形')

#Day 06练习
"""example01:判断素数
要求：输入一个大于 1 的正整数，判断它是不是素数。"""
import math
print('来判断素数')
x=int(input('请输入一个整数：'))
end=int(math.sqrt(x))
is_Prime=True
for i in range(2,end+1):
    if  x%i==0:
        is_Prime=False
        break
if is_Prime:
    print('%d是素数'%x)
else:
    print('%d不是素数'%x)

"""example02:最大公约数
要求：输入两个大于 0 的正整数，求两个数的最大公约数。

提示：两个数的最大公约数是两个数的公共因子中最大的那个数。"""
print('最大公因子是多大，对了说到大，你那里……')
a=int(input('a='))
b=int(input('b='))
y=1     #公因子从1开始
if a>b:
    for i in range(b,1,-1):
        if b%i==0 and a%i==0:
            y=i
            break
else:
    for i in range(a,1,-1):
        if a%i==0 and b%i==0:
            y=i
            break
print('这两个数的最大公因子为%d'%y)
"""
x = int(input('x = '))
y = int(input('y = '))
for i in range(x, 0, -1):
    if x % i == 0 and y % i == 0:
        print(f'最大公约数: {i}')
        break
这个版本是把最外层if-else去掉更简洁
"""

"""
欧几里得算法求最大公约数：
x = int(input('x = '))
y = int(input('y = '))
while y % x != 0:
    x, y = y % x, x
print(f'最大公约数: {x}')
"""

"""example03:猜数字游戏
要求：计算机出一个 1 到 100 之间的随机数，
玩家输入自己猜的数字，计算机给出对应的提示信息“大一点”、“小一点”或“猜对了”，
如果玩家猜中了数字，计算机提示用户一共猜了多少次，游戏结束，否则游戏继续。
"""
print('测试欧皇小游戏')
import random
ran=random.randrange(1,101)
count=1
while True:
    x = int(input('请玩家输入一个数字： '))
    if x==ran:
        print('猜对了')
        print('您一共猜了%d次'%count)
        break
    elif x>ran:
        print('小一点')
        count+=1
    else:
        print('大一点')
        count+=1

```