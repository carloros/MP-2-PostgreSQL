# Primers pasos amb Docker



[TOC]



## 1 - Instal·lar docker



- El primer serà realitzar un update del repositoris del sistema

```bash
sudo apt update
```

![](img/1.png)



- Seguidament desinstal·larem les versions antigues de **Docker**

```bash
sudo apt remove docker docker-engine docker.io
```

![](img/2.png)



- Finalment només caldrà instal·lar el software

```bash
sudo apt install docker docker.io
```

![](img/3.png)



## 2 - Baixar el contenidor



- Seguidament el que farem serà baixar el contenidor a la màquina per fer-lo servir en Docker

```bash
sudo docker pull postgres
```

![](img/4.png)



- Ara comprovarem que realment tenim el contenedor baixat

```bash
sudo docker image ls
```

![](img/5.png)



## 3 - Iniciem el contenidor



- Ara realitzarem l'acció més important, iniciar el contenidor per al seu ús indicant "username", "password" i "database"

```bash
sudo docker run --name username -e POSTGRES_PASSWORD=password -d database
```

![](img/6.png)



- I per ultim només caldra accedir al servei del nostre contenidor amb les credencials inidicades al pas anterior 

```bash
sudo docker run -it --rm --link username:postgres database psql -h postgres -U postgres
```

![](img/7.png)



## 4 - Repetir pràctica 1.2

