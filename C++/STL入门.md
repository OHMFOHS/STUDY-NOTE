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

