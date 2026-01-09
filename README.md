# MySQL-Database-Basics
MySQL ist ein weit verbreitetes, leistungsfähiges relationales Datenbankmanagementsystem (RDBMS), das auf SQL (Structured Query Language) basiert. Es wird vor allem für Web‑Anwendungen, Unternehmenssoftware und datenintensive Systeme eingesetzt. MySQL ist bekannt für seine Stabilität, Geschwindigkeit, Skalierbarkeit und die große Community, die es seit vielen Jahren unterstützt. 

## Wichtige Eigenschaften
- Open Source: Kostenlos nutzbar, mit optionalen Enterprise‑Erweiterungen.
- Relationales Modell: Daten werden in Tabellen organisiert, die über Beziehungen verknüpft sind.
- Hohe Performance: Besonders effizient bei Lese‑lastigen Anwendungen.
- Plattformunabhängig: Läuft auf Linux, Windows, macOS und vielen Serverumgebungen.
- Mehrere Speicher-Engines: z. B. InnoDB (Standard, ACID‑konform), MyISAM (schnell, aber ohne Transaktionen).
- Transaktionen & ACID‑Support: Zuverlässige Datenintegrität bei InnoDB.
- Replikation & Clustering: Unterstützt Master‑Slave‑Replikation, Multi‑Source‑Replikation und MySQL Cluster.

## Typische Einsatzgebiete
- Web‑Anwendungen (z. B. WordPress, Joomla, Drupal)
- E‑Commerce‑Plattformen
- Unternehmenssoftware
- Datenanalyse und Reporting
- Microservices und moderne Cloud‑Architekturen

Create Database if not exist
```sql
CREATE DATABASE IF NOT EXISTS Test;
```

Drop Database
```sql
DROP DATABASE Test;
```

Table creation
```sql
CREATE TABLE test (
id INT PRIMARY KEY AUTO_INCREMENT,
`name` VARCHAR(100),
email VARCHAR(100)
);
```

Show all existing tables
```sql
SHOW TABLES;
```

Show column name, type and Preferences
```sql
DESCRIBE name;
```

Add new column to table "test"
```sql
ALTER TABLE test
ADD COLUMN test DATATYPE;
```

Removes the column test from the table name.
```sql
ALTER TABLE test
DROP COLUMN test;
```

Delete the table test
```sql
DROP TABLE test;
```

Deletes all rows of a table but keeps the structure
```sql
TRUNCATE TABLE test;
```

Selects all rows and columns of a table
```sql
SELECT * FROM test;
```

Selects specific columns and filters rows according conditions
```sql
SELECT col1, col2 FROM
name WHERE
condition;
```

Changes column value which fullfills condition
```sql
UPDATE name SET
col = val WHERE
condition;
```

Deletes rows from table which fullfills conditions
```sql
DELETE FROM test
WHERE condition;
```



