# vector容器

```c++
//stl标准算法
for_each(v.begin(), v.end(), print);
//遍历
  //      存放数据类型   迭代器  名称（类似指针）   解引用得到的为存放数据类型
for (vector<person>::iterator it = v.begin(); it != v.end(); it++)
{
		cout << "姓名" << (*it).m_name << "年龄" << (*it).m_age << endl;
		cout << "姓名" << it->m_name << "年龄" << it->m_age << endl;
	}
```

### 常用迭代器

![image-20210514093012695](../assets/STL%E5%85%A5%E9%97%A8/image-20210514093012695.png)

```c++
//利用区间方式构造
	vector<int>v2(v1.begin(), v1.end());
//赋值
vector<int>v3;
v3.assign(v1.begin(),v1.end());

//容量与大小
empty();//判断是否为空
capacity();//返回容量
size();//返回容器中元素的个数
resize(int num);//重新指定容器的长度为num，变长用默认值填充，变短删除
resize(int num,elem);//重载版本，边长用elem填充

//插入删除
insert(const_iterator pos,ele);//迭代器指向位置插入ele
insert(const_iterator pos,int count,ele);//迭代器指向位置插入count个ele
clear()//清除所有
erase(const_iterator pos);//删除元素

//数据存取
at(int idx);//v1.at(i);
operator[];
front();//返回第一个元素
back();//返回最后一个元素

//互换容器
//用swap收缩内存
vector<int>(v).swap(v);
//利用匿名对象，当前行执行结束后系统自动回收

//预留空间
reserve(int len);//容器预留len个长度，但预留位置不可访问 
```



# string容器

 string是C++风格的字符串，而string本质上是一个类

## **string和char \* 区别：**

- char * 是一个指针
- string是一个类，类内部封装了char*，管理这个字符串，是一个char*型的容器。

### **特点：**

string 类内部封装了很多成员方法

例如：查找find，拷贝copy，删除delete 替换replace，插入insert

string管理char*所分配的内存，不用担心复制越界和取值越界等，由类内部进行负责

### 初始化方式

```c++
string(); //创建一个空的字符串 例如: string str;
string(const char* s); //使用字符串s初始化

string(const string& str); //使用一个string对象初始化另一个string对象

string(int n, char c); //使用n个字符c初始化
```

### 赋值方式

```c++
//assin 方式
//1普通
string str;
str.assign("hello c++");
//2取前n个字符
string str2;
str2.assign("hello c++",5);
```

### 字符串拼接

```c++
//append
string str;
str.append("abc");
```

### 查找替换

```c++
str.find("abc");//左往右找
//返回类型 int  第一次位置  未找到返回-1
str.rfind("abc")//右往左找
    
//替换
          //位置  几个字符替换为
 str.replace(1,3,"1112311");
```

### 字符串比较

```c++
str1.compare(str2);
//逐个根据ascii码对比大小  相等返回0
```

### 字符存取

```c++
for(int i=0;i<str.size();i++)
{//访问单个字符
    cout<<str[i]<<" ";
        cout<<str.at(i)<<" ";
}
```

### 插入删除  字串获取

```c++
//插入删除
//       位置  内容
str.insert(1,"213");
//删除     位置   删除数量
str.erase( 2，     5 )；
    
//字串获取
string str="Abcdef";
//                   起始位置 个数
string substr=str.substr(1,3);
 
string email="meijicuo@163.com";
int pos=email.find("@");
string username = email.substr(0,pos);
cout<<username<<endl;
```

# deque容器（双端数组）

### 特性

1. 头部插入速度快
2. vector访问元素速度较快

![image-20210514152750717](../assets/STL%E5%85%A5%E9%97%A8/image-20210514152750717.png)

```c++
//只读迭代器
void printdeque(const deque<int>&d)
{                   //只读迭代器
    for(deque<int>::const_iterator it=d.begin();it!=d.end();it++)
}
```

