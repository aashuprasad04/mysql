# Filtering Data
## Topic Covered
- WHERE
- AND/OR
- LIKE (search)
- IN

<br><br><br><br>
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
