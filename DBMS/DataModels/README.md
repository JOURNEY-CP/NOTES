## Data Models in DBMS
Data Model gives us an idea that how the final system will look like after its complete implementation. It defines the data elements and the relationships between the data elements. Data Models are used to show how data is stored, connected, accessed and updated in the database management system. Here, we use a set of symbols and text to represent the information so that members of the organisation can communicate and understand it.

### Entity Realtionship Model
An ER model describes the structure of a database with the help of a diagram, which is known as Entity Relationship Diagram (ER Diagram).An ER model is a design or blueprint of a database that can later be implemented as a database
An ER diagram shows the relationship among entity sets
  
3 components of ER-diagram:

- Entities:
  - Entity is a real-world thing. It can be a person, place, or even a concept. Example: Teachers, Students, Course, Building, Department, etc are some of the entities of a School Management System.
- Attributes:
   - An entity contains a real-world property called attribute. This is the characteristics of that attribute. Example: The entity teacher has the property like teacher id, salary, age, etc.
- Relationship:
  - Relationship tells how two attributes are related. Example: Teacher works for a department
  
An entity set is a group of similar entities and these entities can have attributes

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