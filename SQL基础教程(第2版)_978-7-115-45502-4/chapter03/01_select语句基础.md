## SQL语句基础

#### 列的查询

```TEXT
select <列名1>, <列名2>, ... from <表名>;
```

该select语句其实包含了select和from两个子句(clause)

- select子句 : 包含了希望从表中查询出来的列的名称
- from子句 : 指定了选取出数据的表的名称

示例:

```SQL
SELECT `id`, `name`, price FROM product;
```

- 由于MySQL中有些字段可能会被认为是保留关键字, 所以建议在select子句中的字段都加上反引号(\`)
- 查询结果中列的顺序和select子句中的顺序相同
- 查询多列时, 需要使用逗号进行分隔(,)
- 查询所有字段时, 可以使用星号(\*)来代表所有列

```SQL
SELECT * FROM product;
```

#### 为列设定别名

```TEXT
select <列名1> AS <别名1>, <列名2> AS <别名2>, ... from <表名>;
```

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

#### 查询结果去重

使用distinct关键字对字段进行去重

```SQL
SELECT DISTINCT `type` FROM product;
```

也可以多个字段组合去重

```SQL
SELECT DISTINCT `type`,`price` FROM product;
```

在使用DISTINCT时的注意事项

- DISTINCT关键字只能用在第一个列名之前, 也就是select之后, 第一个列名之前
- null也会被视为一类数据, 如果DISTINCT的列有一个或者多个为null的, 去重后也会被合并成一条null数据

#### 使用where子句来选择记录

用于根据条件来进行选择记录

```TEXT
select <列名1>, <列名2>, ... from <表名> where <条件表达式>;
```

示例
```SQL
SELECT DISTINCT `type`,`price` FROM product WHERE `type` = "衣服";
```

- where子句必须跟在from子句后面, SQL中的子句的顺序是固定的

#### 注释的书写方法

- 单行注释: 使用连续两个中划线(--), 注释内容在两个中划线之后
- 多行注释: 注释内容在(/\*)和(\*/)之间
