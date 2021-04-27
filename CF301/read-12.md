# Read-12

## Reading

[nosql vs sql](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)
[nosql modeling techniques](https://highlyscalable.wordpress.com/2012/03/01/nosql-data-modeling-techniques/)

[mongoose api](https://mongoosejs.com/docs/api.html#Model)
[sql vs nosql - YouTube videl](https://www.youtube.com/watch?v=ZS_kXvOeQ5Y)

## SQL vs NoSQL Database Differences Explained with few Example DB

## SQL vs NoSQL: High-Level Differences

- SQL → Relational Databases
  - Query Language
    - Database Structure
      - Tables
        - Fields(columns)
        - Records(rows)
      - Products
        - All records must have the same Schema
        - Id,name,price,description
    - Relations
      - How tables are related
        - One for users, products, orders etc
        - Orders relates the users and products tables by relating their ids
      - Types of Relations
        - One-to-One
        - One-to-Many
        - Many-to-Many
  - (not a database)
    - Data is stored in multiple tables and relations are made and queried
  - MySql,Oracle,Sqlite,Postgres/MS-SQL
  - Table based
  - Data is in rows
  - Predefined schemas
  - Vertically Scalable
    - vertically scalable → increase Server CPU/RAM/SSD → increases load
  - Best for complex query + high transactions
    - More stable and protects integrity of the data, unlike NoSQL
  - Good Support from vendors
- NoSQL → non-Relational or Distributed Databases
  - MongoDB,BigTable,Redis,RavenDB,Cassandra
  - Collection of key/val pairs
  - Documents
  - No standard schema, only dynamic schema for unstructured data
  - Horizontally Scalable
    - Horizontally scalable → add servers → handles increased traffic
  - Best for Hierarchical data storage because of key/val pairs (similar to JSON) data
  - Best for BIG data
  - Have to rely on community support
  - Limited expert support for large scale ops

NOSQL DATA MODELING TECHNIQUES

How it works

Database

- Shop
  - Collections
    - Users
      - Documents
      - No schema, can have:
        - Id,name,age
      - No relations (few) less relations
        - Rely on key/val pairs in collection
        - drawbacks(duplicate data)
    - Orders
      - Documents
      - No schema, can have:
        - Id only (for example)

No need for winner/loser, it all depends on data needs

SQL pros

- Data uses schema for predictable data format
  - con: cannot be flexible with data
- Relations only need to update data field once
  - con: performance is low for complex relations
- Distributed data across multiple tables
- Vertical Scaling: add more power to existing Server Capacity
  - Has limits
- Limitations for read/write queries per second

NOSQL DATA MODELING TECHNIQUES

- Key:Value Storage Model
  - Poorly applicable to processing key-ranges
    - Overcome by Ordered Key Value model
      - Does not provide framework for modeling
      - Value Modeling done by Big Table Style databases
    - Document Databases advanced the Big Table models. They group indexes by field names
      - Schemes of arbitrary complexity
        - Not just map of maps like Big Table
      - Managed indexes
        - Full Text Search Engines
          - Group indexes by field values

Key Notes:

- Starts with: application specific queries
  - Driven by application specific access patterns (types of queries supported)
  - What questions do i have?
- Requires a deep understanding of Data Structures and Algorithms
- Data Duplication and Denormalization === First Class Citizens
- Good for Heirarchical data
- Data Modeling Techniques and system
  - Key-Value Stores: Oracle Coherence, Redis, Kyoto Cabinet
  - BigTable-style Databases: Apache HBase, Apache Cassandra
  - **Document Databases: MongoDB, CouchDB**
  - Full Text Search Engines: Apache Lucene, Apache Solr
  - Graph Databases: neo4j, FlockDB

Conceptual Techniques

Denormalization

- Copy same data into multiple docs/tables
  - To simplify query processing
  - To fit users data into particular data model
- Pros:
  - Can group all data needed to process query in one place
    - Different query flows → data accessed different combos → duplicate data → increased data volume

Aggregates - soft schemas across all NoSQL dbs

- Key/Val Storage + Graph DBs
  - No constraints on values
    - Therefore vals created in needed formats
- BIgTable Models
  - Variable set of columns inside column family
  - Random number of versions per cell
- Document DBs
  - Schema-less
    - Allow one to validate incoming data using user defined schema
- Application Side Joins
  - Handled at design time
    - Unlike relational models where joins are handled at query execution time
  - Impact performance
    - Avoidable to use joins if instead Denormalize + Aggregate the data
  - They are inevitable and best handled by application
    - Many-to-Many relationships modeled by link and require joins
- Atomic Aggregates
  - Not a complete transactional solution
- Enumerable Keys
- Dimensionality Reduction
  - Map multidimensional data to a Key/Val model or non-multidimensional model
- Index Table
  - Most important class: BigTable-style DB
  - create + maintain special table with key that follow access pattern
- Composite Key Index
  - Generic technique
  - Allows you to build multi-dimensional index
- Aggregation with Composite Keys
- Inverted Search - Direct Aggregation
  - Used for data processing pattern
    - Use index to find data that meets criteria
- Hierarchy Modeling Techniques
  - Tree Aggregation
- Adjacency Lists
- Materialized Paths
- Nested Sets
- Nested Documents Flattening: Numbered Field Names
- Nested Documents Flattening: Proximity Queries
- Batch Graph Processing

MongoDB API

Model()

Model () and its parameters:

- Doc OBJECT values for initial set
- Optional:
  - Fields
    - Object containing the fields that were selected in query which returned the document
  - skipId=false
    - If true, mongo doesn't add an \_id field to the document
- Is a CLASS that is the primary tool for interacting with Mongo
- An instance of Model() is called a Document
  - Model is a subclass of mongoose.Model class.
    - Don't use mongoose.Model directly
  - mongoose.model() and connection.model() create subclasses for mongoose.Model

Model.aggregate()

Model.aggregate and its parameters:

- \[pipeline] Array aggregation pipeline as an array of objects
- \[callback] Function

Returns:

- Aggregate
- Model.aggregate() performs aggregations on the models collection
- If callback is passed
  - Aggregate is executed and Promise is returned
- If callback is not passed
  - Aggregate itself is returned
- Model.aggregate() triggers the middleware: aggregate()

### [top of page](#-Read-12)

### [home page](/README.md)
