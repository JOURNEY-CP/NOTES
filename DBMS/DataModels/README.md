## Data Models in DBMS
Data Model gives us an idea that how the final system will look like after its complete implementation. It defines the data elements and the relationships between the data elements. Data Models are used to show how data is stored, connected, accessed and updated in the database management system. Here, we use a set of symbols and text to represent the information so that members of the organisation can communicate and understand it.

### Entity Realtionship Model
An ER model describes the structure of a database with the help of a diagram, which is known as Entity Relationship Diagram (ER Diagram).An ER model is a design or blueprint of a database that can later be implemented as a database.
An ER diagram shows the relationship among entity sets.
An entity set is a group of similar entities and these entities can have attributes.

![ER-diagram](https://beginnersbook.com/wp-content/uploads/2015/04/E-R-Diagram.png)

In above diagram,
- Rectangle---------->Entity Sets
- Ellipses---------->Attributes
- Diamonds---------->Relationship Set
- Double Ellipses---------->Multivalued Attributes
- Dashed Ellipses---------->Derived Attributes
- Double Rectangles---------->Weak Entity Sets
- Lines---------->They link attributes to Entity Sets and Entity sets to Relationship Set
- Double Lines---------->Total participation of an entity in a relationship set
  
3 components of ER-diagram:

#### Entity:
Entity is a real-world thing. It can be a person, place, or even a concept. Example: Teachers, Students, Course, Building, Department, etc are some of the entities of a School Management System.
##### Weak Entity:
- An entity that cannot be uniquely identified by its own attributes and relies on the relationship with other entity is called weak entity.
- The weak entity is represented by a double rectangle.
- For example, a bank account cannot be uniquely identified without knowing the bank to which the account belongs, so bank account is a weak entity.
#### Attribute:
An entity contains a real-world property called attribute. This is the characteristics of that attribute. Example: The entity teacher has the property like teacher id, salary, age, etc.
4 Types of Attributes:

##### Key Attrubute:
- A key attribute can uniquely identify an entity from an entity set.
- For example, student roll number can uniquely identify a student from a set of students.
- Key attribute is represented by oval same as other attributes however the text of key attribute is underlined.
  
##### Composite Attribute:
- An attribute that is a combination of other attributes is known as composite attribute.
- For example, In student entity, the student address is a composite attribute as an address is composed of other attributes such as pin code, state, country.

##### Multivalued Attribute:
- An attribute that can hold multiple values is known as multivalued attribute.
- It is represented with double ovals in an ER Diagram.
- For example, A person can have more than one phone numbers so the phone number attribute is multivalued.

##### Derived Attribute:
- A derived attribute is one whose value is dynamic and derived from another attribute.
- It is represented by dashed oval in an ER Diagram.
- For example, A Person age is a derived attribute as it changes over time and can be derived from another attribute (Date of birth).
#### Relationship:
  - Relationship tells how two attributes are related. Example: Teacher works for a department
  