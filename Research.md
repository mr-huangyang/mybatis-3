##### SQL 执行流程涉及的类
 * Connection -> Transaction(mybatis) -> Executor -> SqlSession
 ```
1: DefaultSqlSessionFactory.openSessionFromDataSource 方法通过 TransactionFactory 创建 Transaction(这一步可以定制从而将事务管理权让出),构建 Executor ,构建 SqlSession
2: MapperProxyFactory 生成 Mapper代理对象，通过调用SqlSession 执行sql 

``` 