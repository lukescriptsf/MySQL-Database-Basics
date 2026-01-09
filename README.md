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

Zeigt alle Tabellen an
```sql
SHOW TABLES;
```



