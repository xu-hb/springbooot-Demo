
# Spring Boot 整合

1. 示例数据库使用MySQL官方示例`sakila`,下载地址[sakila_db](https://dev.mysql.com/doc/index-other.html)

## 整合Mybatis

`pom.xml`引入相关依赖：

- web依赖：spring-boot-starter-web
- mybatis依赖：mybatis-spring-boot-starter
- MySQL依赖：mysql-connector-java

配置mapper扫描包路径：`@MapperScan`

## 整合数据库连接池Druid

依赖：

- druid-spring-boot-starter

源码以及配置参数文档：

- [Druid Github地址](https://github.com/alibaba/druid)
- [druid-spring-boot-starter 地址](https://github.com/alibaba/druid/tree/master/druid-spring-boot-starter)

## 整合Redis

依赖：

- spring-boot-starter-data-redis

Spring Boot 2.x Redis序列化及乱码解决：`RedisConfig`

基于注解缓存：

- @EnableCaching：开启声明式缓存支持
- @Cacheable：先检查缓存是否存在数据，存在则返回缓存数据；不存在则将返回值放入缓存
- @CachePut：将方法的返回值放入缓存
- @CacheEvict：删除缓存中的数据
