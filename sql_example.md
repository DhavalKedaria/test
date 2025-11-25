create table team_building(id int, name text, isindian Boolean)

create table team_building(id int PRIMARY KEY, name text NOT NULL, isindian Boolean)

insert into team_building (id,name,isindian) values(1,'vedant',true)

insert into team_building (id,name,isindian) values(5,'Tushar',true)

insert into team_building (id,name,isindian) values(3,'dhaval',true),(4,'dhaval',true)

insert into team_building (id,isindian) values(5,true)

update team_building set name='sumit' where id =3 

update team_building set isindian=false where id =3

drop table team_building

drop table salary

select * from team_building order by isindian

create table salary (id SERIAL PRIMARY KEY, emp_id int NOT NULL, pay int NOT NULL)

insert into salary (emp_id,pay) VALUES(4,110000) 

select * from salary

select * from team_building inner join salary on team_building.id=salary.emp_id
select * from team_building left join salary on team_building.id=salary.emp_id
select * from team_building as t right join salary as s on t.id=s.emp_id order by t.id

select t.id as roll_no,t.name as employee_name,t.isindian as "nationality_indian?",s.id as salary_id,s.emp_id as employee_id,s.pay as salary from team_building as t right join salary as s on t.id=s.emp_id order by t.id



## Fruit_store
- fruits (id, name, origin, test)
- quantity (id,fruit_id,available_qty,sold_qty)
- price (id,fruit_id,mrp)
- customer (id, fruit_id,date,qty)