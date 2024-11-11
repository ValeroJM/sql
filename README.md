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
3. Follow video on top to connect our SQL developer with the container database.

## SQL with w3Schools
I also started to use W3Schools website to learn and revisit some of the SQL concepts.

Here is the link to w3Schools website for SQL:
[W3Schools - SQL](https://www.w3schools.com/sql/)

## SQL commands
Here are some of the commands I used to practice with the databases

```
CREATE table persona(
    id varchar(10),
    nombre varchar(30),
    edad int
);

INSERT into persona(id,nombre,edad) values ('1','Jesus Martin',45);
INSERT into persona(id,nombre,edad) values ('2','Marianna Martin',44);
INSERT into persona(id,nombre,edad) values ('3','Yolanda Martin',47);
INSERT into persona(id,nombre,edad) values ('4','Marissa Hinoja',44);

COMMIT;

SELECT * FROM persona;

SELECT COUNT(DISTINCT edad) from persona;

SELECT * FROM persona WHERE edad > 46;

SELECT * FROM persona ORDER BY edad DESC;

SELECT * FROM PERSONA;

SELECT * FROM PERSONA
WHERE NOMBRE LIKE 'J%' OR NOMBRE LIKE 'Y%';

SELECT * FROM PERSONA
WHERE NOT EDAD=44;

SELECT * FROM PERSONA
WHERE EDAD NOT BETWEEN 44 AND 45;

--Inserting Multiple rows in the database
INSERT INTO PERSONA (ID, NOMBRE, EDAD)
VALUES
(5, 'Rory Hogan',18),
(6, 'Angel Villena',48),
(7, 'Jose Gregorio',47);
```