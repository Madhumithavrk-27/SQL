mysql> create database kgcas
    -> create database kgcas;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near 'create database kgcas' at line 2
mysql> create database madhu;
Query OK, 1 row affected (0.05 sec)

mysql> use madhu
Database changed
mysql> create table student_profile(
    -> rollno int,
    -> name varchar(20),
    -> date_of_birth date,
    -> departement varchar(10));
Query OK, 0 rows affected (0.05 sec)

mysql> create table marks(
    -> regno int,
    -> mark1 int,
    -> mark2 int,
    -> mark3 int);
Query OK, 0 rows affected (0.07 sec)

mysql> insert into student_profile(rollno,name)value(01,'anu');
Query OK, 1 row affected (0.04 sec)

mysql> insert into student_profile(date_of_birth,departement)value('2006-05-13','cs b');
Query OK, 1 row affected (0.04 sec)

mysql> select * from student_profile;
+--------+------+---------------+-------------+
| rollno | name | date_of_birth | departement |
+--------+------+---------------+-------------+
|      1 | anu  | NULL          | NULL        |
|   NULL | NULL | 2006-05-13    | cs b        |
+--------+------+---------------+-------------+
2 rows in set (0.00 sec)

mysql> update student_profile set date_of_birth='2006-05-13';
Query OK, 1 row affected (0.03 sec)
Rows matched: 2  Changed: 1  Warnings: 0

mysql> select * from student_profile;
+--------+------+---------------+-------------+
| rollno | name | date_of_birth | departement |
+--------+------+---------------+-------------+
|      1 | anu  | 2006-05-13    | NULL        |
|   NULL | NULL | 2006-05-13    | cs b        |
+--------+------+---------------+-------------+
2 rows in set (0.00 sec)

mysql> update student_profile set rollno=02 where name='anu';
Query OK, 1 row affected (0.05 sec)
Rows matched: 1  Changed: 1  Warnings: 0

mysql> select * from student_profile;
+--------+------+---------------+-------------+
| rollno | name | date_of_birth | departement |
+--------+------+---------------+-------------+
|      2 | anu  | 2006-05-13    | NULL        |
|   NULL | NULL | 2006-05-13    | cs b        |
+--------+------+---------------+-------------+
2 rows in set (0.00 sec)

mysql> update student_profile set rollno=2 where departement='cs b';
Query OK, 1 row affected (0.01 sec)
Rows matched: 1  Changed: 1  Warnings: 0

mysql> select * from student_profile;
+--------+------+---------------+-------------+
| rollno | name | date_of_birth | departement |
+--------+------+---------------+-------------+
|      2 | anu  | 2006-05-13    | NULL        |
|      2 | NULL | 2006-05-13    | cs b        |
+--------+------+---------------+-------------+
2 rows in set (0.00 sec)

mysql> update student_profile set rollno=1 where name='anu';
Query OK, 1 row affected (0.04 sec)
Rows matched: 1  Changed: 1  Warnings: 0

mysql> select * from student_profile;
+--------+------+---------------+-------------+
| rollno | name | date_of_birth | departement |
+--------+------+---------------+-------------+
|      1 | anu  | 2006-05-13    | NULL        |
|      2 | NULL | 2006-05-13    | cs b        |
+--------+------+---------------+-------------+
2 rows in set (0.00 sec)

mysql> update student_profile set departement='it c' where name='anu'; 
Query OK, 1 row affected (0.04 sec)
Rows matched: 1  Changed: 1  Warnings: 0

mysql> select * from student_profile;
+--------+------+---------------+-------------+
| rollno | name | date_of_birth | departement |
+--------+------+---------------+-------------+
|      1 | anu  | 2006-05-13    | it c        |
|      2 | NULL | 2006-05-13    | cs b        |
+--------+------+---------------+-------------+
2 rows in set (0.00 sec)

mysql> update student_profile set name='mona' where rollno=2;
Query OK, 1 row affected (0.05 sec)
Rows matched: 1  Changed: 1  Warnings: 0

mysql> select * from student_profile;
+--------+------+---------------+-------------+
| rollno | name | date_of_birth | departement |
+--------+------+---------------+-------------+
|      1 | anu  | 2006-05-13    | it c        |
|      2 | mona | 2006-05-13    | cs b        |
+--------+------+---------------+-------------+
2 rows in set (0.00 sec)

mysql> notee
