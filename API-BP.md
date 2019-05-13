# API设计最佳实践

## API通用设计原则

- 包装
- 分页
- 状态
- 异常
- 入参

## Restful API设计最佳实践

### 实践1：一类资源两个URL

一个URL表示该类型资源集合，另一个URL用来表示特定的资源元素。

1. 资源集合：/epics
2. 资源元素：/epics/5

### 实践2：使用名词而不是动词

使用Http方法来表达动作（增、删、改、查）

1. 查: 使用GET方法读取资源.
2. 增: 使用POST方法创建新的资源.
3. 改: 使用PUT或PATCH方法来更新已存在的资源.
4. 删: 使用DELETE方法删除存在的资源.

反例：

```
/getAllEmployees
/getAllExternalEmployees
/createEmployee
/updateEmployee
```

正例：

```
GET /employees
GET /employees?state=external
POST /employees
PUT /employees/56
```

## 参考案例

https://www.elastic.co/guide/en/elasticsearch/reference

RFC7807：API错误处理最佳实践 https://mp.weixin.qq.com/s?__biz=MjM5NTg2NTU0Ng%3D%3D&chksm=bd5d2c238a2aa5354cc1d6de2804895cd46d655963433ce7b07891f3f2e40d9931cd0d990741&idx=2&mid=2656598662&scene=0&sn=1bb738ad2ee92c5963dd94cba03dd0b9#rd

https://tools.ietf.org/html/rfc7807

RESTful API的十个最佳实践  https://www.cnblogs.com/xiaoyaojian/p/4612503.html

RESTful Service API 设计最佳工程实践和常见问题解决方案 https://www.jianshu.com/p/cf80d644727e

REST API 设计与开发最佳实践 http://www.21cto.com/article/1751

[RESTful API Design. Best Practices in a Nutshell.](https://phauer.com/2015/restful-api-design-best-practices/)
