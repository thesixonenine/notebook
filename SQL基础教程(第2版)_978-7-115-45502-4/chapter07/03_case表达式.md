## case表达式

- 搜索case表达式
- 简单case表达式

```
CASE WHEN <求值表达式> THEN <表达式>
     WHEN <求值表达式> THEN <表达式>
     WHEN <求值表达式> THEN <表达式>
     .
     .
     .
     ELSE <表达式>
END
```

搜索case表达式:

```SQL
SELECT product_name,
    CASE WHEN product_type = '衣服' 
            THEN 'A ：' | | product_type
         WHEN product_type = '办公用品'
            THEN 'B ：' | | product_type
         WHEN product_type = '厨房用具'
            THEN 'C ：' | | product_type
         ELSE NULL
    END AS abc_product_type
FROM Product;
```

简单case表达式:

```SQL
SELECT product_name,
    CASE product_type
        WHEN '衣服' 
            THEN 'A：' | | product_type
        WHEN '办公用品' 
            THEN 'B：' | | product_type
        WHEN '厨房用具' 
            THEN 'C：' | | product_type
        ELSE NULL
    END AS abc_product_type
FROM Product;
```
