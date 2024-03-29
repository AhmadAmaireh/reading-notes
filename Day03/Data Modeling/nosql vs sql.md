## SQL vs NoSQL: High-Level Differences:

## SQL :

* SQL databases are primarily called as Relational Databases (RDBMS).
* SQL databases are table based databases.
* SQL databases represent data in form of tables which consists of n number of rows of data.
* SQL databases have predefined schema.
* SQL databases are vertically scalable.
* SQL databases are scaled by increasing the horse-power of the hardware.
* SQL databases uses SQL ( structured query language ) for defining and manipulating the data.
* SQL database examples: MySql, Oracle, Sqlite, Postgres and MS-SQL.
* For the type of data to be stored: SQL databases are not best fit for hierarchical data storage.
* For scalability: In most typical situations, SQL databases are vertically scalable. You can manage increasing load by increasing the CPU, RAM, SSD, etc, on a single server.
* For high transactional based application: SQL databases are best fit for heavy duty transactional type applications, as it is more stable and promises the atomicity as well as integrity of the data.
* For support: Excellent support are available for all SQL database from their vendors. There are also lot of independent consultations who can help you with SQL database for a very large scale deployments.
* For properties: SQL databases emphasizes on ACID properties ( Atomicity, Consistency, Isolation and Durability).
* For DB types: On a high-level, we can classify SQL databases as either open-source or close-sourced from commercial vendors.


## NoSQL:

* NoSQL database are primarily called as non-relational or distributed database.
* NoSQL databases are document based, key-value pairs, graph databases or wide-column stores. 
* NoSQL databases are the collection of key-value pair, documents, graph databases or wide-column stores which do not have standard schema definitions which it needs to adhered to.
* NoSQL databases have dynamic schema for unstructured data.
* NoSQL databases are horizontally scalable.
* NoSQL databases are scaled by increasing the databases servers in the pool of resources to reduce the load.
* In NoSQL database, queries are focused on collection of documents. Sometimes it is also called as UnQL (Unstructured Query Language  The syntax of using UnQL varies from database to database.
* NoSQL database examples: MongoDB, BigTable, Redis, RavenDb, Cassandra, Hbase, Neo4j and CouchDb.
* NoSQL databases are not good fit for complex queries. On a high-level, NoSQL don’t have standard interfaces to perform complex queries, and the queries themselves in NoSQL are not as powerful as SQL query language.
* NoSQL database fits better for the hierarchical data storage as it follows the key-value pair way of storing data similar to JSON data. NoSQL database are highly preferred for large data set (i.e for big data). Hbase is an example for this purpose.
* NoSQL databases are horizontally scalable. You can just add few more servers easily in your NoSQL database infrastructure to handle the large traffic.
* can use NoSQL for transactions purpose, it is still not comparable and sable enough in high load and for complex transactional applications.
* NoSQL database you still have to rely on community support, and only limited outside experts are available for you to setup and deploy your large scale NoSQL deployments.
* NoSQL database follows the Brewers CAP theorem ( Consistency, Availability and Partition tolerance ).
* NoSQL databases can be classified on the basis of way of storing data as graph databases, key-value store databases, document store databases, column store database and XML databases.


## Examples :

## SQL Database Examples

1. MySQL Community Edition
MySQL database is very popular open-source database. It is generally been stacked with apache and PHP, although it can be also stacked with nginx and server side javascripting using Node js. The following are some of MySQL benefits and strengths:

Replication: By replicating MySQL database across multiple nodes the work load can be reduced heavily increasing the scalability and availability of business application
Sharding: MySQL sharding os useful when there is large no of write operations in a high traffic website. By sharding MySQL servers, the application is partitioned into multiple servers dividing the database into small chunks. As low cost servers can be deployed for this purpose, this is cost effective.
Memcached as a NoSQL API to MySQL: Memcached can be used to increase the performance of the data retrieval operations giving an advantage of NoSQL api to MySQL server.
Maturity: This database has been around for a long time and tremendous community input and testing has gone into this database making it very stable.
Wide range of Platforms and Languages: MySql is available for all major platforms like Linux, Windows, Mac, BSD and Solaris. It also has connectors to languages like Node.js, Ruby, C#, C++, C, Java, Perl, PHP and Python.
Cost effectiveness: It is open source and free.
2. MS-SQL Server Express Edition
It is a powerful and user friendly database which has good stability, reliability and scalability with support from Microsoft. The following are some of MS-SQL benefits and strengths:

Integrated Development Environment: Microsoft visual studio, Sql Server Management Studio and Visual Developer tools provide a very helpful way for development and increase the developers productivity.
Disaster Recovery: It has good disaster recovery mechanism including database mirroring, fail over clustering and RAID partitioning.
Cloud back-up: Microsoft also provides cloud storage when you perform a cloud-backup of your database
3. Oracle Express Edition
It is a limited edition of Oracle Enterprise Edition server with certain limitations. This database is free for development and deployment. The following are some of Oracle benefits and strengths:

Easy to Upgrade: Can be easily upgraded to newer version, or to an enterprise edition.
Wide platform support: It supports a wide range of platforms including Linux and Windows
Scalability: Although the scalability of this database is not cost effective as MySQL server, but the solution is very reliable, secure, easily manageable and productive.


## NoSQL Database Examples

1. MongoDB:
Mongodb is one of the most popular document based NoSQL database as it stores data in JSON like documents. It is non-relational database with dynamic schema. It has been developed by the founders of DoubleClick, written in C++ and is currently being used by some big companies like The New York Times, Craigslist, MTV Networks. The following are some of MongoDB benefits and strengths:

Speed: For simple queries, it gives good performance, as all the related data are in single document which eliminates the join operations.
Scalability: It is horizontally scalable i.e. you can reduce the workload by increasing the number of servers in your resource pool instead of relying on a stand alone resource.
Manageable: It is easy to use for both developers and administrators. This also gives the ability to shard database
Dynamic Schema: Its gives you the flexibility to evolve your data schema without modifying the existing data
2. CouchDB:
CouchDB is also a document based NoSQL database. It stores data in form of JSON documents.
Schema-less: As a member of NoSQL family, it also have dynamic schema which makes it more flexible, having a form of JSON documents for storing data.
HTTP query: You can access your database documents using your web browser.
Conflict Resolution: It has automatic conflict detection which is useful while in a distributed database.
Easy Replication: Implementing replication is fairly straight forward
3. Redis:
Redis is another Open Source NoSQL database which is mainly used because of its lightening speed. It is written in ANSI C language. The following are some of Redis benefits and strengths:

Data structures: Redis provides efficient data structures to an extend that it is sometimes called as data structure server. The keys stored in database can be hashes, lists, strings, sorted or unsorted sets.
Redis as Cache: You can use Redis as a cache by implementing keys with limited time to live to improve the performance.
Very fast: It is consider as one of the fastest NoSQL server as it works with the in-memory dataset.


