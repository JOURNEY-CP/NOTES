## Functional Dependency in DBMS(FD) : 
The attributes of a table is said to be dependent on each other when an attribute is uniquely identifies another attribute of same table.It is denoted by an arrow "→". The functional dependency of X on Y is represented by X → Y.

Formally, If column A of a table uniquely identifies the column B of same table then it can represented as A->B (Attribute B is functionally dependent on attribute A).

For example, Suppose we have a student table with attributes: Stu_Id, Stu_Name, Stu_Age. Here Stu_Id attribute uniquely identifies the Stu_Name attribute of student table because if we know the student id we can tell the student name associated with it. This is known as functional dependency and can be written as Stu_Id->Stu_Name or in words we can say Stu_Name is functionally dependent on Stu_Id.

## Rules of Functional Dependencies : 
### Reflexive Rule :
In the reflexive rule, if Y is a subset of X, then X determines Y.

```
If X ⊇ Y then X → Y 
```
### Augmentation Rule :
The augmentation is also called as a partial dependency. In augmentation, if X determines Y, then XZ determines YZ for any Z in attribute set.

```
If X → Y then XZ → YZ  
```
Example :
```
For R(ABCD),  if A → B then AC → BC
```
### Transitive Rule  :
In the transitive rule, if X determines Y and Y determine Z, then X must also determine Z.

```
If X → Y and Y → Z then X → Z 
```
### Union Rule :
Union rule says, if X determines Y and X determines Z, then X must also determine Y and Z.

```
If X → Y and X → Z then X → YZ  
```
### Decomposition Rule :
Decomposition rule is also known as project rule. It is the reverse of union rule.This Rule says, if X determines Y and Z, then X determines Y and X determines Z separately.

```
If X → YZ then X → Y and X → Z
```
### Pseudo Transitive Rule :
In Pseudo transitive Rule, if X determines Y and YZ determines W, then XZ determines W.

```
If X → Y and YZ → W then XZ → W 
```
## 4 types :
### Multivalued dependency :
Multivalued dependency occurs when there are more than one independent multivalued attributes in a table.

For example: Consider a bike manufacture company, which produces two colors (Black and white) in each model every year.

```
bike_model	manuf_year	  color
M1001	    2007	      Black
M1001	    2007	      Red
M2012	    2008	      Black
M2012	    2008	      Red
M2222	    2009	      Black
M2222	    2009	      Red
```
Here columns manuf_year and color are independent of each other and dependent on bike_model. In this case these two columns are said to be multivalued dependent on bike_model. These dependencies can be represented like this.
```
bike_model ->> manuf_year
```
### Trivial functional dependency :
The dependency of an attribute on a set of attributes is known as trivial functional dependency if the set of attributes includes that attribute.
- Symbolically : A ->B is trivial functional dependency if B is a subset of A.
- The following dependencies are also trivial: A->A & B->B.

```
Emp_id	Emp_name
AS555	Harry
AS811	George
AS999	Kevin
```

Here, {Emp_id, Emp_name} -> Emp_id is a trivial functional dependency as Emp_id is a subset of {Emp_id,Emp_name}.
### Non-Trivial functional dependency :
If a functional dependency X->Y holds true where Y is not a subset of X then this dependency is called non trivial Functional dependency.
```
Emp_id	Emp_name  Emp_address
AS555	Harry     hyderabad
AS811	George    durgapur
AS999	Kevin     bangalore
```
The following functional dependencies are non-trivial :

emp_id -> emp_name (emp_name is not a subset of emp_id)

emp_id -> emp_address (emp_address is not a subset of emp_id)

### Transitive dependency :
A functional dependency is said to be transitive if it is indirectly formed by two functional dependencies.

X -> Z is a transitive dependency if the following three functional dependencies hold true:
- X->Y
- Y does not ->X
- Y->Z

Note: A transitive dependency can only occur in a relation of three of more attributes. This dependency helps us normalizing the database in 3NF (3rd Normal Form).

```
Book	            Author	                Author_age
Game of Thrones	    George R. R. Martin	    66
Harry Potter	    J. K. Rowling	        49
Dying of the Light	George R. R. Martin	    66
```
Here, {Book} ->{Author} (if we know the book, we knows the author name)

{Author} does not ->{Book}

{Author} -> {Author_age}

Therefore as per rule of transitive dependency {Book} -> {Author_age} should hold, that makes sense because if we know the book name we can know the author’s age.




