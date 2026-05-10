# Commons Lang — SRE Final Project
Apache Commons Lang analysed for Software Re-Engineering (BS Software Engineering)

## Group Members

| Member | Full Name     | Roll Number |
|--------|------------- -|-------------|
| 1      |Anna Zubair    | 22F-3658    |
| 2      |Kashmala Ahmad | 22F-3671    |
| 3      |Muhammad Basim | 22F-3684    |

## Project Structure
- `src/` — Apache Commons Lang source code
- `sonar-project.properties` — SonarQube scanner configuration
- `sql/` — Legacy hospital schema SQL scripts (Parts E, F, G)
- `migration_etl.py` — Data migration script (Part G)

## Setup Instructions

### 1. Start SonarQube
```bash
docker start sonarqube
```
Then open http://localhost:9000

### 2. Build the Project
```bash
mvn compile -Drat.skip=true
```

### 3. Run SonarScanner
```bash
sonar-scanner
```

### 4. Load Hospital Schema
```bash
mysql -u root -p < sql/legacy_schema.sql
```

### 5. Run Migration Script
```bash
python3 migration_etl.py
```

## Tools Used
- SonarQube (localhost:9000) — static analysis
- SonarScanner — submits project to SonarQube
- Docker — hosts SonarQube container
- Python Tutor — execution tracing
- Draw.io — CFG and dependency diagrams
- MySQL — legacy hospital database
