# Apunts: Administració de SGBD (ASGBD)

Benvinguts als apunts de l'assignatura d'Administració de Sistemes Gestors de Bases de Dades. Aquesta documentació cobreix des de l'arquitectura interna d'un gestor fins a la configuració avançada de seguretat i usuaris en MySQL.

---

## 📚 Índex de Continguts

### 🏗️ Tema 1: Arquitectura i Fonaments

Entenent com funciona la base de dades "per dins".

- [**Conceptes Clau**](./tema1/conceptes.md): Diferències entre SGBD i BD, funcions ACID i tipus de llicències.
- [**Arquitectura (Model Restaurant)**](./tema1/restaurant.md): L'analogia del cambrer (API), el xef (Optimitzador) i el rebost (Motor) per entendre el flux d'una consulta.
- [**Connectivitat**](./tema1/connectivitat.md): Diferències entre els drivers ODBC i els 4 tipus de JDBC.
- [**Internals de MySQL**](./tema1/mysql-internals.md): Configuració d'instàncies, fitxers de logs i el diccionari de dades (`INFORMATION_SCHEMA`).

### 🛡️ Tema 2: Seguretat i Control d'Accés

Gestionant qui entra i què pot fer.

- [**Autenticació**](./tema2/autenticacio.md): Com verifica MySQL la identitat (Host + Usuari) i com resol conflictes de connexió.
- [**Sistema de Permisos**](./tema2/permisos.md): La jerarquia de privilegis (Global > DB > Taula > Columna).
- [**Rols i Recursos**](./tema2/rols-recursos.md): Creació de rols per agrupar permisos i limitació de recursos per hora.
- [**Seguretat a la Xarxa**](./tema2/seguretat.md): Xifratge amb TLS/SSL i ús de túnels SSH per protegir les dades en trànsit.

### 🔜 Pròximament

- **Tema 3:** (Pendent de publicació)
- **Tema 4:** (Pendent de publicació)

---

> **Nota:** Material basat en les videoclasses del curs 2025-2026.
> [Tornar al meu GitHub](https://github.com/oriolgomezdiaz)
