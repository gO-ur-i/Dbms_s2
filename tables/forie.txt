mysql> create table student(Roll_no int , Sname varchar(20), constraint stu primary key(Roll_no));

mysql> create table mark(Rollno int, sub1 int , sub2 int , sub3 int , constraint mark foreign key(Rollno) references student(Roll_no));

O/P 
---

mysql> desc student;
+---------+-------------+------+-----+---------+-------+
| Field   | Type        | Null | Key | Default | Extra |
+---------+-------------+------+-----+---------+-------+
| Roll_no | int         | NO   | PRI | NULL    |       |
| Sname   | varchar(20) | YES  |     | NULL    |       |
+---------+-------------+------+-----+---------+-------+
2 rows in set (0.00 sec)

mysql> desc mark;
+--------+------+------+-----+---------+-------+
| Field  | Type | Null | Key | Default | Extra |
+--------+------+------+-----+---------+-------+
| Rollno | int  | YES  | MUL | NULL    |       |
| sub1   | int  | YES  |     | NULL    |       |
| sub2   | int  | YES  |     | NULL    |       |
| sub3   | int  | YES  |     | NULL    |       |
+--------+------+------+-----+---------+-------+
4 rows in set (0.00 sec)
