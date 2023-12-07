# Unit 1

## Data
- Represents the raw material, like individual puzzle pieces, that serve as the foundation for knowledge
- Data is raw and unorganized
- It has to be processed to make it meaningful

## Information
- When data is processed, organized, structured or presented to make it useful, it is called as information
- Data is a collection of facts, while information puts those facts into context
- It is organized and is utilized by humans in some significant way to make decisions and draw conclusions

## Database
- Database is a collection of related data representing some aspect of the real world
- Logically coherent collection, not a random assortment of data, but is organized with inherent meaning and structure
- Designed, built and populated for a specific purpose, catering to the needs of applications or systems that interact with them
- Vary in size and complexity, ranging from small databases used by individuals to large-scale enterprise databases handling vast data

## Database Management System
- Modern db system is a complex software system whose task is to manage a large, complex collection of data
- DBMS contains the information about a particular enterprise
  - Collection of interrelated data
  - Set of programs to access the data
  - An environment that is both convenient and efficient to use
- DB Systems are used to manage collections of data that are
  - Highly valuable
  - Relatively large
  - Accessed by multiple users and applications, often at the same time
- ___DBMS:___ A general-purpose software system that facilitates the process of defining, constucting, manipulating and sharing databases among various users and applications

### Defining a database
- Involves specifying the data types, structures and constraints of the data to be stored in the db
- By defining the structure and data types, the DBMS ensures the consistency and integrity of the stored data

### Constructing the database
- Process of storing the data on some storage medium that is controlled by the dbms
- Organizes the data in a way for efficient retrieval and manipulation
- Ensures data is stored securely and can be accessed by authorized users of applications

### Manipulating the database
- Include functions like querying to retrieve data, update the database to reflexct changes and generate reports from the data
- Ensures that any changes made to the database follow predefined constraints and maintain consistency

### Sharing a database
- Allows multiple users and programs to access db at the same time, given they have the necessary permissions

### Why dbs?
- Store large amount of data
- Understand the data
- Keep data secure
- Find required data and use/manipulate it
- Get accurate informatino
- Maintain data integrity

### Database Applications
- Enterprise Information
  - Sales
  - Accouting
  - Human Resources
- Manunfacturing
- Banking and Finance
- Unis
etc.

### How are they used?
- There are two modes in databases are used today

#### Online Transaction Protocol
- Used by large number of users for small data retrieval and updates
- Common in most database applications like banking, unis and airlines

#### Data Analytics
- Processing data to draw conclusions and create predictive models
- Loan apprival, Targeted advertisements and manufacturing decisions
- Data mining combines AI and statistical techniques for efficient analysis of large dbs

## File Processing Systems
- Data redundancy and Incosistency => Takes more storage and can lead to inconsistency in case of any changes
- Diffuculty in accessing the data => Manually have to sift through all the files, or we need to create a special program for this 
- Data is isolated => Data is scattered, so writing an application is quite challenging
- Integrity problems => Need to handle each scenario carefully when making an application
- Atomicity Problems => If computer fails in the middle of a transaction, then there might be partial execution of steps. This should not be the case
- Concurrent access anomalies => If more than one person access, then there might be an issue on the values being read/written
- Security Problems => Users that are not supposed to view data might be able to view data

## Characteristics of Database Systems
- Self describing nature of a database system
  - Not only the database itself, but also a complete definition or description of the database structure and constraints
- Insulation between programs and data
  - Structure of data files is sotred in the DBMS catalog separately from the access programs
- Support multiple views of data
  - Support different kind of viewers based on their permissions and roles
  - View can be a subset or virtual data that can be derived from the remaining tables, but it is not explicitly stored
- Sharing of data and multiuser transaction processing
  - A multiuser DBMS allows multiple users to access the database at the same time
  - Makes sure that changes are effected in a controlled manner

