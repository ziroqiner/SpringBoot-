# 4.1Spring Data JPA常用接口

    说到Spring Data，不得不提它的通用公共接口，其存在于Spring Data Common 中，为Spring Data 的子项目所共享。

```java
@Indexed
public interface Repository<T, ID> {

}
```

    Repository接口是一个标记接口，它的两个泛型参数分别为要管理的域类型以及域类型的 id 类型。 其目的是在类路径扫描期间发现继承这一接口的接口或实现了这一接口的类，以便创建具有数据操作能力的Spring bean。

    @Indexed是一个复杂且与Spring Data无关的注解，我们对此忽略即可。 

    **扩展此接口的域存储库可以通过简单地声明与 CrudRepository 中声明的方法具有相同签名的方法来选择性地公开 CRUD 方法。** 

    **术语声明：**

* 域（domain）：领域驱动设计（DDD）的概念，指数据库表所对应的实体类。







