# SQL
I am reviewing my knowledge about SQL and learning how to use Docker containers to run Oracle Databases in a container.

I found the next video in Youtube that I use to create and run Docker containers for Oracle Databases:

[Oracle - Instalación Base de Datos usando Docker](https://www.youtube.com/watch?v=-W6IveU5Hvo)

There are the main commands you need to use to download Oracle DB and run it into a container:

0. Watch video to install Docker and SQL Developer
1. This cmd is needed to download the Orcacle DB:
```
docker pull container-registry.oracle.com/database/free:latest
```
2. This cmd is needed to run de container in Docker:
```
docker run -d --name "oracle-local" -p 1521:1521 -e ORACLE_PWD="yourPassWord" container-registry.oracle.com/database/free:latest
```