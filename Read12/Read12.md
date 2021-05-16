# Mongo and Mongoose

## SQL vs NoSQL

|#|SQL |NoSQL|
|-----|--------|--------|
|1   |SQL databases are primarily called as Relational Databases (RDBMS)        |are primarily called as non-relational or distributed database|
|2   |table based databases|document based|
|3   |have predefined schema|have dynamic schema for unstructured data|
|4   |are vertically scalable|re horizontally scalable|
|5   |uses SQL ( structured query language ) for defining and manipulating the data, which is very powerful|queries are focused on collection of documents|

**What kind of data is a good fit for an SQL database?**
complex query

**Give a real world example.**
MySQL Community Edition

**What kind of data is a good fit a NoSQL database?**
hierarchical data storage

**Give a real world example.**
MongoDB

**Which type of database is best for hierarchical data storage?**
NoSQL database fits better for the hierarchical data storage as it follows the key-value pair way of storing data similar to JSON data.

**Which type of database is best for scalability?**
In most typical situations, SQL databases are vertically scalable. You can manage increasing load by increasing the CPU, RAM, SSD, etc, on a single server. On the other hand, NoSQL databases are horizontally scalable. You can just add few more servers easily in your NoSQL database infrastructure to handle the large traffic.

**What does SQL stand for?**
Structured Query Language

**What is a realational database?**
A relational database is a type of database. It uses a structure that allows us to identify and access data in relation to another piece of data in the database. Often, data in a relational database is organized into tables.

**What type of structure does a relational database work with?**
Tables

**What is a ‘schema’?**
Feilds(columns) in the table must be filled even if there is no value we can put as null

**What is a NoSQL database?**
NoSQL databases (aka "not only SQL") are non tabular, and store data differently than relational tables. NoSQL databases come in a variety of types based on their data model. The main types are document, key-value, wide-column, and graph. They provide flexible schemas and scale easily with large amounts of data and high user loads.

**How does it work?**
if we have a shop database and there we don't have tables but collections (basiclly it represent the fields in the table)and inside the collections there is something called documents with no schema and relation.

**What is inside of a Mongo database?**
MongoDB stores data records as documents (specifically BSON documents) which are gathered together in collections. A database stores one or more collections of documents.

**Which is more flexible - SQL or MongoDB? and why.**
MongoDB,The schemaless design of MongoDB documents makes it extremely easy to build and enhance applications over time, without needing to run complex and expensive schema migration processes as you would with a relational database.
