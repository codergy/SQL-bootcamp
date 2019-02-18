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

### Enforce predefined default values during inserting data
If NULL is added, the value will be NULL

    CREATE TABLE cats3
    (
    name VARCHAR(100) DEFAULT 'unnamed',
    age INT DEFAULT 99
    );

### Enforce predefined default values, but let only not NULL values

    CREATE TABLE cats4
    (
    name VARCHAR(20) NOT NULL DEFAULT 'unnamed',
    age INT NOT NULL DEFAULT 99
    );

### Define a table with a PRIMARY KEY constraint

    CREATE TABLE unique_cats
    (
    cat_id INT NOT NULL,
    name VARCHAR(100),
    age INT,
    PRIMARY KEY (cat_id)
    );

Insert ID as following:

    INSERT INTO unique_cats(cat_id, name, age) VALUES(1, 'Fred', 23);

### Define a table with an auto-incrementing PRIMARY KEY

    CREATE TABLE unique_cats2 (
    cat_id INT NOT NULL AUTO_INCREMENT,
    name VARCHAR(100),
    age INT,
    PRIMARY KEY (cat_id)
    );
