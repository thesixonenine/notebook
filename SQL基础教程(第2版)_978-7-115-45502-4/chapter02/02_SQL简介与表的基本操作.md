## SQL概要

　　国际标准化组织(ISO)为SQL指定标准, 即**标准SQL**. 但以前完全基于这个标准SQL的RDBMS很少, 导致能在Oracle中使用的SQL在SQL Server却不能使用.

　　SQL: 使用关键字, 表名, 列名等组合成的一条语句(SQL语句)来描述操作的内容.

## SQL的分类

- DDL(Data Definition Language), 用来**创建**或者**删除**存储数据用的**数据库**以及数据库中的**表**等对象
　　- create: 创建数据库和表等对象
　　- drop: 删除数据库和表等对象
　　- alter: 修改数据库和表等对象的结构
- DML(Data Manipulation Language), 用来**查询**或者**变更**表中的**记录**
　　- select: 查询表中的数据(DQL)
　　- insert: 向表中插入数据
　　- update: 更新表中的数据
　　- delete: 删除表中的数据
- DCL(Data Control Language), 用来确认或者取消对数据库中的数据进行的变更, 还可以对RDBMS的用户是否有权限操作数据库中的对象(例如: 表)进行设定
　　- commit: 确认对数据库中的数据进行变更
　　- rollback: 取消对数据库中的数据进行的变更
　　- grant: 赋予用户操作权限
　　- revoke: 取消用户的操作权限