## Sequelize Normalization

Sequelize is an easy-to-use and promise-based Node.js ORM tool for Postgres, MySQL, MariaDB, SQLite, DB2, Microsoft SQL Server, Snowflake, and IBM i. It features solid transaction support, relations, eager and lazy loading, read replication and more.

 * Sequelize four types of associations :

 1. The HasOne association
 2. The BelongsTo association
 3. The HasMany association
 4. The BelongsToMany association

* Creating the standard relationships
 To create a One-To-One relationship, the hasOne and belongsTo associations are used together;
 To create a One-To-Many relationship, the hasMany and belongsTo associations are used together;
 To create a Many-To-Many relationship, two belongsToMany calls are used together.