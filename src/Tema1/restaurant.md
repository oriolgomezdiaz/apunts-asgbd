# Arquitectura: L'analogia del Restaurant

L'arquitectura d'un SGBD es pot dividir en tres capes principals. [cite_start]Per entendre-ho millor, utilitzem l'exemple d'un restaurant [cite: 38-40, 69].

## 1. APIs de Connexió (El Cambrer)

És la capa superior i el punt d'entrada al sistema.

- [cite_start]**Funció:** Permet que usuaris i apps es connectin (com ODBC/JDBC) [cite: 41-43].
- [cite_start]**Exemple:** El cambrer anota la teva comanda ("vull una hamburguesa sense ceba") i la porta a la cuina [cite: 71-74].

## 2. Execució i Optimització (El Xef)

És la capa intermèdia que processa les ordres.

- [cite_start]**Funció:** Interpreta consultes SQL, gestiona la memòria cau i **optimitza** la consulta per trobar la manera més eficient d'executar-la [cite: 44-47].
- **Exemple:** El xef planifica la recepta. [cite_start]Decideix l'ordre òptim: primer la carn a la planxa calenta, després buscar el pa [cite: 77-82].

## 3. Motor d'Emmagatzematge (El Rebost)

És la capa més baixa, responsable de la interacció amb les dades físiques.

- [cite_start]**Funció:** Gestiona l'accés a disc i memòria, i fa transparent per a l'usuari on estan les dades [cite: 48-51].
- [cite_start]**Exemple:** El xef va a la **nevera** (memòria RAM, accés ràpid) pel formatge i al **rebost** (disc dur, emmagatzematge a llarg termini) pel pa [cite: 84-87].
