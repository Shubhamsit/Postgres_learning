###  Commands

docker exec -it postgres_container  psql -U shubham -d testdb







\dt ->  List all tables in current schema
\d table_name  -> Describe a table (schema of table)
\dn+  -> Show schema + roles (ownership)



\l -> list of databases

-> select datname from pg_database;  (list datbase)

### create database

-> select datname from pg_database;

postgres=# create database bank;

## change database

->  \c student (to go inside student database)

### delete databse

-> drop database testdb;  (to delete a database)

### crud operation

1. Create 
2. Read
3. Update
4. Delete


### Table

-> Table is a collection of rleted data held in a table formate within database

create table person( id INT, name VARCHAR(100), city VARCHAR(100));

## insert into table 

(for inseting one values)

insert into person(id,name,city)
values(101,'raju','delhi');


for(inserting muti values at same time)

insert into person(id,name,city)
values(101,'raju','delhi'),(102,'shyam','patna');





### reading data from table

select * from person;  (all rows fro table person)

select name from person (only name  from all rows)

select name,city from person; (name and city from all rows)

###  Update in table

update person set city='Bhubneswar' where id=101;

## deleting data 

delete from person where id=101;  (deleting row)

### Datatypes

-> specifies the type of data in a coloumn of our database table

Numeric: INT , DOUBLE, FLOAT, DECIMAL
String : VARCHAR
Date: DATE
Boolean: BOOLEAN

->  \d employees  (to show employees table schema)


CREATE TABLE employees(emp_id SERIAL PRIMARY KEY, fname VARCHAR(100) NOT NULL, lname VARCHAR(50) NOT NULL, email VARCHAR(100) NOT NULL UNIQUE, dept VARCHAR(50), salary DECIMAL(10,2) DEFAULT 3000.00, hire_date DATE NOT NULL DEFAULT CURRENT_DATE);


insert into employees (fname,lname,email,dept,salary, hire_date) values ('shubham','kumar','shubham@gmail.com','it',476374,'2020-01-15');

















