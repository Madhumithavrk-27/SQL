mysql> create database students;
Query OK, 1 row affected (0.01 sec)

mysql> use students
Database changed
mysql> create table student_details
    -> ;
ERROR 1113 (42000): A table must have at least 1 column
mysql> create table student_details(
    -> rollno int
    -> rollno int
    -> ;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near 'int' at line 3
mysql> create table student_details(
    -> rollno int,
    -> name varchar(10),
    -> subject varchar(15),
    -> department varchar(20));
Query OK, 0 rows affected (0.07 sec)

mysql> insert into student_details values(001,'anu','math','cs b'),(002,'mona','physics','IT c'),(003,'sherin','biology','bca');
Query OK, 3 rows affected (0.02 sec)
Records: 3  Duplicates: 0  Warnings: 0

mysql> select * form student_details;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near 'form student_details' at line 1
mysql> select * from student_details;
+--------+--------+---------+------------+
| rollno | name   | subject | department |
+--------+--------+---------+------------+
|      1 | anu    | math    | cs b       |
|      2 | mona   | physics | IT c       |
|      3 | sherin | biology | bca        |
+--------+--------+---------+------------+
3 rows in set (0.05 sec)

mysql> select * from student_details;
+--------+--------+---------+------------+
| rollno | name   | subject | department |
+--------+--------+---------+------------+
|      1 | anu    | math    | cs b       |
|      2 | mona   | physics | IT c       |
|      3 | sherin | biology | bca        |
+--------+--------+---------+------------+
3 rows in set (0.00 sec)

mysql> create table subject(
    -> rollno int,
    -> subject varchar(30));
Query OK, 0 rows affected (0.05 sec)

mysql> drop table subject;
Query OK, 0 rows affected (0.05 sec)

mysql> create table subject(
    -> rollno int,
    -> name varchar(10),
    -> subject varchar(15));
Query OK, 0 rows affected (0.05 sec)

mysql> insert into subject(23,'arun','tamil'),(23,'arun','tamil'),(23,'arun','tamil'),
    -> insert into subject(23,'anu','tamil'),(23,'anu','tamil'),(23,'anu','tamil'),
    -> insert into subject(3,'mona','tamil'),(3,'mona','tamil'),(3,'mona','tamil');
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near '23,'arun','tamil'),(23,'arun','tamil'),(23,'arun','tamil'),
insert into subje...' at line 1
mysql> drop table subject;
Query OK, 0 rows affected (0.06 sec)

mysql> create table subject(
    -> rollno int,
    -> subject varchar(15));
Query OK, 0 rows affected (0.06 sec)

mysql> insert into subject values(1,'tamil'),(1,'tamil'),(1,'english');
Query OK, 3 rows affected (0.01 sec)
Records: 3  Duplicates: 0  Warnings: 0

mysql> insert into subject values(2,'math'),(1,'english'),(1,'java');
Query OK, 3 rows affected (0.04 sec)
Records: 3  Duplicates: 0  Warnings: 0

mysql> select * form subject;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near 'form subject' at line 1
mysql> select * from subject;
+--------+---------+
| rollno | subject |
+--------+---------+
|      1 | tamil   |
|      1 | tamil   |
|      1 | english |
|      2 | math    |
|      1 | english |
|      1 | java    |
+--------+---------+
6 rows in set (0.04 sec)

mysql> create table departement(
    -> deptid int,
    -> deptname varchar(225),
    -> mentor varchar(230));
Query OK, 0 rows affected (0.10 sec)

mysql> select * from departement;
Empty set (0.06 sec)

mysql> insert into departement value(1,'cs','sudee'),(2,'it','shanju'),(3,'bca','madhu');
Query OK, 3 rows affected (0.01 sec)
Records: 3  Duplicates: 0  Warnings: 0

mysql> select * from departement;
+--------+----------+--------+
| deptid | deptname | mentor |
+--------+----------+--------+
|      1 | cs       | sudee  |
|      2 | it       | shanju |
|      3 | bca      | madhu  |
+--------+----------+--------+
3 rows in set (0.00 sec)

mysql> select * from student_details;
+--------+--------+---------+------------+
| rollno | name   | subject | department |
+--------+--------+---------+------------+
|      1 | anu    | math    | cs b       |
|      2 | mona   | physics | IT c       |
|      3 | sherin | biology | bca        |
+--------+--------+---------+------------+
3 rows in set (0.00 sec)

mysql> alter table student_details drop column subject;
Query OK, 0 rows affected (0.06 sec)
Records: 0  Duplicates: 0  Warnings: 0

mysql> select * from student_details;
+--------+--------+------------+
| rollno | name   | department |
+--------+--------+------------+
|      1 | anu    | cs b       |
|      2 | mona   | IT c       |
|      3 | sherin | bca        |
+--------+--------+------------+
3 rows in set (0.00 sec)

mysql> teenote
    -> teenote;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near 'teenote
teenote' at line 1
mysql> teenote;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near 'teenote' at line 1
mysql> notee;
