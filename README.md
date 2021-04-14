# Create_Database

CREATE DATABASE <name of database>;
  
  https://www.postgresql.org/docs/
  
  
  https://www.postgresql.org/files/documentation/pdf/13/postgresql-13-A4.pdf
  
CREATE TABLE person (
id INT, 
First_name VARCHAR(50),
last_name VARCHAR(50),
gender VARCHAR(7),
date_of_birth DATE);

To view the list of all tables in the database we simply write the command

\d

d for describe

\ d person (\d <table name>
  
d for describe table name 
  
  
extra contraints to the table before adding to the table the constraints must be met

first we drop the previous table person with the command below 

DROP TABLE person;

and to check whether it is dropped you can simply type below command and you cannot find the table person. 
\d

Did not find any relations. 




specify the actual constraint
CREATE TABLE person(
id BIGSERIAL NOT NULL PRIMARY KEY, 
First_name VARCHAR(50) NOT NULL,
last_name VARCHAR(50) NOT NULL,
gender VARCHAR(7) NOT NULL,
date_of_birth DATE NOT NULL,
email VARCHAR(150));


The reason we have person_id_seq because we created bigserial and from documentation the description of that says autoincrementing eight_byte integer

so it is not a table but a sequence


How to insert records into tables

so far we have a database "test" with only one column "person"

INSERT INTO person ( 
first_name,
last_name, 
gender, 
date_of_birth)
VALUES('Anne', 'Smith', 'FEMALE', DATE '1988-01-09' );
we set the DATE to say that the date is not the string and the order is like year-month-day.

VALUES('Jack', 'Jones', 'MALE', DATE '1990-12-31', 'jack@gmail.com' );

SELECT * FROM person;

SELECT first_name FROM person

SELECT first_name, last_name FROM person;


SELECT email FROM person;