## Advantages of Database Systems
- Controlling redundancy in data storage
- Sharing data among multiple users
- Restricting unauthorized access to data
- Providing persistent storage for program Objects
- Providing storage structures and search techniques for efficient Query Processing
- Provides backup and recovery
- Providing multiple interfaces to different classes of users
- Representing complex relationships among data
- Enforcing integrity constraints on the database
- Drawing interfaces and actions from stored data with triggers
- Potential for enforcing standards
- Reduced application development time
- Flexibility to change data structures
- Availability of current info
- Economies of scale

## View of Data
- A DB system is a collection of interrelated data and a set of programs that allow users to access and modify this data
- Major purpose of db system is provide users with abstract view
  - ___Data Model:___ Collection of conceptual tools for describing data, data relationships and data semantics and consistency constraints
  - ___Data Abstraction:___ Hide complexity of data structures to represent data in the database through several layers of data abstraction
- Structure of db is defined by its data model, which includes tools to describe data, relationships, semantics and constraints

## Relational Model
- Uses a collection of tables to represent both data and relationships among those data
- Tables are also called as relations
- Relational Model is an example of a record based model
- Database is structured in fixed-format records of several types
- Each row of the table represents one piece of information
- Columns of table correspond to the attributes of the record type
- Relational data model is the most widely used data model

## Data Models
### Entitiy Relationship Model
- The ER-data model uses a collection of basic objects, called entities, and relationships among these objects
- Entity is a "thing" in that real worls that is distinguishable from other objects
- ER model is widely used in database design

### Semi Structured Data Model
- Permits the specification of data where individual data items of the same type may have different sets of attributes
- JSON and Extensible Markup Language are widely used semu-structured data representations
- DB Model where there is no separation between the data and the scheme
- The amount of structure used depends on the purpose
- It can represent the info of some data that cannot be constrained by schema

### Object Based Data Model
- Object Oriented Programming led to the development of an object oriented data model, but it is now integrated into relational databases
- Standards exist to store objects in relational tables
- DB systems allow procedures to be stored in and executed by the db system
- This can be seen as extending the relational model with notions of encapsulation, methods and obejct identity

## Data Abstraction
- Need for efficiency has led db developers to use complex data structures to represent data in db
- Developer hides all this complexity from the users through several layers of data abstraction
- Layers:
  - Physical Level
  - Logical Level
  - View Level
### Physical Level
- It is the lowest level of data abstraction
- Describes how the data is actually sotred in the computer
### Logical Level
- Describes what kind of data is stored in the database and how different pieces of information are related to each other
- The logical level thus describes the entire database in terms of small number of relatively simple structures
- More organized and simpler view of the data
### View Level
- Highest level of abstraction that individual users interact with
- Different users might see different parts of database, depending on need and permissions

- User at logical level doesn't need to know about the complexity at the physical level
- User at view level, doesn't need to know about the complexity at the logical level

### Physical Data Independence
- Characteristic of being able to modify the physical schema without any alterations to the conceptual or logical scheme
- Conceptual structure of the db will not be affectedby any change in the storage size of the db system server
- Changing from sequential to random access files is one example
- Without it, minor changes to the storage system or hardware upgrades could potenitally break interfaces, applications or queries

### Logical Data Independence
- Modify the logical schema without affecting the external schema or application program
- User view of the data would not be affected by any changes to the conceptual view
- Includes insertion or deletion of attributes
- Altering table structures entities or relationships to the logical schema
- Without Logical Data Independence:
  - Any alteration to logical schema, like adding or removing attributes/changing relationships between entities would result in changes going through the applications relying on the db
  - Force devs to modify all affected applications
  - Even minor changes can lead to downtime of the application

### Instances and Schema
- Databases change over time as information is inserted and deleted or modified
- Collection of info stored in the db at a particular moment is called instance of db
- Overall design is called as database schema

#### Physical Schema
- Describes the database at the physical level
- Describes how data is stored in the db physically
- Includes detailes like stat storage format, file organization and indexing methods
- Changes here will not affect applications using the db

#### Logical Schema
- Describes the db design at the logical level
- Defines the db design focusing on the structure and relationships between the tables
- Essential for application developers as they build software which is based on logical schema

#### Subschema
- Describe different views that are tailored to specific user needs or applications
- Views allow users to see only relevant information and protect data

  
