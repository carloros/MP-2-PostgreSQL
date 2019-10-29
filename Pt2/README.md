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



Primer que rés entrarem a la BD correcta amb l'usuari desitjat, no ho he pogut fer amb albums per problemes de seguretat

```bash
#psql -d databse -U user -W
psql -d albums -U postgres -W
```

![](img/3.png)


Aqui ja podem veure com creem i llistem la taula

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

![](img/4.png)



## 4 - Crear taules complementàries

- Crea les següents taules complementàries (cadascuna en la seua clau primària):
  - autor
  
  ```plsql
  CREATE TABLE autor (
      id        		serial CONSTRAINT firstkeyautor PRIMARY KEY,
      nom       		varchar(40) NOT NULL,
      cognom			varchar(100)
  );
  ```
  
  ![](img/5.png)
  
  
  
  - discogràfica
  
  ```plsql
  CREATE TABLE discografica (
      id        		serial CONSTRAINT firstkeydiscografica PRIMARY KEY,
      nom       		varchar(40) NOT NULL,
      carrer			varchar(200)
  );
  ```
  
  ![](img/6.png)
  
  
  
  - suport
  
  ```plsql
  CREATE TABLE suport (
      id        		serial CONSTRAINT firstkeysuport PRIMARY KEY,
      nom       		varchar(40) NOT NULL
  );
  ```
  
  ![](img/7.png)



## 5 - Crear les claus foranes

- Crea les claus foranes necessàries a la taula principal.



## 6 - Introdueix dades

- Introdueix dades a totes les taules (un parell de registres és suficient).



## 7 - Realitzar alguna consulta

- Des de l’eina pgAdmin III realitza alguna consulta dels tipos següents:
  - INNER JOIN 
  - OUTER JOIN (FULL/LEFT/RIGHT)