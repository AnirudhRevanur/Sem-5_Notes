# Unit 4

## Testing
- Testing is a set of activites that can be planned in advance and conducted systematically
- Establishes that the software will perform as expected
- Involves measuring attributes to build confidence
- Tests for low-level necessary to verify that a small segment of the code has been implemented properlu
- High-level tests that validate major system functions against customer requests

### Objectives of Testing
- ___Demonstration:___
  - System used with acceptable risk
  - Functions under special conditions
  - Product ready for integration/use
- ___Detection:___
  - Discover defects, errors and deficiencies
  - Determine capabilites and limitations
  - Quality of components
- ___Prevention:___
  - Info to prevent/reduce errors
  - Reduce error propagation
  - Clarify system specifications and performance
  - Identify ways to avoidd risks and problems

### Verification
- Is the right product being built?
- Process of checking that software achieves its goals to ensure products and deliverables meet
- ___Static Testing:___
  - Does not execute code
  - Check documents, design and code walkthroughs, inspections etc.
- Find bugs early in dev
- Targets software architecture, design, db etc
- Occurs before validation

### Validation
- Are we building the right product?
- Focuses on product related activites that determine if the system or project deliverables meet customer expectations
- ___Dynamic Testing:___
  - Execution of code
  - Validates capabilites and features in project scope and requirements
  - Typically done by the testing team
- ___Methods:___ Black Box testing, White Box Testing and Non-Functional Testing

### Terminologies
#### Defect
- Deviation from requirements
- Fault/Imperfection due to the Design requirement being wrong
#### Bug
- Coding error that prevents intended working
- Programmer's mistake
#### Failure
- Resulting state due to a defect
- Occurs during development lifecycle
#### Issue
- Raised by end user when product doesn't meet expectation

## Categorization
- Functional, Structural, Static, Dynamic

### Black Box Testing
- Functional Testing
- Treats software as a black box
- No regards to structure or logic
- Concerned with the external behaviour
- Tested from User POV
- Test cases are provided to the tester and the results are verified
- ___Advantages:___
  - Best for larger units of code
  - Early test planning
- ___Disadvantages:___
  - Some paths may not be tested
  - Hard to direct tests to error prone code

### White Box Testing
- Structural Testing
- Test the internal logic and structure of the code
- Test specifier uses the knowleedge of the internal structure to derive test cases
  - Test cases cannot be designed until code has been written
- Test from Dev POV
- Tester's should have programming skills
- ___Advantages:___
  - Partitioning execution equivalence
  - Reveals hidden errors
- ___Disadvantages:___
  - Needs skilled testers
  - Hard to test all code

### Static Testing
- Check for defects in the software without executing the code
- Performed in early stages of development to avoid errors
- Easier to find the source and solution
- ___Review:___
  - Informal
  - Walkthrough
  - Peer Review
  - Inspection
- ___Static Analysis:___
  - Evaluation of Code Quality
  - Data Flow
  - Control Flow
  - Cyclomatic Complexity

#### Cyclomatic Complexity
- Is the quantitative measure of the number of linearly independent paths in a code
- Indicates the complexity of a program and is computed using control flow graph
- ___Control Flow Graph:___
  - Directed graph where nodes represent the smalled group and edges connect two blocks of commands
- ___Cyclomatic Complexity = Edges - Nodes + 2*(Number of connected components)___
- Number of connected components is usually 1

### Dynamic Testing
- Involves the execution of code for analyzing dynamic behaviour
- Provide input values, observe the output values
- ___Advantage:___ Finds difficult and complex defects
- ___Disadvantage:___ Time and Budget
- Kinds of Dynamic Testing:
  - Code or Fault Based
  - Approach for testing
  - How testing is done
  - Levels of testing

#### Code Based approach
##### Control Flow Based
- Graphical representation of all the paths that might be traversed
- ___Path testing:___ Statement, Brach and Condition testing
- ___Branch coverage:___
  - Tests every branch at least once
  - No branch leads to abnormal behaviour
##### Data Flow based criteria
- Selecting paths through programs control flow in order to explore sequences of events related to status of variables or data objects
- ___Statement Coverage:___
  - Executes all statements at least once
  - No side effects

#### Approach Used
##### Equivalence Partitioning and Boundary values
- Uncover errors and reduce test cases
- Divide input data into partitions from which test case are derived per partition
- Bounday value analysis handles edge case
##### Specification Based
- Test according to stated requirements
- Test the behaviour of the system based on specific input
##### Intuition Based
- Rely on tester's experience
##### Usage Based
- Finding defects that are revealed by user as they interact with the product
##### Application Domain
- Use specific knowledge of product domain to make test cases

#### Mode of Testing
##### Manual testing
- Slow and tedious
- Used in complex testing scenarios where automation is expensive
- Ex: Acceptance testing, Black Box Testing, White Box Testing etc.
##### Automated Testing
- Testing without human assistance
- Fast and repeatable
- Most efficient for periodic and regular tests

## Levels of Testing

### Unit Testing
- Innermost Layer
- Verifies proper functioning of the individual unit
- ___Focus:___ Test for coding/construction errors prior to quality engineering
- Tests the smallest individually executable code
  - Done by the programmers
- Test cases for
  - Algorithms and logic
  - Data Structures
  - Interfaces
  - Independent Paths
  - Boundary conditions
  - Error Handling
- In Object Oriented Programming, tests are at class level using constructors and destructors

### Integration Testing
- Focuses on finding interface errors between components
- Bugs that are not identified during unit testing
- ___Focus:___ Verify the interface between components against a software design
- Performed by programmers to isolate timing and resource contention problems
- ___Approach:___ Look at the issues that rise when modules are put together
#### Strategies
- ___Big Bang Approach:___
  - Integrate everything and run to see if system works
- ___Iterative Approach:___
  - Software components are integrated iteratively until software works
  - Top down or Bottom Up

### System Testing
- Assesment of the entire system behaviour
- Info that helps direct product release
- Discover bugs that cannot be attributed to single component
- Tests a completely integrated system to verify compliance
- Detects defects both within inter-assemblages and within the system as a whole
- Black Box Testing which involves testing from end-to-end flow of an application
- ___Process:___
  - Test Environment Setup
  - Create Test Case
  - Create Test Data
  - Execute Test Case
  - Defect Report and Logging

### Acceptance Testing
- Done by system users/providers
- Determines if the system meets the needs
- Involves running a suite of tests on the completed system
- Each test case exercises a particular operating condition
  - Test environment has to be designed as indentical as possible
- Tests are created through collaboration between customer, business analysts, testers and developers
- Verifies the completeness of a user story during a sprint
- Provides confidence that the delivered system meets the business requirements of sponsors and users








