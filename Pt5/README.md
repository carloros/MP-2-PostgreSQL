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
sudo apt install docker docker-engine docker.io
```

![](img/3.png)



## 2 - Baixar el contenidor

- Seguidament el que farem serà baixar el contenidor a la màquina per fer-lo servir en Docker

```bash
sudo docker pull postgres
```

![](img/4.png)