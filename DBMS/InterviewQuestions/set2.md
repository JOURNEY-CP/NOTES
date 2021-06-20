# DBMS-Interview-Questions

***Q1. What are the differences between a DBMS and RDBMS?***
1. DBMS stores data as file, RDBMS stores in Tabular form.
2. Also, the relationship between various tables will be stored in tables as well.
3. RDBMS implies entity integrity
4. Normalization is present in RDBMS
5. RDBMS defines integrity constraints to maintain ACID property.
6. RDBMS supports distributed databases.  
[Reference](https://www.javatpoint.com/difference-between-dbms-and-rdbms)

***Q2. Explain the terms database and DBMS. Also, mention the different types of DBMS.***
**Database:**   
Database is a collection of data stored in structured tabular form. 
  
**DBMS:**   
Database Management System is a software application which helps user to interact, analyze and perform CRUD operations on the information stored in databases.  
Different types of DBMS are as follows;
1. Relational DBMS
2. Hierarchical DBMS
3. Network DBMS
4. Object Oriented DBMS  
[Reference](https://www.guru99.com/what-is-dbms.html)

***Q4. Mention the different languages present in DBMS.***
1. **DDL - Data Definition Language**  
Used to design and modify the structure of databases and it's objects
- CREATE
- ALTER
- DROP

2. **DML - Data Manipulation Language**  
To perform CRUD operations over databases/ objects
- INSERT
- SELECT
- UPDATE
- DELETE

3. **DCL - Data Control Language**  
It defines access control definitions of databases
- GRANT
- REVOKE

4. **TCL - Transaction Control Language**  
These are used to manage the transactions in databases. They manage the changes made by DML commnands.
- COMMIT
- ROLLBACK
- SAVEPOINT

***Q5. What do you understand by query optimization?***  
**Query optimization** is the process of determining the fastest way to execute a given query by considering the costs of all the possible *query plans*.  
**Query plan** or **query execution plan** is a sequence of steps used to access data in a SQL relational DBMS.

***Q6. Do we consider NULL values the same as that of blank space or zero?***  
No, we do not consider zero or blank space same as null value.  
**Null:** It represents that the value is unavailable, unassigned, unknown or not applicable.  
**Zero:** It is a number and determines that the value is 0.  
**Blank space:** It is a character.  

***Q8. What are the different levels of abstraction in the DBMS?***  
There are three levels of abstraction in DBMS:
1. View Level
	- It is the highest level of abstraction.
	- It describes how the data is visible and accessible to various users.
2. Logical Level
	- It is the lower level of abstraction in DBMS.
	- It determines what data is stored in databases and the relationships between them.
3. Physical Level
	- It is the lowest level of abstraction in DBMS.
	- It describes where and how the data is stored.
	
***Q9. What is an entity-relationship model?***  
**Entity-Relationship Model** is a diagrammatic approach to design databases where the real-life objects are represented as *entities* and also the *relationships* between them are included.  
The ER model helps the users to understand the schema easily.
  
***Q10. What do you understand by the terms Entity, Entity Type, and Entity Set in DBMS?***  
**Entity:**  
Entity is a real-life object which can be identified uniquely with it's *attributes* or characteristics.  
    
**Entity Type:**  
Enity type is a collection of entities having similar attributes.  
  
**Entity Set:**  
A collection of more than one *entities* of the same *entity type* are called as entity set.  
  
***Q11. What are relationships and mention different types of relationships in the DBMS.***  
There are four types of relationships in DBMS:  
1. **One-to-One** - When a single row in Table A is related to the single row in Table B  
2. **One-to-Many** - When a single row in Table A is related to many rows in Table B  
3. **Many-to-Many** - When many rows in Table A are related to many rows in Table B  
4. **Self-Referencing** - When a record in Table is related to the same table itself  
  
***Q12. What is concurrency control?***  
**Concurrency Control** is process of controlling *concurrent execution* of operations on database so that the database integrity is not compromised.  
[Reference](https://www.javatpoint.com/dbms-concurrency-control)  
  
***Q13. What are the ACID properties in DBMS?***  
**Atomicity:**  
Atomicity means that if any operation is performed on the databases, either it should be performed completely, or not executed at all.  

**Consistency:**  
Consistency refers that all values in the database must remain preserved before and after the transaction.  
  
**Isolation:**  
Isolation means that consistency of databases is ensured even in occurrence of concurrent transactions.   
  
**Durability:**  
Durability ensures that after *committing* the operations on databases, all the modifications persists even in case of system failure.  
  
***Q15. What are the different types of keys in the database?***
There are several types of keys in Databases as follows;  
1. **Super Key**  
A set of attributes which can uniquely identitfy every record from a table, is called as *super key*.  
  
2. **Primary Key**  
An attribute which can uniquely identify every record from a table, and selected by the DBA for that purpose, is known as *primary key*.  
  
3. **Candidate Key**    
A minimal *super key* which can uniquely identify every record from the table, is called as *candidate key*.  
  
4. **Alternate Key**  
All the *candidate keys* which are not chosen as *primary key* are called as *alternate keys*.  
  
5. **Unique Key**  
An attribute which has capability to uniquely identify the records from the table like *primary key*, but accepts *null* value as a valid input are called as *unique keys*.  
   
6. **Simple Key**  
A single attribute which can uniquely identify every record in the table is termed as *simple key*.  
   
7. **Composite Key**  
When none of the individual attribute is sufficient to identify every record in the table uniquely, the set of attributes chosen to complete the purpose is called as *compound key*.  
   
8. **Compound Key**     
A set of two or more *simple keys* which can uniquely idenify each record in the table is known as *compound key*.  
  
9. **Natural Key or Business Key or Domain Key**  
An attribute which is already a part of table or holds logical relation with other attributes and uniquely identifies the records in table is called as *natural key*.
  
10. **Surrogate Key or Aritificial Key**  
An artificially generated attributed which was added to uniquely identify the records uniquely and doesn't have any business meaning is known as *surrogate key* or *artificial key*.  
  
11. **Foreign Key**   
An attribute of a *parent table* which generates its relationship with the *child table* is called as *foreign key*. 
  
***Q16. What do you understand by correlated subqueries in DBMS?***  
**Correlated Subquery** or **Synchronized Subquery** is a query *nested* inside an another query that uses the values from outer query.  
Hence, the correlated subquery is executed repeatedly for every row of the outer query.  

***Q17. Explain Database partitioning, its types and the importance.***  
**Database Partitioning** is the process of dividing a large database into *partitions* such that every partition can be managed and access separately.  
  
**Types of Database Partitioning**
1. Horizontal Partitioning  
2. Vertical Partitioning  
3. Functional Partitioning  

**Importance of Database Partitioning**  
1. Scalability  
2. Faster Access and Performance  
3. Improved Security  
[Reference](https://docs.microsoft.com/en-us/azure/architecture/best-practices/data-partitioning)
  
***Q19. What is the difference between two and three-tier architectures?***
**Two-Tier Db Architecture**  
- It is a *Client-Server Architecture*.  
- In two-tier, the application logic is buried inside either client-side machine or the database server or both.  

**Three-Tier Db Architecture**  
- It is a *Web-based application*.
- In three-tier, the application logic resides in the middle-tier or *application server* which is separated from the user and data interface.  
[Reference](https://www.geeksforgeeks.org/difference-between-two-tier-and-three-tier-database-architecture/#:~:text=Two%2Dtier%20architecture%20consists%20of,Business%20Layer%20and%20Data%20Layer.&text=Two%2Dtier%20architecture%20runs%20slower,Three%2Dtier%20architecture%20runs%20faster.)  
[Reference](https://www.guru99.com/dbms-architecture.html)  
  
***Q21. What is a checkpoint in DBMS and when does it occur?***
**Checkpoint** in DBMS is the mechanism where all the previous *logs* (of transactions) are removed from the system and stored in the storage disk. 
Checkpoint declares a point where all the transactions are *committed* and database is in the *consistent* state.  
Thus, checkpoint mechanism ensures the *durability* property of database even in case of unexpected system crash.  

***Q22. Mention the differences between Functions and Stored Procedures and  Trigger.***  
Criteria|Functions|Stored Procedures|Triggers
--------|---------|-----------------|-----------
**Definition**|Functions are the *routines* that could be called to perform certain operations and return the results as a value or in tabular form.|Stored procedures are the *pre-compiled set of SQL statements* which can be stored and reused over and over again.|Triggers are the *stored procedures* which perform operations in response to certain events occuring in the databases.
**Parameter**|Function accepts only input parameters.|Stored Procedures accepts both *in* and *out* parameters.|Triggers *do not accept* any parameters.
**Return Result**|Function *must* return any value, hence always has RETURN and RETURNS arguments.|Stored Procedures *may or may not* return any result.|Triggers *never* return any result.
**Invocation**|Function is called from *SELECT* statements, another *function*, *stored procedures* and *triggers*.|Stored procedures can be invoked from another *stored procedures*, *triggers* and *not from functions*.|Trigger *can not be invoked from either* stored procedures, functions or another triggers.
**Execution**|Function can only be called whenever required.|Stored procedures store the compiled object after first execution, and hence reuses the same for subsequent executions.|Triggers are executed only as the automatic response for certain events in databases.

***Q24. What do you understand by Proactive, Retroactive and Simultaneous Update?***  
**Proactive Update:** Updates which are applied to the databases before the occur in real-world environment.  
e.g. The post-dated cheque.  
**Retroactive Update:** Updates which are applied to the databases after they become effective in real-world environment.  
e.g. Increase in salary of an employee  
**Simultaneous Update:** Updates which are updated in the databases at same time when they are effective in real-world environment.  
e.g. Real-time temperature data logging in an IoT system  