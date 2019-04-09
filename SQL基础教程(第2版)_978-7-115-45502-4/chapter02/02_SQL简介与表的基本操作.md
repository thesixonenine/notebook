## SQL概要

　　国际标准化组织(ISO)为SQL指定标准, 即**标准SQL**. 但以前完全基于这个标准SQL的RDBMS很少, 导致能在Oracle中使用的SQL在SQL Server却不能使用.

　　SQL : 使用关键字, 表名, 列名等组合成的一条语句(SQL语句)来描述操作的内容.

## SQL的分类

- DDL(Data Definition Language), 用来**创建**或者**删除**存储数据用的**数据库**以及数据库中的**表**等对象
    - create : 创建数据库和表等对象
    - drop : 删除数据库和表等对象
    - alter : 修改数据库和表等对象的结构
- DML(Data Manipulation Language), 用来**查询**或者**变更**表中的**记录**
    - select : 查询表中的数据(DQL)
    - insert : 向表中插入数据
    - update : 更新表中的数据
    - delete : 删除表中的数据
- DCL(Data Control Language), 用来确认或者取消对数据库中的数据进行的变更, 还可以对RDBMS的用户是否有权限操作数据库中的对象(例如: 表)进行设定
    - commit : 确认对数据库中的数据进行变更
    - rollback : 取消对数据库中的数据进行的变更
    - grant : 赋予用户操作权限
    - revoke : 取消用户的操作权限

## SQL的基本书写规则

- SQL语句需要以分号(;)结尾

- SQL语句不区分大小写

- 常数的书写方式是固定的
    - 字符串/日期 : 直接用单引号括起来
    - 数字 : 直接书写
- 单词之间需要用**半角空格**或者**换行符**来进行分隔

## 表的创建

创建表之前, 一定要先创建数据库

> create database <数据库名称>;

然后才能创建表

```TEXT
create table <表名> (
    <列名1> <数据类型> <该列所需约束>,
    <列名1> <数据类型> <该列所需约束>,
    <列名1> <数据类型> <该列所需约束>,
    .
    .
    .
    <该表的约束1>, <该表的约束2>, ...
);
```

示例:

```SQL
create table product (
    id          char(4)      not null,
    name        varchar(100) not null,
    type        varchar(32)  not null,
    price       integer(10),
    regist_date datetime,
    primary key (id)
);
```

#### 命名规则

只能使用**半角英文字母**, **数字**, **下划线**作为**数据库**, **表**, **列**的名称

> 一个RDBMS中不能有两个相同名称的数据库, 一个数据库中不能有两个相同名称的表, 一张表中不能有两个相同名称的列.