# Connexions Segures i Normativa

## Per què xifrar?

Per defecte, les connexions MySQL no estan xifrades. Un atacant amb un _sniffer_ podria llegir dades i contrasenyes en text pla. [cite_start]Per evitar-ho, s'utilitza el protocol **TLS** (l'antic SSL ja no s'usa per ser feble) [cite: 1266-1273].

## Funcionament de TLS

[cite_start]Es basa en clau pública i privada i **Certificats Digitals** emesos per una Autoritat de Certificació (CA) per garantir la confiança [cite: 1281-1295].
[cite_start]Per configurar-ho al servidor necessitem les variables: `ssl_ca`, `ssl_cert` i `ssl_key` [cite: 1316-1319].

## Forçar Seguretat per Usuari

[cite_start]Podem obligar un usuari a connectar-se de forma segura [cite: 1330-1335]:

- `REQUIRE SSL`: Obliga a xifrar.
- `REQUIRE X509`: Obliga a presentar un certificat de client vàlid.
- `REQUIRE ISSUER / SUBJECT`: Obliga a que el certificat sigui d'una CA concreta o d'una persona concreta.

Exemple:

```sql
GRANT ALL ... TO 'root'@'localhost' REQUIRE SSL;
```
