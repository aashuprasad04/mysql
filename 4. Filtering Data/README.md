```text
4. Filtering Data (WHERE Clause)
   4.1 WHERE Clause
   4.2 Comparison Operators (=, >, <, >=, <=, !=)
   4.3 Logical Operators (AND, OR, NOT)
   4.4 IN and NOT IN
   4.5 BETWEEN and NOT BETWEEN
   4.6 LIKE Operator
   4.7 Wildcards (% , _)
   4.8 IS NULL and IS NOT NULL
```
```mysql
+----+-------+------+
| id | name  | age  |
+----+-------+------+
|  1 | Aman  |   20 |
|  2 | Aman  |   22 |
|  3 | Rohit |   22 |
|  4 | Rohit |   22 |
|  5 | Sneha |   19 |
|  6 | Sneha |   19 |
|  7 | Priya |   21 |
|  8 | Priya |   21 |
|  9 | Karan |   23 |
| 10 | Neha  |   20 |
| 11 | Arjun |   24 |
| 12 | Pooja |   18 |
| 13 | Vikas |   21 |
| 14 | Riya  |   19 |
+----+-------+------+
```

<br><br><br><br>## 4.1 WHERE Clause
- WHERE clause is used to select only those rows that satisfy a given condition.
- Syntax :
  ```mysql

    SELECT column_name(s)
    FROM table_name
    WHERE condition;

  ```
- Example :
  - ex_01:
    ```mysql

    MariaDB [mydb1]> select * from students where age = 20;
    +----+------+------+
    | id | name | age  |
    +----+------+------+
    |  1 | Aman |   20 |
    | 10 | Neha |   20 |
    +----+------+------+
    2 rows in set (0.006 sec)

    ```  


## 4.3 Logical Operators (AND, OR, NOT) 
- Logical operators are used to combine or modify condition in a WHERE clause.
- Syntax :
  ```mysql

    SELECT column_name(s)
    FROM table_name
    WHERE condition1 AND/OR/NOT condition2;

  ```
- Example :
  - ex_01 [AND]:
    ```mysql

    MariaDB [mydb1]> select * from students where name = 'Aman' and age = 20;
    +----+------+------+
    | id | name | age  |
    +----+------+------+
    |  1 | Aman |   20 |
    +----+------+------+

    ```  
  - ex_02 [OR]:
    ```mysql

    MariaDB [mydb1]> select * from students where name = 'Aman' OR  age = 50;
    +----+------+------+
    | id | name | age  |
    +----+------+------+
    |  1 | Aman |   20 |
    |  2 | Aman |   22 |
    +----+------+------+
    
    ```  
  - ex_03 [NOT]:
    ```mysql

    MariaDB [mydb1]> select * from students where not age = 20;
    +----+-------+------+
    | id | name  | age  |
    +----+-------+------+
    |  2 | Aman  |   22 |
    |  3 | Rohit |   22 |
    |  4 | Rohit |   22 |
    |  5 | Sneha |   19 |
    |  6 | Sneha |   19 |
    |  7 | Priya |   21 |
    |  8 | Priya |   21 |
    |  9 | Karan |   23 |
    | 11 | Arjun |   24 |
    | 12 | Pooja |   18 |
    | 13 | Vikas |   21 |
    | 14 | Riya  |   19 |
    +----+-------+------+
    
    ```
- Advance :
  - AD_01 :
    ```mysql

    MariaDB [mydb1]> select * from students where not age in (19,20,50);
    +----+-------+------+
    | id | name  | age  |
    +----+-------+------+
    |  2 | Aman  |   22 |
    |  3 | Rohit |   22 |
    |  4 | Rohit |   22 |
    |  7 | Priya |   21 |
    |  8 | Priya |   21 |
    |  9 | Karan |   23 |
    | 11 | Arjun |   24 |
    | 12 | Pooja |   18 |
    | 13 | Vikas |   21 |
    +----+-------+------+

    ```               


      4.4 IN and NOT IN


## 4.4 IN and NOT IN 
- IN is used to match any value from a list, and NOT IN is used to exclude values from a list
- Syntax :
  ```mysql

    SELECT column_name(s)
    FROM table_name
    WHERE column_name IN (value1, value2, ...);

  ```

  ```mysql

    SELECT column_name(s)
    FROM table_name
    WHERE column_name NOT IN (value1, value2, ...);

  ```

- Example :
  - ex_01 [AND]:  
    ```mysql

    MariaDB [mydb1]> select * from students where name = 'Aman' and age = 20;
    +----+------+------+
    | id | name | age  |
    +----+------+------+
    |  1 | Aman |   20 |
    +----+------+------+

    ```  
  - ex_02 [OR]:
    ```mysql

    MariaDB [mydb1]> select * from students where name = 'Aman' OR  age = 50;
    +----+------+------+
    | id | name | age  |
    +----+------+------+
    |  1 | Aman |   20 |
    |  2 | Aman |   22 |
    +----+------+------+
    
    ```  
  - ex_03 [NOT]:
    ```mysql

    MariaDB [mydb1]> select * from students where not age = 20;
    +----+-------+------+
    | id | name  | age  |
    +----+-------+------+
    |  2 | Aman  |   22 |
    |  3 | Rohit |   22 |
    |  4 | Rohit |   22 |
    |  5 | Sneha |   19 |
    |  6 | Sneha |   19 |
    |  7 | Priya |   21 |
    |  8 | Priya |   21 |
    |  9 | Karan |   23 |
    | 11 | Arjun |   24 |
    | 12 | Pooja |   18 |
    | 13 | Vikas |   21 |
    | 14 | Riya  |   19 |
    +----+-------+------+
    
    ```
- Advance :
  - AD_01 :
    ```mysql

    MariaDB [mydb1]> select * from students where not age in (19,20,50);
    +----+-------+------+
    | id | name  | age  |
    +----+-------+------+
    |  2 | Aman  |   22 |
    |  3 | Rohit |   22 |
    |  4 | Rohit |   22 |
    |  7 | Priya |   21 |
    |  8 | Priya |   21 |
    |  9 | Karan |   23 |
    | 11 | Arjun |   24 |
    | 12 | Pooja |   18 |
    | 13 | Vikas |   21 |
    +----+-------+------+

    ```               
    

