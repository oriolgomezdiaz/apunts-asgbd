# Sistema de Permisos

[cite_start]Un cop connectat, s'activa la **Fase 2**: la verificació de privilegis per a cada comanda que executes[cite: 1127].

## Jerarquia de Taules de Permisos

MySQL comprova els permisos en aquest ordre. [cite_start]Si troba permís en un nivell, autoritza; si no, baixa al següent [cite: 907-914, 1135-1146]:

1.  **Global (`mysql.user`):** S'aplica a **totes** les bases de dades del servidor.
2.  **Base de Dades (`mysql.db`):** S'aplica a una base de dades concreta.
3.  **Taula (`mysql.tables_priv`):** Específic per a una taula.
4.  **Columna (`mysql.columns_priv`):** Específic per a una columna.

[cite_start]El servidor **suma** tots els permisos que troba en aquests nivells[cite: 1144].

## Gestió de Privilegis

- **Atorgar (GRANT):**
  ```sql
  GRANT SELECT, INSERT ON db1.* TO 'usuari'@'localhost';
  ```
  [cite_start]Dona permisos de lectura i escriptura a totes les taules de `db1` [cite: 1201-1202].
- **Revocar (REVOKE):**
  ```sql
  REVOKE INSERT ON db1.* FROM 'usuari'@'localhost';
  ```
  Retira permisos prèviament concedits[cite: 1204].
- **Consultar:** `SHOW GRANTS FOR 'usuari'@'localhost';`[cite: 1206].

[cite_start]Existeixen privilegis **Estàtics** (integrats al servidor com SELECT, CREATE) i **Dinàmics** (definits en temps d'execució, sovint per tasques admin com BACKUP_ADMIN) [cite: 1057-1067].
