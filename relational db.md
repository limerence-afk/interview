### What are the three rules of referential integrity?

The three rules that referential integrity enforces are:

1.    A foreign key must have a corresponding primary key. (“No orphans” rule.)

2.    When a record in a primary table is deleted, all related records referencing the primary key must also be deleted, which is typically accomplished by using cascade delete.

3.    If the primary key for a record changes, all corresponding records in other tables using the primary key as a foreign key must also be modified.  This can be accomplished by using a cascade update.


## Features of relational databases

-   They work with structured data.
    
-   Relationships in the system have constraints, which promotes a high level of data integrity.
    
-   There are limitless indexing capabilities, which results in faster query response times.
    
-   They are excellent at keeping data transactions secure.
    
-   They provide the ability to write complex SQL queries for data analysis and reporting.
    
-   Their models can ensure and enforce business rules at the data layer adding a level of data integrity not found in a non-relational database.
    
-   They are table and row oriented.
    
-   They Use SQL (structured query language) for shaping and manipulating data, which is very powerful.
    
-   SQL database examples: [MySql](https://www.pluralsight.com/paths/mysql), [Oracle](https://www.pluralsight.com/courses/oracle-database-12c-fundamentals), Sqlite, Postgres and MS-SQL. NoSQL database examples: MongoDB, [BigTable](https://www.pluralsight.com/courses/google-bigtable-architecting-big-data-solutions), Redis, RavenDb, Cassandra, Hbase, Neo4j and CouchDb.
    
-   SQL databases are best fit for heavy duty transactional type applications.


## Features of non-relational databases

-   They have the ability to store large amounts of data with little structure.
    
-   They provide scalability and flexibility to meet changing business requirements.
    
-   They provide schema-free or schema-on-read options.
    
-   They have the ability to capture all types of data “Big Data” including unstructured data.
    
-   They are document oriented.
    
-   NoSQL or non-relational databases examples: MongoDB, Apache Cassandra, Redis, Couchbase and Apache HBase.
    
-   They are best for Rapid Application Development. NoSQL is the best selection for flexible data storage with little to no structure limitations.
    
-   They provide flexible data model with the ability to easily store and combine data of any structure without the need to modify a schema.