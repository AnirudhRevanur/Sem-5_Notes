# Unit 3

## Software Implementation

|Prior to Implementation|During Implementation|
|:---:|:---:|
|1. Choose between compiled/interpreted langauge|Use coding standards and Coding guidelines|
|2. Decide on development environment|Address Quality, Security and Testability|
|3. Follow Configuration Management Plan|Provide Unit Tested, Peer-Reviewed Functioning Code|


- ___Software Implementation:___ Detailed creation of working software through a combination of coding, reviews and Unit Testing
- Goals:
  - Minimize Complexity
  - Reuse
  - Anticipate Change
  - Readable
  - Verifiable

- Characteristics
  - Produces High Volume of configuration Items
    - Source Files, Test Cases
  - Extensive usage of Computer Knowledge
    - Algorithms, Coding
  - Related to Software Quality
    - Clean and maintainable Code
  - Tool Intensive
    - Compilers, Debuggers, GUI Builders

- Choice of Programming Language
  - __Assembly:__ Maps directly onto CPU Architecture
  - __Procedural:__ Modset level of abstraction from underlying layers
  - __Aspect Orientation Support:__ Allow separation of aspects during development
  - __Object-Oriented:__ Allows the developer to code in terms of objects

- Choice of Development Environment
  - Commercial vs Open Source
  - Support of Development Process
  - Security
  - Account for future capabilites
  - Integration between toold and environment

- Locations to catch a bug
  - Coding
  - Code review
  - Unit Testing
  - Integration Testing
  - System Testing
  - Field Trials
  - Production

- Characteristics of Code
  - Programs should be simple and clear
  - Naming
  - Structuring
  - Easy to read and understand

- Programmers should use a reasonable amount of
  - Lines per function
  - Lines/Functions per file
  - Arguments per function
  - Levels of Nesting
  - Conditions

- Naming convention
  - Names have to be meaningful and descriptive
  - Avoid using similar keywords
  - No variable name should start with "_"
  - Use minimum 2-3 characaters and max of 30 chars in a name
  - Do not use numberic values that are used elsewhere in a name

- Types of Naming
  - Pascal Casing
    - Ex: BackColor
    - Uses: Class/Variable Names, Method Parameters
  - Camel Casing
    - Ex: backColor
    - Usage: Method Names
  - Underscore Prefix
    - Underscore then camelCase
    - Ex: _backColor
    - Usage: Internal Use in Class/Methods


- ___Structure:___ Dependencies between software components (subprograms, parameters etc)
- ___Dependencies:___ Can be highlighted via proper naming and layout

- ___File Structure:___
  - Logically grouped
    - `#includes, #defines, structures, functions`
  - Well Partitioned
    - Decide what goes into the header files, and what goes in the C files
    - Which functions/variables are to be exposed

- ___Code and Data Structure:___
  - Well encapsulated and logically grouped
  - Properly Initialized

- __Readability__ depends on identifier naming and visual layout of statements
  - Ex: Usage of standardized indentation, blank lines and spaces to illustrate blocks of code and hierarchy

- Comments should concisely explain the logic of the program. They should not be cryptic or misleading

### Good Programming Style

|Do|Don't|
|:-:|:-:|
|1. Use few standards and agree on constructs|Dont' be too clever|
|2. Use `GOTO` in a disciplined manner. Use user defined data types to model entities|Avoid dangling if(null then)|
|3. Hide data structures behind access functions|Avoid Then If statements|
|4. Use appropriate variable names|Don't nest too deeply|
|5. Use indentation, paranteses, blank space and lines to enhance readability|Don't use same identifier for multiple purposes|
|`NULL`|Examine routines that have more than five formal parameters|

- ___Standards:___ Rules that have to be followed
- ___Guidelines:___ Rules which are recommended to be followed
- Practiced as a checklist, enforces as a part of reviews

- Coding Standards
  - Provides a uniform apperance to code written by different engineers
  - Improves readability, maintainability, and reduces complexity
  - Proactively addresses some commonly occuring issues with code
  - Helps in code reuse
  - Promotes sound programming practices and increases efficiency of programmers

- Examples:
  - Rules for usage of global about which type of data
  - Standard headers for different modules
  - Naming Conventions
  - Error and Excxeption Handling

- Common Coding Practices
  - Defensive Programming
  - Secure Programming
  - Testable Programming

### Defensive Programming
- Redundant code is incorporated to check system state after modification
- Implicit assumptions are tested explicitly

### Secure Programming
- Developing computer software to guard against accidental introduction of security vulnerabilities
- Some practices
  - Validate Input
  - Heed compiler Warning
  - Default Deny
  - Adhere to Principle of Least Privilige
  - Sanitize Data sent to other systems

### Testable Programming
- Develop computer software that is easy to test, find and fix bugs
- Some practices
  - Assertions
  - Tets Points
  - Scaffolding
  - Test Harness
  - Test Stubs
  - Instrumenting
  - Build test data sets

## Managing construction
- Minimizing complexity
- Anticipating Change
- Verifiable software solutions
- Constructing software using standards

