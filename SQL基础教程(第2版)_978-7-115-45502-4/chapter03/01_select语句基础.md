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

- 由于MySQL中有些字段可能会被认为是保留关键字, 所以建议在select子句中的字段都加上反引号(`)
- 查询结果中列的顺序和select子句中的顺序相同
- 查询多列时, 需要使用逗号进行分隔(,)
- 查询所有字段时, 可以使用星号(*)来代表所有列

```SQL
SELECT * FROM product;
```