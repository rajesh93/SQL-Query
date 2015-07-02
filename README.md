# SQL-Query

use test;
create table student(rollnum int,studnme varchar(25),email varchar(30),primary key(rollnum));
insert into student values(101,"hari","hari13445@gmail.com");
insert into student values(102,"srini","srini13445@gmail.com");
insert into student values(103,"nagu","nagu13445@gmail.com");
select * from student where rollnum=102;

use test;
create table studadd(addrnum int,addr varchar(100),rollnum int,primary key(addrnum));
update  studadd set addrnum='101' where addrnum=1;
insert into studadd values(102,"23, annasalai,velacherry",101);
insert into studadd values(103,"23, gandhi street,chennai",103);
insert into studadd values(104,"23, gandhi street,chennai",103);
select * from studadd;

select rollnum,studnme,addrnum 
from student 
inner join studadd 
on student.rollnum = studadd.addrnum;

select * from student order by studnme desc;
SELECT a.addr,a.addrnum,b.rollnum
FROM studadd a left join student b
ON a.rollnum = b.rollnum;

alter table user  rename to newuser;
select*from newuser;
truncate table newuser;
insert into newuser values(111,"rajesh");
insert into newuser values(121,"srini");
delete from newuser where eid=121:
insert into newuser select *from student;
select *from student;
use test;
create table student(sname varchar(10),sid varchar(8));
select *from student;
