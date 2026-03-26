## 项目场景：

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/d7daf023d31180e68dc785b51d0f3e2a.png#pic_center)

## 问题描述：

在用Idea工具连接Redis的时候报错。

org.springframework.data.redis.RedisConnectionFailureException: Unable to connect to Redis; nested exception is io.lettuce.core.RedisConnectionException: Unable to connect to localhost:6379

```
at org.springframework.data.redis.connection.lettuce.LettuceConnectionFactory$ExceptionTranslatingConnectionProvider.translateException(LettuceConnectionFactory.java:1534)
at org.springframework.data.redis.connection.lettuce.LettuceConnectionFactory$ExceptionTranslatingConnectionProvider.getConnection(LettuceConnectionFactory.java:1442)
at org.springframework.data.redis.connection.lettuce.LettuceConnectionFactory$SharedConnection.getNativeConnection(LettuceConnectionFactory.java:1228)
at org.springframework.data.redis.connection.lettuce.LettuceConnectionFactory$SharedConnection.getConnection(LettuceConnectionFactory.java:1211)
at org.springframework.data.redis.connection.lettuce.LettuceConnectionFactory.getSharedConnection(LettuceConnectionFactory.java:975)
at org.springframework.data.redis.connection.lettuce.LettuceConnectionFactory.getConnection(LettuceConnectionFactory.java:360)
at org.springframework.data.redis.core.RedisConnectionUtils.doGetConnection(RedisConnectionUtils.java:134)

```

## 原因分析：

可能是我连接的IP地址有问题，为啥是localhost。  
![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/30677fbc5d97f27a9a86ebc138cdc968.png#pic_center)

---

## 解决方案：

datasource 与 redis 要写在同一级。

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/7b6360014715a583aea11bb2e6f370a4.png#pic_center)

![在这里插入图片描述](https://i-blog.csdnimg.cn/blog_migrate/d3f9751b1535821751cb5c3edc643a49.png#pic_center)