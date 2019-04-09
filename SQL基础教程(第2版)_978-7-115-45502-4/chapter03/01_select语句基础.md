## SQL语句基础

#### 列的查询

> select <列名1>, <列名2>, ... from <表名>;

该select语句其实包含了select和from两个子句(clause)

1. select子句 : 包含了希望从表中查询出来的列的名称
2. from子句 : 指定了选取出数据的表的名称

示例:

```SQL
SELECT `id`, `name`, price FROM product;
```

由于MySQL中有些字段可能会被认为是保留关键字, 所以建议在select子句中的字段都加上反引号(`)