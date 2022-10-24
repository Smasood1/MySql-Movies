mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| homework12         |
| information_schema |
| mysql              |
| performance_schema |
| sys                |
| year12flix         |
+--------------------+
6 rows in set (0.01 sec)

mysql> create database Homework1;
Query OK, 1 row affected (0.06 sec)

mysql> use Homework1
Database changed
mysql> create table movies(
    -> Id INT NOT NULL,
    -> title VARCHAR(20) NOT NULL,
    -> genre VARCHAR(100) NOT NULL DEFAULT '',
    -> duration int unsigned NOT NULL DEFAULT 0);
Query OK, 0 rows affected (0.09 sec)

mysql> describe movies;
+----------+--------------+------+-----+---------+-------+
| Field    | Type         | Null | Key | Default | Extra |
+----------+--------------+------+-----+---------+-------+
| Id       | int          | NO   |     | NULL    |       |
| title    | varchar(20)  | NO   |     | NULL    |       |
| genre    | varchar(100) | NO   |     |         |       |
| duration | int unsigned | NO   |     | 0       |       |
+----------+--------------+------+-----+---------+-------+
4 rows in set (0.01 sec)

mysql> INSERT INTO books VALUE(1, "Metropolis", "Sci-Fi", 153);
ERROR 1146 (42S02): Table 'homework1.books' doesn't exist
mysql> INSERT INTO movies VALUE(1, "Metropolis", "Sci-Fi", 153);
Query OK, 1 row affected (0.03 sec)

mysql> INSERT INTO movies VALUE(2, "Nosferatu", "Horror", 94);
Query OK, 1 row affected (0.00 sec)

mysql> INSERT INTO movies VALUE(3, "The Kid", "Comedy", 68);
Query OK, 1 row affected (0.01 sec)

mysql> INSERT INTO movies VALUE(4, "The Gold Rush", "Adventure", 95);
Query OK, 1 row affected (0.00 sec)

mysql> SELECT * FROM movies;
+----+---------------+-----------+----------+
| Id | title         | genre     | duration |
+----+---------------+-----------+----------+
|  1 | Metropolis    | Sci-Fi    |      153 |
|  2 | Nosferatu     | Horror    |       94 |
|  3 | The Kid       | Comedy    |       68 |
|  4 | The Gold Rush | Adventure |       95 |
+----+---------------+-----------+----------+
4 rows in set (0.00 sec)

mysql> 
