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
mysql -u root -p
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
    CREATE DATABASE mydb;
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
   USE mydb;
   ```
   ```mysql
   MariaDB [(none)]> USE mydb;
   Database changed
   ```

4. Create a table   
   ```mysql
    CREATE TABLE Students(
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

3.    
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
