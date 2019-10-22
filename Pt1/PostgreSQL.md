# PostgreSQL



[TOC]



## 1 - Instal·lació PostgreSQL

### 1.1 - Actualització repositoris

- El primer pas serà actualitzar els repositoris de la nostra màquina

```bash
sudo apt-get update
```

![](img/1_(1).png)



### 1.2 - Instal·lar la paqueteira

- Ara seguidament instal·larem els paquets necessaris per a la pràctica

```bash
sudo apt-get install postgresql postgresql-contrib
```

![](img/2.png)

![](img/3.png)



### 1.3 - Configuració

- Per a tots aquells que vulguin revisar els arxius de configuració es troben a:

```bash
cd /etc/postgresql/X.X/main
```

![](img/4.png)



## 2 - Gestio del PostgreSQL

### 2.1 - Posada en marxa del servei

- El primer que farem serà iniciar el servei

```bash
sudo systemctl start postgresql
```

- Seguidament comprovarem l'estat del servei per assegurar el seu correcte funcionament

```bash
sudo systemctl status postgresql
```

![](img/5.png)



### 2.2 - Gestió bàsica del PostgreSQL

- El primer serà posar una contrasenya a l'usuari postgres

```bash
sudo passwd postgres
```

![](img/10.png)



- Seguidament ens loguejarem amb postgres i executarem la BD

```bash
su postgres
psql
```

![](img/11.png)

![](img/12.png)



- Una de les comandes més bàsiques i útils és posar contrasenya al nostre usuari postgres

```plsql
ALTER USER postgres WITH PASSWORD ‘contrasenya’;
```

![](img/13.png)



- Generalment no treballarem mai amb el nostre usuari postgres així que millor creem un:

```plsql
CREATE USER usuari WITH PASSWORD ‘contrassenya’;
```



- Per poder utilitzar un usuari necessita permisos suficients i en aquest cas volem un administrador:

```plsql
ALTER USER usuari WITH SUPERUSER;
```



## 3 - Entorn gràfic pgadmin3

### 3.1 - Instal·lació del GUI

- Com qualsevol altre paquet el primer que hem de fer és descarregar-lo, en aquest cas dels repositoris d'ubuntu

```bash
sudo apt install pgadmin3
```

![](img/6.png)

![](img/7.png)



### 3.2 - Execució i configuració

- Ara executarem la GUI i la configurarem per al nostre ús

```bash
pgadmin3
```

![](img/8.png)

![](img/9.png)



- Seguidament configurarem la connexió per nosaltres

![](img/14.png)



- Finalment ja tenim accés a la BD desde la GUI

![](img/15.png)

