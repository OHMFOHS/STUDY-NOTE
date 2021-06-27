```python
#转换进制
n=input()
n=int(n,2)#二进制转换为十进制
bin(n)#转二进制
oct(n)
hex(n)
print(bin(n)[2:])//切片操作
#格式控制 format
print(a)
print('{:.2f}'.format(a))
#输入转换为 数字存放于列表
a=list(map(int,input()))
#打印列表中数字
print(*z)
#字典操作
for key in c.keys():
for v in c.values():
for k,c in c.item():
#字典按键排序
s=sorted(c)
for x in s:
    print(x,c[x])
#导入random随机数
from random import *

#
list=[n for n in range(1,15) if n%3==0]
print(list)


```