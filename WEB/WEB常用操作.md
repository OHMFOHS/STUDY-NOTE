```html
<div style="width:100%;text-align:center">
</div>
```

```java
JDBC 数据库连接

1 加载驱动
Class.forName("com.mysql.jdbc.Driver");

2获得连接
Connection conn = DriverManager.getConnection("jdbc://mysql://localhost:3306/web_test3","root","abc");

3执行sql语句
3.1获得执行sql语句的对象
    Statement statement = conn.createStatement();
3.2编写sql语句
    String sql = "select * from user";
3.3执行sql
    ResultSet rs = statement.executeQuery(sql);
3.4遍历结果集
    while(rs.next()){
        System.out.println(rs.getInt("id"));
        System.out.println(rs.getString("username"));
        System.out.println(rs.getString("password"));
    }

4.释放资源
rs.close();
statement.close();
conn.close();
```

<

```java
DBUtils
    
```



```java
servlet
	1 新建包和类
    2 实现servlet接口
     	用来处理客户请求的方法service
    public void service(ServletRequest req, ServletResponse resp) throws ServletException,IOException{
    
}
	3 配置这个类
        在web.xml配置servlet
        <servlet>
        	<servlet-name></servlet-name>
        /配置全路径
        	<servlet-class></servlet-class>
        </servlet>
              
        <servlet-mapping> /映射
                <servlet-name>   <servlet-name>/名称
                <url-pattern>     </url-pattern> /访问路径
        </servlet-mapping>
          
    4访问servlet
                输入对应地址
                
Servlet执行流程
                输入地址->找到配置 访问路径->
                 
Servlet实现关系:
	
```

![image-20211126090853522](../assets/WEB%E5%B8%B8%E7%94%A8%E6%93%8D%E4%BD%9C/image-20211126090853522.png)