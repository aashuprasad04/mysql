# Filtering Data
## Topic Covered
- WHERE
- AND/OR
- LIKE (search)
- IN

<br><br><br><br>
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

### 1.  WHERE
```mysql
SELECT * FROM students WHERE age > 18;
```
```mysql
MariaDB [mydb1]> select * from students where age = 18;
+----+------+------+
| id | name | age  |
+----+------+------+
|  2 | roni |   18 |
|  5 | lily |   18 |
+----+------+------+
2 rows in set (0.001 sec)
```
### 2. AND / OR
- AND
    ```mysql
    SELECT * FROM TableName WHERE CONDITION-1 AND CONDITION-2;
    ```
    ```mysql
    MariaDB [mydb1]> select * from students where name = 'Aman' and age > 20;
    +----+------+------+
    | id | name | age  |
    +----+------+------+
    |  2 | Aman |   22 |
    +----+------+------+
    ```
- OR
    ```mysql
    SELECT * FROM TableName WHERE CONDITION-1 OR CONDITION-2;
    ```
    ```mysql
    MariaDB [mydb1]> select * from students where name = 'Aman' or age > 20;
    +----+-------+------+
    | id | name  | age  |
    +----+-------+------+
    |  1 | Aman  |   20 |
    |  2 | Aman  |   22 |
    |  3 | Rohit |   22 |
    |  4 | Rohit |   22 |
    |  7 | Priya |   21 |
    |  8 | Priya |   21 |
    |  9 | Karan |   23 |
    | 11 | Arjun |   24 |
    | 13 | Vikas |   21 |
    +----+-------+------+
    ```
### 3. Like (search)
- %    : Any number of characters (0,1, or many)
  - 'A%'    : Starting with 'A'
       ```mysql
        ariaDB [mydb1]> select*from students where name like 'A%';
        +----+-------+------+
        | id | name  | age  |
        +----+-------+------+
        |  1 | Aman  |   20 |
        |  2 | Aman  |   22 |
        | 11 | Arjun |   24 |
        +----+-------+------+
        3 rows in set (0.001 sec)
       ```
  - '%a'    : Ending with 'a'
       ```mysql
        MariaDB [mydb1]> select*from students where name like '%a';
        +----+-------+------+
        | id | name  | age  |
        +----+-------+------+
        |  5 | Sneha |   19 |
        |  6 | Sneha |   19 |
        |  7 | Priya |   21 |
        |  8 | Priya |   21 |
        | 10 | Neha  |   20 |
        | 12 | Pooja |   18 |
        | 14 | Riya  |   19 |
        +----+-------+------+
        7 rows in set (0.001 sec)
       ```
  - '%a%'   : Containing 'a'
       ```mysql
        MariaDB [mydb1]> select*from students where name like '%a%';
        +----+-------+------+
        | id | name  | age  |
        +----+-------+------+
        |  1 | Aman  |   20 |
        |  2 | Aman  |   22 |
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
