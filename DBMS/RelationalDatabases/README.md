## RDBMS:
RDBMS stands for relational database management system. A relational model can be represented as a table of rows and columns. A relational database has following major components:
### Table:
A table is a collection of data represented in rows and columns. Each table has a name in database.
### Record or Tuple:
Each row of a table is known as record. It is also known as tuple.
### Field or Column name or Attribute:
For example if we see student database table, stud_id,stud_name,stud_addr and stud_age are attributes.
### Domain:
A domain is a set of permitted values for an attribute in table. For example, a domain of month-of-year can accept January, February,…December as values,a domain of dates can accept all possible valid dates etc. We specify domain of attribute while creating a table.An attribute cannot accept values that are outside of their domains.For example if we declare stud_id as int in student database table so that stud_id cannot accept values that are not integers for example, stud_id cannot has values like, “First”, 10.11 etc.
### Instance and Schema:
It is already discussed in intro part please recheck there.

![student table](https://media.geeksforgeeks.org/wp-content/uploads/image7.png)

### Keys
#### Candidate Key:
minimal set of attributes which can be uniquely identify a tuple is known as candidate key.For example, STUD_NO in STUDENT relation.
- The value of candidate key is unique and non-null for every tuple.
- there can be more than one candidate key in a relation.For example, STUD_NO is candidate key for relation STUDENT.
- candidate key can be simple(having only one attribute) or composite as well.For example, {STUD_NO, COURSE_NO} is a composite candidate key for relation STUDENT_COURSE.
- No of candidate keys in a Relation are nC(floor(n/2)),for example if a Relation have 5 attribute i.e. R(A,B,C,D,E) then total no of candidate keys are 5C(floor(5/2))=10.
- 
### Super Key:
The set of attributes which can uniquely identify a tuple is known as Super Key. For Example, STUD_NO, (STUD_NO, STUD_NAME) etc.
- Adding zero or more attributes to candidate key generates super key.
- A candidate key is super key but not vice versa.
  
### Primary Key:
There can be more than one candidate key in relation out of which one can be choosen as primary key.For example,STUD_NO, as well as STUD_PHONE both, are candidate keys for relation STUDENT but STUD_NO can be chosen as the primary key (only one out of many candidate keys). 

### Alternate Key:
Out of all candidate keys, only one gets selected as primary key, remaining keys are known as alternate or secondary keys.

### Composite Key:
A key that consists of more than one attribute to uniquely identify rows (also known as records & tuples) in a table is called composite key.

### Foreign Key:
Foreign keys are the attributes of a table that points to the primary key of another table. They act as a cross-reference between tables.
- Note: Unlike primary key of any given relation, Foreign Key can be NULL and may contain duplicate tuples. i.e. it need not follow uniqueness constraint. 
- For Example, STUD_NO in STUDENT_COURSE relation is not unique. It has been repeated for the first and third tuple. However, the STUD_NO in STUDENT relation is a primary key and it needs to be always unique and it cannot be null. 

## Introduction to Relation Algebra and Relational Calculus:
 In the previous tutorials, we discussed the designing of database using Relational model, E-R diagram and normalization. Now that we have designed the database, we need to store and retrieve data from the database, for this purpose we need to understand the concept of Relational algebra and relational calculus.

### Query Language:
 A language which is used to store and retrieve data is known as Query language. For example, SQL.
 These are 2 types:
#### 1. Procedural Query language:
In procedural query language user instructs the system to perform a series of operations to produce desired results. Here users tells what data to be retrieved from database and how to retrieve it.
For example, Let’s take a real world example to understand the procedural language, you are asking your younger brother to make a cup of tea, if you are just telling him to make a tea and not telling the process then it is a non-procedural language, however if you are telling the step by step process like switch on the stove, boil the water, add milk etc. then it is a procedural language.

#### 2. Non-procedural query language:
In Non-procedural query language, user instructs the system to produce the desired result without telling the step by step process. Here users tells what data to be retrieved from database but doesn’t tell how to retrieve it.

![query language](https://beginnersbook.com/wp-content/uploads/2019/02/Relational_algebra__calculus.png)

#### NOTE:
- Relational algebra and calculus are the theoretical concepts used on relational model.
- RDBMS is a practical implementation of relational model.
- SQL is a practical implementation of relational algebra and calculus.

## Relational Algebra:
Relational Algebra is a procedural query language that works on relational model.The purpose of a query language is to retrieve data from database or perform various operations such as insert, update, delete on the data. When I say that relational algebra is a procedural query language, it means that it tells what data to be retrieved and how to be retrieved.

## Types Of Operations in Relational Algebra:

### Basic/Fundamental Operations:
```
Table: CUSTOMER
---------------

Customer_Id     Customer_Name      Customer_City
-----------     -------------      -------------
C10100           Steve              Agra
C10111           Raghu              Agra
C10115           Chaitanya          Noida
C10117           Ajeet              Delhi
C10118           Carl               Delhi
```
#### Select Operator (σ):
- It is used to find tuples or rows in the relation which satisfy given condition.
- It is similar to "where clause in sql".
- Syntax : σ Condition/Predicate(Relation/Table name).
  
Query: 

σ Customer_City="Agra" (CUSTOMER)

output:
```
Customer_Id   Customer_Name    Customer_City
-----------   -------------    -------------
C10100        Steve            Agra
C10111        Raghu            Agra
```

#### Project Operator (∏):
- It is used to select desired columns(or attributes) from a table(or relation).
- It is similar to "Select statement in SQL".
- Syntax : ∏ column_name1, column_name2, ...., column_nameN(table_name).

Query: 

∏ Customer_Name, Customer_City (CUSTOMER)

Output:
```
Customer_Name      Customer_City
-------------      -------------
Steve              Agra
Raghu              Agra
Chaitanya          Noida
Ajeet              Delhi
Carl               Delhi
```

#### Union Operator(∪):
- It is used to select all rows from 2 tables(relations).
-  Lets say we have two relations R1 and R2 both have same columns and we want to select all the tuples(rows) from these relations then we can apply the union operator on these relations.
-  The rows (tuples) that are present in both the tables will only appear once in the union set. In short you can say that there are no duplicates present after the union operation.
-  Syntax : table_name1 ∪ table_name2

```
Table 1: COURSE

Course_Id  Student_Name   Student_Id
---------  ------------   ----------
C101        Aditya         S901
C104        Aditya         S901
C106        Steve          S911
C109        Paul           S921
C115        Lucy           S931
```
```
Table 2: STUDENT

Student_Id     Student_Name   Student_Age
------------   ----------     -----------
S901           Aditya         19
S911           Steve          18
S921           Paul           19
S931           Lucy           17
S941           Carl           16
S951           Rick           18
```
Query:

∏ Student_Name (COURSE) ∪ ∏ Student_Name (STUDENT)

Output:

```
Student_Name
------------
Aditya
Carl
Paul
Lucy
Rick
Steve
```
#### Intersection Operator (∩):
- it is used to select common rows (tuples) from two tables (relations).
-  Only those rows that are present in both the tables will appear in the result set.
-  Syntax : table_name1 ∩ table_name2.

Query :

∏ Student_Name (COURSE) ∩ ∏ Student_Name (STUDENT)

Output :

```
Student_Name
------------
Aditya
Steve
Paul
Lucy
```
#### Set Difference (-):
- Lets say we have two relations R1 and R2 and we want to select all those tuples(rows) that are present in Relation R1 but not present in Relation R2, this can be done using Set difference R1 – R2.
- Syntax : table_name1 - table_name2.
  
Query : 
∏ Student_Name (STUDENT) - ∏ Student_Name (COURSE)

Output : 

```
Student_Name
------------
Carl
Rick
```
#### Cartesian product (X) :
- Lets say we have two relations R1 and R2 then the cartesian product of these two relations (R1 X R2) would combine each tuple of first relation R1 with the each tuple of second relation R2. I know it sounds confusing but once we take an example of this, you will be able to understand this.
- Syntax : R1 X R2

```
Table 1: R1

Col_A    Col_B
-----    ------
AA        100
BB        200
CC        300 
```

```
Table 2: S

Col_X     Col_Y
-----     -----
XX         99
YY         11
ZZ         101
```
Query :

R X S

Output : 

```
Col_A    Col_B     Col_X     Col_Y
-----    ------    ------    ------
AA        100      XX         99
AA        100      YY         11
AA        100      ZZ         101
BB        200      XX         99
BB        200      YY         11
BB        200      ZZ         101
CC        300      XX         99
CC        300      YY         11
CC        300      ZZ         101
```

#### Rename (ρ) :
- It is used to rename a relation or an attribute of a relation.
- Syntax : ρ(new_relation_name, old_relation_name).

```
Table: CUSTOMER

Customer_Id     Customer_Name      Customer_City
-----------     -------------      -------------
C10100           Steve              Agra
C10111           Raghu              Agra
C10115           Chaitanya          Noida
C10117           Ajeet              Delhi
C10118           Carl               Delhi
```
Query :
 
ρ(CUST_NAMES, ∏(Customer_Name)(CUSTOMER))

Output :

```
CUST_NAMES
----------
Steve
Raghu
Chaitanya
Ajeet
Carl
```


