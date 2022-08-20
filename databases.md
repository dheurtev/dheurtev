# My picks for databases

Tools and packages I am using are marked `in use`.
Tools and packages I used are marked as `past`.

- [SQL](#sql)
- [No SQL](#no-sql)
- [Multi-model](#multi-model)
- [Hierarchical](#hierarchical)

[Types of databases](https://www.javatpoint.com/types-of-databases)
[Comparing databases types](https://www.prisma.io/dataguide/intro/comparing-database-types)

## SQL Databases ##
**[`^        back to top        ^`](#)**

### SQL ###

#### PostgreSQL ####
relational, document (JSON and XML), key–value, graph, arrays, objects

- [PostgreSQL](https://www.postgresql.org/): PostgreSQL, also known as Postgres, is an open-source SQL relational database management system. `PostgreSQL License` `in use`
- [PgAdmin](https://www.pgadmin.org/): most popular and feature rich Open Source administration and development platform for PostgreSQL and EnterpriseDB. Cross-platform. `PostgreSQL licence`. `in use`
- [PhpPgAdmin](https://github.com/phppgadmin/phppgadmin): mature web-based administration tool for PostgreSQL. `GPLv2` `in use`
- [Run Postgres in Oracle compatibility mode wit EDB - Proprietary](https://www.enterprisedb.com/postgres-tutorials/how-run-postgres-oracle-compatibility-mode)

#### MySQL / Maria DB ####

Often used with PHP.

- [MariaDB](https://mariadb.org/): Open-source SQL relational database management system. MySQL fork. `GPLv2` `in use`
- [MySQL](https://www.mysql.com/): Open-source SQL relational database management system. `GPLv2` or `proprietary`. `in use`
- [Vitess](https://vitess.io/): Database clustering system for horizontal scaling of MySQL. `Apache License 2.0`
- [MySQL Workbench](https://www.mysql.com/products/workbench/): visual database design tool that integrates SQL development, administration, database design, creation and maintenance into a single integrated development environment for the MySQL database system. Cross-Platform. Free edition. `GPLv2`
- [PhpMyAdmin](https://www.phpmyadmin.net/): free and open source administration tool for MySQL and MariaDB. `GPLv2` `in use`

#### SQLITE ####
- [SQLite](https://www.sqlite.org/index.html): Single file SQL database. Useful for embedded or lightweight projects. `Public Domain` `past`

### Query tools ###
- [DBeaver](https://dbeaver.io/): SQL client software application and a database administration tool. MySQL, PostgreSQL, SQLite, Oracle, DB2, SQL Server, Sybase, MS Access, Teradata, Firebird, Apache Hive, Phoenix, Presto, etc. Cross-platform. `Apache license` `in use`. 
- [HeidiSQL](https://www.heidisql.com/): free and open-source administration tool for MySQL and its forks, as well as Microsoft SQL Server, PostgreSQL and SQLite. `GPLv2` `past`. Windows.
- [DB Browser for Sqlite - Sqlitebrowser](https://sqlitebrowser.org/about/): High quality, visual, open source tool to create, design, and edit database files compatible with SQLite. Cross-platform. DB Browser for SQLite is bi-licensed under the `Mozilla Public License Version 2`, as well as the `GNU General Public License Version 3 or later`.

### Column-oriented databases ###
[Column oriented DBMS - Wikipedia](https://en.wikipedia.org/wiki/Column-oriented_DBMS)
- [MariaDB ColumnStore](https://mariadb.com/kb/en/mariadb-columnstore/)
- PostgreSQL
  * IMCS (In-Memory-Columnar-Store): https://github.com/knizhnik/imcs.git
  * VOPS (Vectorized Operations): https://github.com/postgrespro/vops.git
- [MonetDB](https://www.monetdb.org/):  open-source column-oriented relational database management system (RDBMS). `Mozilla Public License 2.0`

## No SQL ##
**[`^        back to top        ^`](#)**

### Documents : RethinkDB, MongoDB ###
Often used with Javascript/NodeJS.

#### RethinkDB ####
- [RethinkDB](https://rethinkdb.com/): open-source database for the realtime web. JSON. `Apache 2.0 License`.
  * [Github](https://github.com/rethinkdb/rethinkdb)

#### MongoDB ####
- [MongoDB](https://www.mongodb.com/): source-available cross-platform document-oriented database program. JSON like storage. `⚠ Server Side Public License [pseudo free]` `past`
  * [Documentation](https://www.mongodb.com/docs/)
- [Robo Mongo 3T](https://robomongo.org/): free, lightweight, open-source MongoDB GUI with an embedded mongo shell, real auto-completion, and support for MongoDB. `GPLv3` `past`. 
  * [Github](https://github.com/Studio3T/robomongo). `⚠ Abandonned`
- [Studio3T free](https://studio3t.com/free): RoboMongo successor. `⚠ Proprietary`
- [NoSQL Booster](https://nosqlbooster.com/): Cross-platform IDE for MongoDB v2.6-6.0, which provides a build-in MongoDB script debugger, SQL query, server monitoring tools. `⚠ Proprietary`

### Key Value : Redis ###

key–value, document (JSON), property graph, streaming, time-series

- [Redis](https://redis.io/): Open source in-memory data structure store, used as a database, cache, and message broker. `BSD 3 licensed` `in use`
  * [Documentation](https://redis.io/docs/)
- [RedisInsight](https://redis.com/redis-enterprise/redis-insight/#insight-form): REDIS GUI, browser tool, advanced CLI, custom data visualization, and built-in guides to help with using Redis data models like JSON and time series. `⚠ Server Side Public License [pseudo free]`

Alternatives: Memcached, etcd

#### Embedded ####
- [Oracle BerkeleyDB](https://www.oracle.com/fr/database/technologies/related/berkeleydb.html): Embedded Key-Value database. Dual licensed `GNU Affero General Public License` and `proprietary license` `past`
- [HDF5](https://www.hdfgroup.org/solutions/hdf5/): Hierarchical Data Format. Primarily used in Science. `BSD-like Licence` `past`

### Column-family databases: Cassandra ###
- [Cassandra](https://cassandra.apache.org/_/index.html): free and open-source, distributed, wide-column store, NoSQL database management system designed to handle large amounts of data across many commodity servers, providing high availability with no single point of failure. `Apache 2.0 License`

### Time Series : InfluxDB ###
- [InfluxDB](https://www.influxdata.com/): open-source time series database. `MIT License` `in use`
- [Prometheus](https://prometheus.io/): free software application used for event monitoring and alerting. It records real-time metrics in a time series database built using a HTTP pull model, with flexible queries and real-time alerting. `Apache License 2.0`

### Object Storage ###
- [Minio](https://min.io/): highly-available, S3 compatible object storage solution. `Affero General Public License Version 3 (AGPLv3)`

## Multi-model ##
document (JSON), graph, key–value
- [ArangoDB](https://www.arangodb.com/): free and open-source native graph database system. multi-model database system since it supports three data models (graphs, JSON documents, key/value) with one database core and a unified query language AQL (ArangoDB Query Language). `Apache 2.0 License`

## Hierarchical ##
**[`^        back to top        ^`](#)**
- [Hierarchical Database Model - Wikipedia](https://en.wikipedia.org/wiki/Hierarchical_database_model)
### LDAP ###
- [LDAP - Wikipedia](https://en.wikipedia.org/wiki/Lightweight_Directory_Access_Protocol)
- [openLDAP](https://www.openldap.org/): open source implementation of the Lightweight Directory Access Protocol. Cross-platform. `OpenLDAP Public License`
### XML Database ###
Supported by Postgresql among others.
- [XML Database - Wikipedia](https://en.wikipedia.org/wiki/XML_database)



