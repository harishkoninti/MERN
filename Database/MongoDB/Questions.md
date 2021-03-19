### 1). What are NoSQL databases? What are the different types of NoSQL databases?
A NoSQL database provides a mechanism for storage and retrieval of data that is modeled in means other than the tabular relations used in relational databases (like SQL, Oracle, etc.).
Types of NoSQL databases:
Document Oriented
Key Value
Graph
Column Oriented

### 2) What kind of NoSQL database MongoDB is?
MongoDB is a document oriented database. It stores data in the form of BSON structure based documents. These documents are stored in a collection.

### 3) Which are the most important features of MongoDB?
Flexible data model in form of documents
Agile and highly scalable database
Faster than traditional databases
Expressive query language

### 4) What is a Namespace in MongoDB?
A Namespace is the concatenation of the database name and collection name. For e.g. school.students with school as the database and students as the collection

### 5) Which all languages can be used with MongoDB?
Currently, MonggoDB provides official driver support for C, C++, C#, Java, Node.js, Perl, PHP, Python, Ruby, Scala, Go and Erlang. MongoDB can easily be used with any of these languages. There are some other community supported drivers too but the above mentioned ones are officially provided by MongoDB.

### 6) Compare SQL databases and MongoDB at a high level.
SQL databases store data in form of tables, rows, columns and records. This data is stored in a pre-defined data model which is not very much flexible for today's real-world highly growing applications. MongoDB in contrast uses a flexible structure which can be easily modified and extended.

### 7) How is MongoDB better than other SQL databases?
MongoDB allows a highly flexible and scalable document structure. For e.g. one data document in MongoDB can have five columns and the other one in the same collection can have ten columns. Also, MongoDB database are faster as compared to SQL databases due to efficient indexing and storage techniques.

### 8) Compare MongoDB and CouchDB at high level.
Although both of these databases are document oriented, MongoDB is a better choice for applications which need dynamic queries and good performance on a very big database. On the other side, CouchDB is better used for applications with occasionally changing queries and pre-defined queries.

### 9) Does MongoDB support foreign key constraints?
No. MongoDB does not support such relationships.

### 10) Does MongoDB support ACID transaction management and locking functionalities?
No. MongoDB does not support default multi-document ACID transactions. However, MongoDB provides atomic operation on a single document.

### 11) How can you achieve primary key - foreign key relationships in MongoDB?
By default MongoDB does not support such primary key - foreign key relationships. However, we can achieve this concept by embedding one document inside another. Foe e.g. an address document can be embedded inside customer document.

### 12) Does MongoDB need a lot of RAM?
No. MongoDB can be run even on a small amount of RAM. MongoDB dynamically allocates and de-allocates RAM based on the requirements of other processes.

### 13) Does MongoDB pushes the writes to disk immediately or lazily?
MongoDB pushes the data to disk lazily. It updates the immediately written to the journal but writing the data from journal to disk happens lazily.

### 14) Explain the structure of ObjectID in MongoDB.
ObjectID is a 12-byte BSON type with:
4 bytes value representing seconds
3 byte machine identifier
2 byte process id
3 byte counter

### 15) MongoDB uses BSON to represent document structures. True or False?
True

### 16) If you remove a document from database, does MongoDB remove it from disk?
Yes. Removing a document from database removes it from disk too.

### 17) Mention the command to insert a document in a database called school and collection called persons.
use school;
db.persons.insert( { name: "kadhir", dept: "CSE" } )
### 18) What are Indexes in MongoDB?
Indexes support the efficient execution of queries in MongoDB. Without indexes, MongoDB must perform a collection scan, i.e. scan every document in a collection, to select those documents that match the query statement. If an appropriate index exists for a query, MongoDB can use the index to limit the number of documents it must inspect.

### 19) How many indexes does MongoDB create by default for a new collection?
By default, MongoDB created the _id collection for every collection.

### 20) Can you create an index on an array field in MongoDB? If yes, what happens in this case?
Yes. An array field can be indexed in MongoDB. In this case, MongoDB would index each value of the array.

