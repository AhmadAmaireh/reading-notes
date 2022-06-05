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





