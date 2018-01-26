# Movie Fun!

Smoke Tests require server running on port 8080 by default.

## Build WAR ignoring Smoke Tests

```
$ mvn clean package -DskipTests -Dmaven.test.skip=true
```

## Run Smoke Tests against specific URL

```
$ MOVIE_FUN_URL=http://moviefun.example.com mvn test
```

vnameits-Mac-mini-3:apps-movie-fun-code sunil$ cf create-service-key movies-mysql EXTERNAL-ACCESS-KEY
Creating service key EXTERNAL-ACCESS-KEY for service instance movies-mysql as sunil.khobragade@cognizant.com...
OK
vnameits-Mac-mini-3:apps-movie-fun-code sunil$ cf service-key movies-mysql EXTERNAL-ACCESS-KEY
Getting key EXTERNAL-ACCESS-KEY for service instance movies-mysql as sunil.khobragade@cognizant.com...

{
 "hostname": "10.0.16.78",
 "jdbcUrl": "jdbc:mysql://10.0.16.78:3306/cf_a588a81e_40b6_4855_80e9_da4114d64405?user=uo9anjzmqkOrL9Ci\u0026password=tluKc6IVoxs1j4mg",
 "name": "cf_a588a81e_40b6_4855_80e9_da4114d64405",
 "password": "tluKc6IVoxs1j4mg",
 "port": 3306,
 "uri": "mysql://uo9anjzmqkOrL9Ci:tluKc6IVoxs1j4mg@10.0.16.78:3306/cf_a588a81e_40b6_4855_80e9_da4114d64405?reconnect=true",
 "username": "uo9anjzmqkOrL9Ci"
}
vnameits-Mac-mini-3:apps-movie-fun-code sunil$ cf ssh -L 63306:10.0.16.78:3306 moviefun-bgjobssync

open a new terminal window 

mysql -u uo9anjzmqkOrL9Ci -h 0 -p -D cf_a588a81e_40b6_4855_80e9_da4114d64405 -P 63306

u will be prompted for password give the password asin the service keys above

the mysql monitor will be opened give the sql command

mysql> DROP TABLE IF EXISTS album_scheduler_task;
Query OK, 0 rows affected, 1 warning (0.04 sec)

mysql> CREATE TABLE album_scheduler_task (started_at TIMESTAMP NULL DEFAULT NULL);
Query OK, 0 rows affected (0.06 sec)

mysql> INSERT INTO album_scheduler_task (started_at) VALUES (NULL);
Query OK, 1 row affected (0.04 sec)

download the commander tool and connect to amazon s3

make changes to the file albums.csv and refresh the paalication page 
you will see the latest changes picked up

show databases;
use movies;
show tables;
 then create the table 
 
 
 for pcf changing the msql tabes need to connect to the following
 
 