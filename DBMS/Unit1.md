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
- Sharing 



  
