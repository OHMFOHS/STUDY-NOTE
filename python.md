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

```python
#python处理excel
import xlrd
import xlwt
from xlutils.copy import copy
data_r=xlrd.open_workbook('maog.xlsx')
table_r=data_r.sheet_by_index(0)
wb=copy(data_r)
sheet=wb.get_sheet(0)
for i in range(4,991,1):
        row_info=table_r.row_values(i)
        pre_data=row_info[4]
        num=len(pre_data.split(';'))
        print(num)
        if num==1:
                sheet.write(i,8,"A.正确")
                sheet.write(i,9,"B.错误")
                print("完成")
        elif num==4:
                u1,u2,u3,u4=pre_data.split(';')
                sheet.write(i,8,"A."+u1)
                sheet.write(i,9,"B."+u2)
                sheet.write(i,10,"C."+u3)
                sheet.write(i,11,"D."+u4)
                print("完成")
        elif num==5:
                u1,u2,u3,u4,u5=pre_data.split(';')
                sheet.write(i,8,"A."+u1)
                sheet.write(i,9,"B."+u2)
                sheet.write(i,10,"C."+u3)
                sheet.write(i,11,"D."+u4)
                sheet.write(i,12,"E."+u5)
                print("完成")
        elif num==6:
                u1,u2,u3,u4,u5,u6=pre_data.split(';')
                sheet.write(i,8,"A."+u1)
                sheet.write(i,9,"B."+u2)
                sheet.write(i,10,"C."+u3)
                sheet.write(i,11,"D."+u4)
                sheet.write(i,12,"E."+u5)
                sheet.write(i,13,"F."+u6)
                print("完成")
wb.save('maog.xls')
print("保存成功")




```

