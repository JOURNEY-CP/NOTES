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


