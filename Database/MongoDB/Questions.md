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