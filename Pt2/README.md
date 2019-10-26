# DAM2_M2_UF4_Pt1.2

[TOC]



## 1 - Crear user albums i BD

- Crea un usuari àlbums i una base de dades amb el mateix nom.

```plsql
CREATE USER albums WITH PASSWORD '123';
```

```plsql
ALTER USER albums WITH SUPERUSER;
```

![](img/1.png)



```
CREATE DATABASE albums;
```

![](img/2.png)



## 2 - Donar password al usuari

- Dóna-li una contrasenya a l’usuari.

```plsql
CREATE USER albums WITH PASSWORD '123';
```

![](img/1.png)



## 3 - Crear taula principal

- Crea la taula principal amb la que poder gestionar la teva col·lecció d’àlbums musicals (ID de tipus serial, titol de tipus varchar, autor de tipus varchar, suport de tipus varchar, data_edicio de tipus date, discogràfica de tipus varchar). Poseu el ID com a clau primària.

```plsql
CREATE TABLE album (
    id        		serial CONSTRAINT firstkey PRIMARY KEY,
    titol       	varchar(40) NOT NULL,
    autor			varchar(40) NOT NULL,
    suport			varchar(40),
    data_edicio		date,
    discogràfica	varchar(40)
);
```



## 4 - Crear taules complementàries

- Crea les següents taules complementàries (cadascuna en la seua clau primària):
  - autor
  - discogràfica
  - suport



## 5 - Crear les claus foranes

- Crea les claus foranes necessàries a la taula principal.



## 6 - Introdueix dades

- Introdueix dades a totes les taules (un parell de registres és suficient).



## 7 - Realitzar alguna consulta

- Des de l’eina pgAdmin III realitza alguna consulta dels tipos següents:
  - INNER JOIN 
  - OUTER JOIN (FULL/LEFT/RIGHT)