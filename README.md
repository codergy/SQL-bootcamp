# SQL-bootcamp
Notes on Colt Steel's SQL bootcamp

### Starting mysql in c9.io
    mysql-ctl start;
    mysql-ctl cli;

## Manipulate databases

### Show all databases
    SHOW DATABASES;

### Create a database
    CREATE DATABASE <name>;

### Delete a database
    DROP DATABASE <name>;

### Select a database
    USE <database name>;

### Show active database name
    SELECT DATABASE();

## Manipulate tables

###  Show all tables in the active database
    SHOW TABLES;

### Create new table
    CREATE TABLE cats
	(
	name VARCHAR(100),
	age INT
	);

### Delete a table
    DROP TABLE <tablename>;

### Shows columns and their type
    SHOW COLUMNS FROM <tablename>;
    DESC <tablename>;

### Insert data into the table
    INSERT INTO <tablename>(columnname1, columnname2) VALUES (value1, value2);

### Multiple insert data into the table
    INSERT INTO <tablename>(columnname1, columnname2)
    VALUES (value1, value2)
    ,(value3, value4)
    ,(value5, value6);

### Enforce not NULL values during inserting data
Data will be empty string or zero. If NULL value is added, error message pops up.

    CREATE TABLE cats2
    (
    name VARCHAR(100) NOT NULL,
    age INT NOT NULL
    );
