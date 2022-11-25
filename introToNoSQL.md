## What is NoSQL

- NoSQL Databases (AKA "not only SQL") are non-tabular databases and store data differently then relational tables.

  > They are Document-based Model which is non-relational in nature.

- They are typically open source softwares. The software is free, and most of them are free to use in commercial products.
- In today's world, It is becoming easier to access and capture through third parties such as Facebook, Google, and others. SQL Databases were never designed to process data at scale. Therefore, NoSQL was introduced to handle the data of this magnitude.
- NoSQL is particularly useful for storing unstructured data, which is growing far more rapidly than structured data and does not fit the relational schemas of the RDBMS.

## Difference between Relational and Non-Relational Databases (Document-based Model)

| Relational                                                  | Non-Relational                                                |
| ----------------------------------------------------------- | ------------------------------------------------------------- |
| Structured                                                  | Unstructured                                                  |
| Data is stored in tables, rows and columns                  | Data is stored in collections, documents and key-value pairs. |
| Examples of Relational Database: SQL, Oracle Database, etc. | Examples of Non-Relational Database: MongoDB, GraphQL, etc.   |

## Difference between SQL and NoSQL

| SQL                                   | NoSQL                           |
| ------------------------------------- | ------------------------------- |
| Relational Database Management System | Distributed Database Management |
| Vertically Scalable                   | Horizontally Scalable           |
| Fixed or Static Schema                | Dynamic/Flexible or No Schema   |
| MySQL, MS-SQL Server, etc.            | MongoDB, GraphQL                |

## Merits of NoSQL

- **High Scalability**:
  - NoSQL database uses sharding for horizontal scaling.
  - NoSQL stores data horizontally against relational databases which stores data vertically.
  - Vertical scaling means adding more resources to the existing machine to store the data whereas Horizontal Scaling means adding more machines to store more data.
  - NoSQL databases can handle huge amount of data because of scalability. As the data increases, NoSQL databases can scale itself to handle that data in an efficient manner.
    > **Sharding**: Partitioning of data on multiple machines in such a way that the order of the data is preserved is known as **Sharding**

## Demerits of NoSQL

- **Open-Source**: NoSQL is an open-source database. This means that there is no reliable standard for this database, which means that two database are likely to be unequal.
- **GUI is not available**: A reliable GUI for this database is not flexibly available in the market.
- **Large Document Size**: Some database like MongoDB use key-value pairs in JSON (Javascript Object Notation) format.

## Types of NoSQL Databases

- **Key-Value**
  - In this type of database, The data is stored in key-value pairs.
  - For instance, key-value pair may contain a key like "Name" and value like "John".
  - Key-Value works well for storing data like Shopping Cart contents.
- **Column-Oriented**
  - In this type of database, The data primarily work on columns and every column is treated individually.
  - High performance on aggregation queries (for eg. COUNT, SUM, AVG, MAX, MIN)
- **Graph**
  - In this type of database, The data is stored in the form of Graphs.
  - A graph contains nodes and edges, Where the nodes represents Entities and edges represent connections or relationships.
- **Document-Based**
  - In this type of database, the data is stored in collection of documents.
  - Documents are not forced to have a schema, and therefore is flexible and easy to change/scale.
  - Documents can contain many different key-value pairs, key-array pairs, and even nested documents.
