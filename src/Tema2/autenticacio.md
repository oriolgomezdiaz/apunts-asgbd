# Autenticació i Gestió d'Usuaris

[cite_start]MySQL desa la informació dels comptes a la base de dades `mysql`, principalment a la taula `user` [cite: 892-895].

## Fase 1: Verificació de la Connexió

[cite_start]Quan intentes connectar-te, el servidor comprova [cite: 1075-1078]:

1.  **Identitat:** Si l'usuari, el host (origen) i la contrasenya són correctes.
2.  **Estat:** Si el compte no està bloquejat (`account_locked`).

### Com decideix MySQL quin usuari ets?

Si hi ha conflictes (ex: tens 'usuari'@'localhost' i 'usuari'@'%'), MySQL ordena la taula `user` per **especificitat**:

1.  **Host:** Primer IPs concretes o 'localhost', al final els comodins (`%`).
2.  **User:** Primer noms concrets, al final els usuaris anònims.
    [cite_start]El servidor utilitza la **primera fila** que coincideix amb la teva connexió [cite: 1092-1098].

## Gestió d'Usuaris (DDL)

- [cite_start]**Crear:** `CREATE USER 'nom'@'host' IDENTIFIED BY 'pass';`[cite: 1159].
  - `'localhost'`: Només connexió local.
  - [cite_start]`'%'`: Connexió des de qualsevol màquina [cite: 1176-1177].
- **Modificar:** `ALTER USER ...` (ex: canviar password o bloquejar).
- [cite_start]**Esborrar:** `DROP USER 'nom'@'host';`[cite: 1186].
- [cite_start]**Canviar nom:** `RENAME USER ...`[cite: 1184].

> **Nota:** Un usuari sempre s'identifica com a `nom` + `host`. [cite_start]`pep@localhost` i `pep@%` són dos usuaris diferents[cite: 1187].
