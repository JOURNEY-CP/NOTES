## Introduction
DBMS stands for Database Management System. We can break it like this DBMS = Database + Management System. Database is a collection of data and Management System is a set of programs to store and retrieve those data. Based on this we can define DBMS like this: DBMS is a collection of inter-related data and set of programs to store & access those data in an easy and effective manner.

### Need Of DBMS
Database systems are basically developed for large amount of data.
So we need to optamize two feutures
- Low Storage:
  - Avoid duplication of data (reductancy)
  - for this we need to learn Normal forms
- Fast Retrieval of data: 
  - We use b trees and indexing stratagies

### Drawbacks of File system
- Data redundancy: 
  - Duplicate data
  - so much memory is wated
  - Ex : student is enrolled for two courses, the same student details in such case will be stored twice, which will take more storage than needed
- Data inconsistency: 
  - If duplicate data is found we need to update at all places else data inconsistancy will occur.
  - Take above example and assume there is spelling mistake in name. then every techer need to update name if there is duplicate data.
- Data Isolation: Data is present at various files and not properly organized
- Dependency on application programs: As there is no particular pattern a small change in file sysem way needs many changes in application. Ex: if you move a image to some folder X then you need changes in application
- Atomicity issues: A transaction may be partially executed in file system. Building fully automic system is hard. We can take bank transaction example.
- Data Security: Student dont need access of faculty's salary

### Advantage of DBMS over file system
- No redundant data: Because of normal forms 
- Data Consistency and Integrity:  as no reductant data no need to worry on this
- Data Security and Privacy: We can easyly manage access to particular set of people
- Easy access to data: Fast access
- Easy recovery
- Flexible

### Disadvantages of DBMS:
- Implementation cost is high compared to file system
- Complex in understanding
- May effect performance in some apps

## Architecture
### single tier
- local database
- Client -> Client App/local db
- client has complete data
- no need on internet

### two-tier
- Client dirctly access data from sql server
- Client -> Client App ------------> Db Server
- Components
  - Client has user and db app
  - server has only db server

### three-tier
- Client asks data from his app and it askes data to app at server and in contacts db server
- Client -> Client App ------------> Server App -> Db Server
- user -> React App ----------------> ExpressServerApp->SQL_DB
- Components
  - Client has user and db app
  - server has server Db App and db server
- More secure
- Mostly used

## DBMS Three Level Architecture (3 tier)
1. External Level
   - this is the view level
   - which is on client side
   - Ex : React App
2. Conceptual level
   - Logical level
   - We write core logics here
   - We specify access to different people here
   - Duty of Database Administrator
   - Ex : Creating tables and db part of nodejs App
3. Internal level
   - The physical Layer
   - Core Implementation
   - Duty of database system core desinger
   - Ex : As a part of normal app development we dont use this

### Abstraction
- We must ensure that user from view level to not see any data from logical level or physical level.
- And this is maintained in 3 level architecture

### Schema
- The design of database in View layer is View schema
- The design of database in Logical layer is Logical schema
- The design of database in Physical layer is Physical schema

### Instance
- The core desidn is schema and all details(rows) of a particular thing is instance
- In marks sheet (NAME,PHY_MARKS,CHE_MARKS) (all these atributes are combindly called as logical schema)
- each row (describing marks of a particular student) is called Record
- The data stored in database at a particular moment of time is called instance of database.

## Database Languages
1. Data Definition Language (DDL)
    - Used to create the schema, tables indexes etc
    - CREATE ALTER DROP TRUNCATE RENAME COMMENT
2. Data Manipulation Language (DML)
    - Used to add and manipulate data 
    - SELECT INSERT UPDATE DELETE
3. Data Control language (DCL)
    - Used to define access to users
    - GRANT REVOKE
4. Transaction Control Language(TCL)
    - The changes in the database that we made using DML commands are either performed or rollbacked using TCL.
    - COMMIT ROLLBACK