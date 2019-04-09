## SQL语句基础

#### 列的查询

> select <列名1>, <列名2>, ... from <表名>;

该select语句其实包含了select和from两个子句(clause)

- select子句 : 包含了希望从表中查询出来的列的名称
- from子句 : 指定了选取出数据的表的名称

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

#### 为列设定别名

> select <列名1> AS <别名1>, <列名2> AS <别名2>, ... from <表名>;

- 别名设定使用关键字as
- 别名可以是中文, 但需要使用双引号括起来

#### 常数的查询

```SQL
SELECT "测试", `id`, `name`, price FROM product;
```

或者使用别名

```SQL
SELECT "测试" AS "常数", `id`, `name` AS "商品名称", price AS "价格" FROM product;
```