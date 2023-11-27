## 2nd Normal Form
- Table or relation must be in 1st normal form
- All the non-prime attributes should be fully functionally dependent on Candidate Key

## 3rd Normal Form
- Table should be in 2nd Normal Form
- There should be __no__ transitive dependency in the table

## Boyes Codd Normal Form
- Gets more and more restrictive
- Table should be in 3rd Normal Form

___Third Normal form always ensures `Dependency Preserving Decomposition` but it is not true in BCNF___


### Normalization:
- The process of decomposing unsatisfactory and bad relations by breaking up their attributes into smaller relations

### Normal Form:
- Condition using keys and Functional Dependencies of a relation to certify wheter a relational schema is in a particular normal form

### Practical Use of Normal Forms

#### Normalization:
- Normalization is carried out in practice so that the resulting designs are of high quality and meet the desirable properties
- Database designers need not normalize to the highest possible degree

#### Denormalization
- Process of storing the join of higher normal form relations as a base relation - which is in a lower normal form

### First Normal Form
- Disallows:
  - Composite Attributes
  - Multivalued Attributes
  - Nested Relations
- Part of the definition of a relation


## Transaction

- It is a set of operations used to perform a logical unit of work
- Transaction generally represents a change in database

### Operations in a transaction:
- Read, Write, Commit
- Read: Access the database
- Write: Change the values in the database
- Commit: Push all the changes to the database

### ACID Properties:
#### Atomicity:
- All or None
- All the operations are performed, or none of the steps are performed
- If the transaction fails during _any_ step before commit, then it will rollback to the first step

#### Consistency:
- Before the transaction starts and after transaction completes, sum of the total money should be the same

#### Isolation:
- Make all the parallel schedule to serial schedule, because then it will be consistent

#### Durability:
- All the changes made should be permanent

### Scheduling
- Schedule is a collection of Transactions
#### Serial:
- If T1, T2, T3 are tasks, then only one task can be done at a time.
- Its advantage is that it is consistent and security
- Disadvantage is waiting time, performance will decrease
- Example: ATMs

#### Parallel Schedule:
- Multiple transactions can be done at a time
- CPU is switching resources
- The advantage is that performance is very high

##### Common issues under Parallel:
- Write-Read Conflict also called as Dirty Read
- Read-Write Conflict also called as Unrepeatable Read