|Proceeding as Planned?|Technical Quality?|
|:--:|:--:|
|1. Development progress and productivity|Ease in debugging, maintaining, extending etc|
|2. __Measures:__ Effort expenditure, Rate of completion, Productivity|Lines of Code, Number of defects, Code complexity
|3. __Metrics:__ LoC/effor dats, LoC generated|No of errors/KLoc|
|4. Adjust plans based on milestones|Adjust the construction plans or processes|

- ___Sprint Burndown:___
  - Graphically communicated key metric representing completion of work throughout sprint based on story points
  - Goal of team is to consistently deliver all work

- ___Team Velocity Metric:___
  - "Amount" of software or stories completed during a sprint
  - Can be meausured in story points of hours
  - Used for estimation and planning

- ___Throughput:___
  - Indicates total value-added work output by the team
  - Represented by units of work completed in period of time

- ___Cycle Time:___
  - Total time that elapses from the moment work is started until its completion

### Construction Technical Quality
1. _Peer Review:_ Common and informal process of seeking advice or comments from others
2. _Unit Testing:_ Writing code that calls individual modules/functions and tests their workin
3. _Test-first:_ Designing and building test harness before code
4. _Code stepping:_ Code is executed one statement at a time and the values of variables and flow of control is analyzed
5. _Pair Programming:_ Two developers work on same code with one focusing on logic and another on syntax
6. _Debugging:_ Analyzing code to locate a known defect
7. _Code inspection:_ Formal process of Peer Review
8. _Static Analysis:_ Examination of code without execution


#### Code review
- What to review for?
  - Correctness
  - Error handling
  - Readability
  - Coding standars
  - Optimization

- ___Software Inspection:___ Examining the source representation with the aim of discovering anomalies and defects
- Check conformance with a specification but not with real requirements
- Formalized appriace to code/document reviews

- Preconditions
  - Precise specification must be available
  - Team memebers must be familiar with organization standards
  - Syntactially correct code or other representations must be available
  - Error checklist

### Unit Testing Tools
- Unit Testing Frameworks
  - Allow the tester to enter method name, parameters an expected results
  - Framework supplies method call, return value and error comparision
  - NUnit for .NET and JUnit for Java

- Code Coverage
  - Helps identify code that is not covered by test cases
  - CoCo for C, JaCoCo fo Java
  - Debuggers help in finding bugs, Ex: GDB

- Record-Playback Tools
  - Lets the tester start a session and records every keystroke and mouse for replay
  - Selenium


## Software Configuraiton Management
- ___SCM:___ Process to systematically organize, manage and control changes in documents, code and other entities that constitute a software product

- Goal: Increase productivity by increased planned and coordination among the programmers and eliminates cofusion and mistakes
  - Identifying elements and configurations, tracking changes, version selection, control and baselining
  - Avoid config related problems
  - Effective management of simultaneous updating of source files
  - Build Management
  - Defect Tracking

### Need for SCM
- Software engineering in large products with multiple people need to be reliably managed for
  - Multiple people working on same piece of software
  - Working on more than one version
  - Released systems
  - Changes in configuration due to changes in user requirements
  - Custom configured systems
  - Software must run on different machines
  - Coordination among stakeholders
  - Controlling costs in making changes
  
- SCM in Scrum Agile Approach
  - SCM is the responsiblity of the "whole team" and is automated as much as possible
  - Definitive versions of components are held in a shared paroject repo
  - Developers copy versions from the repo into workspaces, make changes and use the system-building tools to create a new system on their computer
  - Once the changes are tested, the modified components are pushed to parent repo
  - Versions of the modified code is available to all team members

- Benefits of SCM
  - Permits orderly development of software config items
  - Ensures the orderly release and implementation of new or revised software products
  - Ensures only approved changes are implemented in accordance with approved specifications
  - Ensure that documentation accurately reflects updates
  - Evaluates and communicates the impact of changes
  - Prevents unauthorized changes from being made


### Configuration Management Roles
- Config manager
  - Identify configuration items
  - Define procedures for creating promotions and releases
- Developer
  - Creates versions triggered by change requests or normal development activiteies
  - Checks in changes and resolves conflicts
- Auditor
  - Validate processes for selection and evaluation of promotions for release
  - Ensures consistency and completeness
- Change Control Board Member
  - Responisble for approving or rejecting change requests

### SCM Planning
- Planning is done by a configuration manager and starts during the early phases of the project
- Results in the SCM Plan
  - May follow a public or internal standard
  - Defines the configuration items and a naming scheme
  - Define who takes responsibilty for Config Management procedues and creation of baselines
  - Defines policies for change control and version management
  - Describe tools to assist in Config Management and any limitations
  - Defines config management database

### Configuration Items
- Independent or aggregation of hardware, software or both, that is designated for config management and treated as a single entitiy
- Software config items could be
  - All types of code files
  - Requirement, Analysis, Design, Test and other non-temp docs
  - User or developer manual
  - System configs

- Challenges associated with config items
  - Some items must be maintained for the lifetime of the software. These need Configuration Control
  - If you place entities under config control too early, it leads to too much bureaucracy. If it's too late, then leads to chaos

### SCM Directories
- Programmer's Directory
  - Lib for hodling newly created/modified software entities
  - Controlled by programmer
- Software Repo
  - Archive for various baselines in general use
  - Copies may be made available on request
- Master Directory
  - Controlled Library
  - Manages current baselines and for controlling changes
  - Entry is controlled after verification
  - Changes must be authorized