### 21) What is a covered query in MongoDB?
A covered query is the one in which:

### 22) fields used in the query are part of an index used in the query, and
the fields returned in the results are in the same index

### 23) Does MongoDB provide a facility to do text searches? How?
Yes. MongoDB supports creating text indexes to support text search inside string content. This was a new feature which can introduced in version 2.6.

### 24) What happens if an index does not fit into RAM?
If the indexes do not fit into RAM, MongoDB reads data from disk which is relatively very much slower than reading from RAM.

### 25) Mention the command to list all the indexes on a particular collection.
db.collection.getIndexes()

### 26) At what interval does MongoDB write updates to the disk?
By default configuration, MongoDB writes updates to the disk every 60 seconds. However, this is configurable with the commitIntervalMs and syncPeriodSecs options.

### 27) How can you achieve transaction and locking in MongoDB?
To achieve concepts of transaction and locking in MongoDB, we can use the nesting of documents, also called embedded documents. MongoDB supports atomic operations within a single document.

### 28) What is Aggregation in MongoDB?
Aggregations operations process data records and return computed results. Aggregation operations group values from multiple documents together, and can perform a variety of operations on the grouped data to return a single result. MongoDB provides three ways to perform aggregation: the aggregation pipeline, the map-reduce function, and single purpose aggregation methods and commands.

### 29) What is Sharding in MongoDB? Explain.
Sharding is a method for storing data across multiple machines. MongoDB uses sharding to support deployments with very large data sets and high throughput operations.

### 30) What is Replication in MongoDB? Explain.
Replication is the process of synchronizing data across multiple servers. Replication provides redundancy and increases data availability. With multiple copies of data on different database servers, replication protects a database from the loss of a single server. Replication also allows you to recover from hardware failure and service interruptions.

### 31) What are Primary and Secondary Replica sets?
Primary and master nodes are the nodes that can accept writes. MongoDB's replication is 'single-master:' only one node can accept write operations at a time.

Secondary and slave nodes are read-only nodes that replicate from the primary.

### 32) By default, MongoDB writes and reads data from both primary and secondary replica sets. True or False.
False. MongoDB writes data only to the primary replica set.

### 33) Why are MongoDB data files large in size?
MongoDB preallocates data files to reserve space and avoid file system fragmentation when you setup the server.

### 34) When should we embed one document within another in MongoDB?
You should consider embedding documents for:

'contains' relationships between entities
One-to-many relationships
Performance reasons
### 35) Why MongoDB is not preferred over a 32-bit system?
When running a 32-bit build of MongoDB, the total storage size for the server, including data and indexes, is 2 gigabytes. For this reason, do not deploy MongoDB to production on 32-bit machines.

If you're running a 64-bit build of MongoDB, there's virtually no limit to storage size.

### 36) What is a Storage Engine in MongoDB
A storage engine is the part of a database that is responsible for managing how data is stored on disk. For example, one storage engine might offer better performance for read-heavy workloads, and another might support a higher-throughput for write operations.

### 37) Which are the two storage engines used by MongoDB?
MongoDB uses MMAPv1 and WiredTiger.

### 38) What is the role of a profiler in MongoDB? Where does the writes all the data?
The database profiler collects fine grained data about MongoDB write operations, cursors, database commands on a running mongod instance. You can enable profiling on a per-database or per-instance basis.

The database profiler writes all the data it collects to the system.profile collection, which is a capped collection.

### 39) How does Journaling work in MongoDB?
When running with journaling, MongoDB stores and applies write operations in memory and in the on-disk journal before the changes are present in the data files on disk. Writes to the journal are atomic, ensuring the consistency of the on-disk journal files. With journaling enabled, MongoDB creates a journal subdirectory within the directory defined by dbPath, which is /data/db by default.

### 40) Mention the command to check whether you are on the master server or not.
db.isMaster()

### 41) Why is a covered query important?
Since all the fields are covered in the index itself, MongoDB can match the query condition as well as return the result fields using the same index without looking inside the documents. Since indexes are stored in RAM or sequentially located on disk, such access is a lot faster.