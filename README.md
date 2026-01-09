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

Erstellt Datenbank falls diese nicht existiert
```sql
CREATE DATABASE IF NOT EXISTS Test;
```

Löscht Datenbank
```sql
DROP DATABASE name;
```

Erstellt Tabelle
```sql
CREATE TABLE name (
id INT PRIMARY KEY AUTO_INCREMENT,
`name` VARCHAR(100),
email VARCHAR(100)
);
```

Zeigt alle existierenden Tabellen
```sql
SHOW TABLES;
```

Zeigt Spalten Name, typ und Eigenschaften
```sql
DESCRIBE name;
```

Fügt neue Spalte zur Tabelle "Name" hinzu
```sql
ALTER TABLE name
ADD COLUMN test DATATYPE;
```

Löscht die Spalte "test" von der Tabelle Name
```sql
ALTER TABLE name
DROP COLUMN test;
```

Löscht die Tabelle name
```sql
DROP TABLE name;
```

Löscht alle Zeilen einer Tabelle aber behält die Struktur
```sql
TRUNCATE TABLE name;
```
Wählt alle Zeilen einer Spalte aus
```sql
SELECT * FROM test;
```

Wählt bestimmte Spalten aus und filtert die Zeilen nach Konditionen
```sql
SELECT col1, col2 FROM
name WHERE
condition;
```

Ändert den Spalten Wert bei erfüllung bestimmter Konditionen
```sql
UPDATE name SET
col = val WHERE
condition;
```

Löscht alle Zeilen einer Tabelle bei erfüllung bestimmter Konditionen
```sql
DELETE FROM test
WHERE condition;
```



