```zsh
sudo systemctl status mysql
```
```zsh
sudo systemctl start mysql
```
```zsh
sudo systemctl stop mysql 
```
1. Login Database
```zsh
sudo mysql
```
2. Login Database using pass
```zsh
mysql -u root -p   //1234
```
<br><br>
# Basic Commands
1. ```mysql
   SHOW DATABASES;
   ```
   ```mysql
    MariaDB [(none)]> show databases;
    +--------------------+
    | Database           |
    +--------------------+
    | information_schema |
    | mysql              |
    | performance_schema |
    | sys                |
    +--------------------+
    4 rows in set (0.007 sec)
    ```
2. ```mysql
    CREATE DATABASE dbName;
   ```
   ```mysql
    MariaDB [(none)]> CREATE DATABASE mydb;
    Query OK, 1 row affected (0.007 sec)
    
    MariaDB [(none)]> SHOW DATABASES;
    +--------------------+
    | Database           |
    +--------------------+
    | information_schema |
    | mydb               |
    | mysql              |
    | performance_schema |
    | sys                |
    +--------------------+
    5 rows in set (0.001 sec)
   ```
3. Use Databases
   ```mysql
   USE dbName;
   ```
   ```mysql
   MariaDB [(none)]> USE mydb;
   Database changed
   ```

4. Create a table   
   ```mysql
    CREATE TABLE tableName(
        -> id INT AUTO_INCREMENT PRIMARY KEY,
        -> name VARCHAR(100),
        -> age INT,
        -> email VARCHAR(100));
   ```
   ```mysql
    MariaDB [mydb]> CREATE TABLE Students(
        -> id INT AUTO_INCREMENT PRIMARY KEY,
        -> name VARCHAR(100),
        -> age INT,
        -> email VARCHAR(100));
    Query OK, 0 rows affected (0.014 sec)

    MariaDB [mydb]> show tables;
    +----------------+
    | Tables_in_mydb |
    +----------------+
    | Students       |
    +----------------+
    1 row in set (0.001 sec)

   ```
4. Delete Table
   - ```mysql
     DROP TABLE tableName;
     ```
   - ```mysql
     DROP TABLE IF EXISTS tableName;
     ```
   ```mysql
    MariaDB [mydb]> show tables;
    +----------------+
    | Tables_in_mydb |
    +----------------+
    | Students       |
    +----------------+
    1 row in set (0.000 sec)

    MariaDB [mydb]> create table tb1(
        -> id int);
    Query OK, 0 rows affected (0.010 sec)

    MariaDB [mydb]> show tables;
    +----------------+
    | Tables_in_mydb |
    +----------------+
    | Students       |
    | tb1            |
    +----------------+
    2 rows in set (0.001 sec)

    MariaDB [mydb]> drop table if exists tb;
    Query OK, 0 rows affected, 1 warning (0.008 sec)

    MariaDB [mydb]> show tables;
    +----------------+
    | Tables_in_mydb |
    +----------------+
    | Students       |
    | tb1            |
    +----------------+
    2 rows in set (0.001 sec)

    MariaDB [mydb]> drop table if exists tb1;
    Query OK, 0 rows affected (0.009 sec)

    MariaDB [mydb]> show tables;
    +----------------+
    | Tables_in_mydb |
    +----------------+
    | Students       |
    +----------------+
    1 row in set (0.001 sec)

    ```   
5. View table structure   
   ```mysql
   DESCRIBE tableName;
   ```    
   ```mysql
    MariaDB [mydb]> show tables;
    +----------------+
    | Tables_in_mydb |
    +----------------+
    | Students       |
    +----------------+
    1 row in set (0.001 sec)
    
    MariaDB [mydb]> describe Students;
    +-------+--------------+------+-----+---------+----------------+
    | Field | Type         | Null | Key | Default | Extra          |
    +-------+--------------+------+-----+---------+----------------+
    | id    | int(11)      | NO   | PRI | NULL    | auto_increment |
    | name  | varchar(100) | YES  |     | NULL    |                |
    | age   | int(11)      | YES  |     | NULL    |                |
    | email | varchar(100) | YES  |     | NULL    |                |
    +-------+--------------+------+-----+---------+----------------+
    4 rows in set (0.001 sec)
   ```
6. Insert data
   ```mysq
   INSERT INTO  (name, age, email)
   VALUES ('John', 20, 'john@example.com');
   ```
   ```mysql
    MariaDB [mydb]> insert into Students(name, age, email)
        -> values('azy', 20, 'azy001@');
    Query OK, 1 row affected (0.006 sec)
    
    MariaDB [mydb]> select*from Students;
    +----+------+------+---------+
    | id | name | age  | email   |
    +----+------+------+---------+
    |  1 | azy  |   20 | azy001@ |
    +----+------+------+---------+
    1 row in set (0.001 sec)
 
   ```
7. View data
   ```mysql
   SELECT * FROM tableName;
   ```
   ```mysql
    MariaDB [mydb]> select*from Students;
    +----+------+------+---------+
    | id | name | age  | email   |
    +----+------+------+---------+
    |  1 | azy  |   20 | azy001@ |
    +----+------+------+---------+
   ```






```zsh

```
```zsh
```
```zsh
```
```zsh
```
```zsh
```
```zsh
```
```zsh
```
```zsh
```
```zsh
```
```zsh
```
```zsh
```
```zsh
```
```zsh
```
```zsh
```
```zsh
```
```zsh
```
```zsh
```
