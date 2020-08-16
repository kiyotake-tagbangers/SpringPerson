## Running by jar

```shell
# maven install before
$ pwd       
/Users/kiyotakeshi/gitdir/java/SpringPerson/target

$ java -jar free-code-camp-spring-tutorial-0.0.1-SNAPSHOT.jar
```

## DB Setup

```shell
$ docker run --name postgres-spring -e POSTGRES_PASSWORD=password -d -p 5432:5432 postgres:alpine

$ docker exec -it postgres-spring bin/bash

bash-5.0# psql -U postgres

postgres=# CREATE DATABASE demodb;
CREATE DATABASE

postgres=# \l
                                 List of databases
   Name    |  Owner   | Encoding |  Collate   |   Ctype    |   Access privileges   
-----------+----------+----------+------------+------------+-----------------------
 demodb    | postgres | UTF8     | en_US.utf8 | en_US.utf8 | 
 postgres  | postgres | UTF8     | en_US.utf8 | en_US.utf8 | 
 template0 | postgres | UTF8     | en_US.utf8 | en_US.utf8 | =c/postgres          +
           |          |          |            |            | postgres=CTc/postgres
 template1 | postgres | UTF8     | en_US.utf8 | en_US.utf8 | =c/postgres          +
           |          |          |            |            | postgres=CTc/postgres
(4 rows)

postgres=# \c demodb
You are now connected to database "demodb" as user "postgres".

demodb=# \d
Did not find any relations.

```