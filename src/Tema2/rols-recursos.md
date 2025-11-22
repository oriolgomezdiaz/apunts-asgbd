# Rols i Límits de Recursos

## Límits de Recursos

Podem limitar l'ús que fa un usuari del servidor per evitar abusos. [cite_start]Els límits principals són [cite: 1211-1218]:

- `MAX_QUERIES_PER_HOUR`
- `MAX_UPDATES_PER_HOUR`
- `MAX_CONNECTIONS_PER_HOUR` (connexions totals).
- `MAX_USER_CONNECTIONS` (connexions simultànies).

[cite_start]Es poden assignar al crear l'usuari (`CREATE USER ... WITH MAX_...`) o modificar després (`ALTER USER ...`) [cite: 1224-1230].

## Rols

Un **Rol** és una agrupació de permisos (un contenidor). [cite_start]Facilita la gestió quan tens molts usuaris amb les mateixes funcions[cite: 1238, 1249].

[cite_start]**Passos per usar Rols:** [cite: 1249-1260]

1.  **Crear el rol:** `CREATE ROLE 'desenvolupador';`
2.  **Donar permisos al rol:** `GRANT ALL ON app_db.* TO 'desenvolupador';`
3.  **Assignar el rol a l'usuari:** `GRANT 'desenvolupador' TO 'pep'@'localhost';`
4.  **Activar el rol:** `SET ROLE 'desenvolupador';` (o configurar-ho per defecte).
