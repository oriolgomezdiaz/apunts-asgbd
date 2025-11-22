# Connectivitat: ODBC i JDBC

Les aplicacions es connecten a les bases de dades mitjançant estàndards que fan d'intermediaris.

## ODBC (Open Database Connectivity)

És un estàndard que permet comunicar-se amb qualsevol SGBD mitjançant un _driver_ específic. [cite_start]Això fa que l'aplicació (ex: Excel) sigui independent del SGBD [cite: 146-148].

- [cite_start]**Funcionament:** L'aplicació parla amb el _Driver Manager_, que carrega el _Driver_ específic, el qual tradueix la petició al SGBD [cite: 164-166].

## JDBC (Java Database Connectivity)

[cite_start]És l'equivalent a ODBC però específic per al llenguatge Java [cite: 149-150]. Existeixen 4 tipus de drivers JDBC, sent el **Tipus 4** el més recomanat:

### Driver Tipus 4 (Protocol Natiu)

- Està escrit 100% en Java.
- Es comunica directament amb el protocol de xarxa del SGBD sense intermediaris.
- [cite_start]**Avantatges:** És molt ràpid i altament portable (funciona a qualsevol lloc amb JVM) [cite: 179-183].
