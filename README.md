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

Verknüpft Tabelle a und b gibt nur übereinstimmende Zeilen zurück
```sql
SELECT ... FROM a INNER
JOIN b ON a.key = b.key;
```

Legt einen Datenbank Benutzer und Passwort an
```sql
CREATE USER 
'user'@'host' IDENTIFIED BY 'pw';
```

Vergibt Rechte (z.b SELECT) an eine Benutzer in der Datenbank
```sql
GRANT SELECT, INSERT ON
db.* TO 'user'@'host';
```

Zeigt Berechtigungen eines Benutzers an
```sql
SHOW GRANTS FOR
'user'@'host';
```

Exportiert die Datenbank name in eine SQL Dumpdatei
```sql
mysqldump -u user -p
name > dump.sql
```

Importiert eine SQL Dumpdatei
```sql
mysql -u user -p
name < dump.sql
```

#Definitionen Erklärt

identifier = Name für DB/Tabelle/Spalte
```sql
CREATE DATABASE name;
id #Beziechnung für Spatlte; Buchstaben, Zahlen, Zeichen usw.
```

datatype =
```sql
INT #(ganze zahl)
VARCHAR #(legt max zeichen länge an) 
DATE #(Zeit und Datum)
```

constraint = Regel
```sql
NOT NULL #(darf nicht leer sein)
UNIQUE #(einzigartig, nicht wiederhohlt)
PRIMARY KEY #(Primärschlüssel)
```

verhindert Fehler, wenn schon Exisitert
```sql
CREATE DATABASE [IF NOT EXISTS] name;
```

Verhindert Fehler, genaues löschen
```sql
USE name;
DROP DATABSE [IF EXISTS] name;
```

Automatisch generiert, fortlaufend zahl für neue Zeile
```sql
AUTO_INCREMENT
--Beispiel
id INT UNSIGNED NOT NULL AUTO_INCREMT PRIMARY KEY;
```

Tabelle erstellen beispiel
```sql
CREATE TABLE users (
id INT UNSIGNED AUTO_INCREMENT PRIMARY KEY,
username VARCHAR(50) NOT NULL UNIQUE,
email VARCHAR(255) DEFAULT NULL,
created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;
```

