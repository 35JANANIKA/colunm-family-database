To create a Cassandra database for a library management system, we would first need to identify the different entities that we need to store data for, and then create tables accordingly using Cassendra query language.

First we create a KEYSPACE.and then use the database.the database is library_managenent_system

  CREATE KEYSPACE library_management_system WITH replication = {'class': 'SimpleStrategy', 'replication_factor': '3'};
The tables are: library1 users
   The library table include book_id ,title ,author ,year_published ,num_copies,available_copies,PRIMARY KEY (book_id)
Syntax for creating table:
      CREATE TABLE <table_name> (
   <column_name> <data_type>,
   <column_name> <data_type>,
   PRIMARYKEY(<partition_key_column_name>,     <clustering_column_name>)
);
library1 Table Creation:

    CREATE TABLE library1(book_id int,title text,author text,year_published int,num_copies int,available_copies int,PRIMARY KEY (book_id));
Users Table creation:

     CREATE TABLE users(id int PRIMARY KEY,name text,email text,address text);
 To adding values to the attribute are performed below.

INSERT INTO TABLE

Syntax:

   INSERT INTO <column_family_name> (<column1>, <column2>, <column3>, ...) VALUES (<value1>, <value2>, <value3>, ...);
   
library1 Table insertion:

   library1> INSERT INTO library1(book_id,title,author,year_published,num_copies,available_copies)VALUES(100,'believe in yourself','joseph',2010,5,5); 
   
   library1>  INSERT INTO library1(book_id,title,author,year_published,num_copies,available_copies)VALUES(101,'wins of fire','abdul kalam',1999,10,10);
   
   library1> INSERT INTO library1(book_id,title,author,year_published,num_copies,available_copies)VALUES(102,'cbot','gunjan verma',2014,6,6);
   
   library1> INSERT INTO library1(book_id,title,author,year_published,num_copies,available_copies)VALUES(103,'mobile computing','vinay kumar',2011,2,2);
   
   library1>  INSERT INTO library1(book_id,title,author,year_published,num_copies,available_copies)VALUES(104,'the secret','rhonda byrne',2006,5,5);
   
   library1> INSERT INTO library1(book_id,title,author,year_published,num_copies,available_copies)VALUES(105,'queen of fire','devika',2021,15,15);
   
   library1> INSERT INTO library1(book_id,title,author,year_published,num_copies,available_copies)VALUES(106,'the light of asia','edwin arnoid',1879,10,10);
   
Users Table insertion:

    library1> CREATE TABLE users(id int PRIMARY KEY,name text,email text,address text);
    
    library1>INSERT INTO users(id,name,email,address)VALUES(1,'avi','abc@gmail','first street');
    
    library1> INSERT INTO users(id,name,email,address)VALUES(2,'shasha','xxx@gmail','street second');
    
    library1> INSERT INTO users(id,name,email,address)VALUES(3,'damy','yyy@gmail','new street');
    
    library1>INSERT INTO users(id,name,email,address)VALUES(4,'sara','zzz@gmail','t nagar');
    
    library1> INSERT INTO users(id,name,email,address)VALUES(5,'ric','xyz@gmail','erode');
    
DISPLAY:

Display library1 Table:

library1> SELECT * FROM library1;

Display users Table:

SELECT * FROM users;

 DELETE 

SYNTAX:

DELETE FROM <column_family_name>
WHERE <primary_key> = <value>;

DELETE VALUES IN TABLE:

library1> DELETE FROM library1 WHERE book_id=101;

UPDATE

SYNTAX:

UPDATE <keyspace_name>.<column_family_name>
SET <column_name> = <new_value>
WHERE <primary_key> = <key_value>;

Update in library1 Table:

library1> UPDATE library1 SET year_published=1880 WHERE book_id=106;

SEARCH

SYNTAX:
  SELECT * FROM table name;
  
CONCLUSION:
  
  This readme file explain about how to create tables using cassendra query language and perform opreations like insert,delete,update and search.

  
