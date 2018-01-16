# PostgreSQL-solution
PostgreSQL is a free object relational database management system (ORDBMS), world's most advanced open source database which serves as a good alternative to commercial databases.
### How it works

The server is launched on containerum.com, so you can connect to it using any data management tool, e.g. Valentina Studio.

### It consists of:

* PostgreSQL

To launch this solution on Containerum.com sign up with the service, download and use [Containerum CLI](https://github.com/containerum/chkit) `chkit`.

1. Run the Solution with `chkit solution`:
```
chkit solution run containerum/postgresql-solution -e USER=maria -e PASSWORD=12345678 -e NAME=pg
```

2. Make sure that the Solution is running:

```
$ chkit get deploy
+----------------+------+-------------+------+-------+-----+
|      NAME      | PODS | PODS ACTIVE | CPU  |  RAM  | AGE |
+----------------+------+-------------+------+-------+-----+
| pg-dk2ix       |    1 |           1 | 500m | 512Mi | 7m  |
+----------------+------+-------------+------+-------+-----+
```
3. Using `chkit get` get the address and the port to access the running Solution:
```
$ chkit get svc
+----------------+----------------+----------+-------------------+----------------+-----+
|      NAME      |   CLUSTER-IP   | EXTERNAL |       HOST        |     PORTS      | AGE |
+----------------+----------------+----------+-------------------+----------------+-----+
| pg-dk2ix       | 10.109.153.6   | true     | x2.containerum.io | 33577:5432/TCP | 8m  |
+----------------+----------------+----------+-------------------+----------------+-----+
```
4. Open your data management tool, e.g. Valentina Studio, and connect to `x2.containerum.io:33577`- now you can create or manage your DB.

![](gif/pgsln.gif)
