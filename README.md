# MySQL-Database-Basics
MySQL Database basics for beginners


Create Database if not exist
```sql
CREATE DATABASE IF NOT EXISTS schule_uebung;
```

Drop Database
```sql
DROP DATABASE schule_uebung;
```

Table creation
```sql
CREATE TABLE test (
id INT PRIMARY KEY AUTO_INCREMENT,
`name` VARCHAR(100),
email VARCHAR(100)
);
```

