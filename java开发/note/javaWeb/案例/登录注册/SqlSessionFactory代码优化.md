创建SqlSessionFactory代码优化：

```
// 2. 调用MyBatis完成查询
// 2.1 获取SqlSessionFactory对象   https://mybatis.net.cn/ 直接去官网查 
String resource = "mybatis-config.xml";
InputStream inputStream = Resources.getResourceAsStream(resource);
SqlSessionFactory sqlSessionFactory = new SqlSessionFactoryBuilder().build(inputStream);    
```

问题：

    1. 代码重复：工具类
    2. SqlSessionFactory 工厂只创建一次，不要重复创建：静态代码块

