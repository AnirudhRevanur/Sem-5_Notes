# Unit 2

## Software Project Management
- Software Projects are temporary individual or collaborative enterprises that are carefully planned to achieve a particular aim

### Characteristics of Software Projects
- Consists of interrelated activites
- Need adequate resources
- Intangible
- Have certain activities which are not repeated under any circumstance
- Goal specific
- Sequence of activities

|Software Project Managemet|Project Management|
|:--:|:--:|
|Art and discipline of planning and supervising software projects|It facilitates the project workflow with team collaboration on a single project|
|Activities towards planning, execution of plans, monitoring and controlling project|Planning, organizing, motivating, controlling the resources to achieve specific project goals, monitoring, risk management etc.|

### Quality of Project
- Is to achieve project goals and targets whilel keeping in mind the __scope__, __time__, __quality__ and cost
- Project Management will need to maintain this triad to remain in equilibrium

### Project Management Life Cycle
1. Initiation and Approval
2. Planning
3. Monitoring Execution and Control
4. Closing

### Software Development Life Cycle
1. Requirements Engineering
2. Architecture
3. Design
4. Implementation
5. Testing
6. Deploy

#### Initiation
- This is the point where opportunity or reason for the project has been identitifies
- Project is initiated after the _"go"_ after the feasibility study
- What is done  during this phase?
  - Project charter is created
  - Project charter outlines purpose, structure and execution of the project
  - Detailing out the responsibilities of the project teams and the stakeholders
  - Initial Project Owner/Manager is identified
  - Initial budget is identified
  - Identification of resources

#### Project Planning
1. Understanding the project
2. Planning the project
3. Organize the project
4. Determining deliverables
5. Work Breakdown Structure
6. Scheduling and Allocating resources
7. Identifying and Managing risks
8. Developing a quality management process for Dev
9. Delivery plan planning to manage the plan

#### Project Monitoring and Control
- Process is continnuously performed and encompasses all the tasks and uses all the measures and metrics necessary to ensure that the project is on track
- __Monitoring:__ Using Quantitative Data which is continuously collected all along the project
- __Control:__ Making decisions or adjustments in dimensions like time or cost

#### Project Closure
1. Hand over deliverables + User Acceptance Test sign off
2. Finish documentation
3. Post implementation review
4. Release staff and equipment + inform stakeholders of closure


## Software Project Planning
- First task in a project
- Project Manager focusses on __what__ and __how__
- The outcome is the Project Plan
  - Depends on nature of the project
  - Project plan can evolve over the lifecycle of the project
- Three perspectives:
  - Sponsor's Perspective
  - Customer's Perspective
  - Execution Stakeholder's Perspective

### Execution Stakeholder's Perspective
- What lifecycle are we gonna follow
- Criteria for prioritizing of requirements
- Project Organizaion
  - Relationships to other parts of organization
  - Roles of people
  - User involvement
- Standards to follow
- Communication Mechanisms
- Schedule with Detailed Work Breakdown and Ownership


### Steps in Project Planning
#### Developing a quality management process
- Plan for progress tracking of the project
- Communication plans
- Quality Assurance plans
- Test completin criteria
- Early verification

#### Plans for tracking Project Plan & Delivery Plan
- Plan for management of Project Plan
- Procedures for release of product to customer
- Staff and people management
- Performance management
- Compensation and benefits management

### Outcomes and Roles
- Outcomes of Project Planning
  - Project Plan
  - Resource Management
  - Work Break down
  - Plans for communication metrics
  - Schedule
  - Risk Management Plan
- Roles
  - Project Management
  - Project Manager

## Proect Monitoring and Control
- Processes performed to observe project execution so that potential problems can be identified in a timely manner
- Project control activites involves making decisions or adjustments in dimensions like time, cost etc
- Dimensions:
  - Time
  - Information
  - Organization
  - Quality
  - Cost & Infrastructure

### Time
- In terms of effort and the schedules
- Measuring progress is hard
- Development models serve to manage time
- More people does not mean less time

### Information
- Includes availability, propogation, communication and documentation
- Technical documentation
- Current state of projects
- Changes agreed upon

### Organization
- Involves structure, roles and responsibilities from people and team aspects
- Building a teaem
- Reorganizing structures
- Clarifying, managing expectations and reorienting roles
- Coordination of work

### Quality
- It is not an add-on feature; it has to be built in
- Quality has to be designed in, not an afterthought
- Quality requirements often conflict
- Requires frequent interaction with stakeholders

### Cost and Infrastructure
- Includes personnel capital and expenses
- What factors influence cost?
- What influences productivity
- Relation between cost and schedule

## Architecture
- ___Architectural Design:___ Describes how softeare is decomposed and organized into components
- ___Detailed Design:___ Describes the specific behaviour of components identified during architectural design
- Well written software will be more maintainable
- ___Mastering Software Development:___
  - Learn rules
  - Learn principles
  - Study architectural and design patterns of other projects
  - Patterns must be understood and applied repeatedly

### Software Architecture
- Top level decompositino into major components with a characterization of how components interact
- Software architecture of computing system can be
  - Used for communication among stakeholders
  - Blueprint for system and project under development
  - Used for negotiations and balancing of functional and quality goals happen during architecture

#### Importance of Architecture
- Architecture manifests the earliest set of design decisions
  - Constraints on implementation
  - Dictates organizational structure
  - Inhibits or enables quality attributes and suports WBS
- Supports reuse at architectural level
- Helps in work breakdown and structures in the development
- Changes to architecture is expensive later in the SDLC

#### Characteristics of Software Architecture
- Addresses variety of stakeholder perspectives
- Realized all of the use cases ans scenarios for the problem
- Supports separation of concerns
- Quality Driven
- Recurring Styles
- Conceptual Integrity

#### Factors that influence Software Architecture
- Functional Requirements
- Data Profile
- Audience
- Usage characteristics
- Business priority
- Regulatory and Legal Obligations
- Architectural Standards
- Dependencies and Integration
- Cost Constraints
- Initial State
- Architect and staff skill level
- Technical and Organizational environment
- Technology Constraints

### Architect
- Role within the software development organization structure, who makes high level design choices and dictates technical standards
- Architect has:
  - Distinct role in project
  - Broad Training & Extensive Experience
  - Deep Understanding of the domain

#### Views
- Represent ways of describing the Software Architecture, enabling the system to be viewed by different stakeholders in perspectives of their interest
- Ex: UI View, Process View

#### Styles
- Demos how the subsystems or elements are organized
- Way of organizing code
- Ex: Pipe & Filters, Client-Server, Peer-to-Peer

#### Pattern
- Known or proven solution to the architectural problem of structuring and functioning of the subsystems
- Ex: MVC separating UI from the rest

### Design Issues and Decisions
- Designer makes a design decision to resolve design issues faced
- Design Decision: Process involves choosing the best option among the alternatives

### Theme - Decomposition
- First step typically involves decomposition of the problem to individual modules
- Approaches:
  - Decomposition based on _Layering_
  - Decomposition based on _Distribution of resources_
  - Decomposition based on _Exposure_
  - Decomposition based on _Functionality_
  - Decomposition based on _Generality_
  - Decomposition based on _Volatility_
  - Configuration
- Keeping internals of a module together: ___Coupling___
- Different Modules working together: ___Cohesion___
- Look for __Low Coupling__ and __High Cohesion__
- Other ways of Decomposition:
  - Divide and Conquer
  - Stepwise Refinement
  - Top Down Approach
  - Bottom Up Approach
  - Information Hiding

## Architectural Views
- Module View Point/Structure of Modules
- Component and Connector Structure
- Allocation Structure
- Krutchen's View/4+1 View

### Module View Point
- Modules are units of Implementation with some functional responsibility
- Structure the system as a set of code units
- Architect enumerates what the units of software will have to do and assign each item to a module
- Larger modules may be decomposed to sub-modules
- Used as the basis for development project's organization and deliverables like documentation

### Component and Connector View Point
- Indicates a way of representing a dynamic view of the system

#### Components or Processing Element
- Software structure which converts inputs to outputs
- Series of processes
- Components are:
  - Computational
  - Manager
  - Controller

#### Data Element
- Information needed for processing or to be processed
- Data Elements include: Memory with data

#### Connecting Elements
- Glue to the components and Data Elements
- Communication and Synchronization Link
- Connecting Elements are:
  - Procedure calls
  - RPCs
  - Communication Protocols
  - Object Persistence

### Allocation View Point
- ___Deployment Structure:___
  - Shows how software is assigned to hardware elements and which communication paths are used
  - This view allows engineer to reason about performance, data integrity, availability and security
  - Important in distributed or Parallel Systems
- ___Implementation Structure:___
  - Indicates how software is mapped onto file structures in system's development, integration, or config control environments
- ___Work Assignment Structure:___
  - Shows who is doing what and helps determine what knowledge is needed where

### Krutchen's View Point
- ___Use Case View:___
  - Exposing the requirements of the system or scenarios
- ___Design View:___
  - Exposes vocabulary of the problem and solution space
  - Class Diagrams, Sequence Diagrams etc.
- ___Process View:___
  - Encompasses the dynamic aspects or runtime behaviour of the system
  - Threads and processes that form the systems
  - Addresses, performance, concurrency etc.
- ___Implementation View:___
  - Addresses the realization of the system
  - UML diagrams
- ___Deployment View:___
  - Focuses of system engineering issues

## Architectural Styles
- It is way of organization of the components in an architecture, characterized by the features that make it notable
- Toolbox having tools of architecture
- Addresses the structure and behaviour of the system and is a way of organizing modules
- ___Vocabulary:___ A set of design elements
- ___Design Rules:___ A set of constraints
- ___Semantic Interpretation:___ Well-defined meaning of the connected design elements
- ___Analysis:___ Analysis that can be performed on systems built in that style

### Main Program with Subroutine
- ___Generic:___ Traditional Langauge-Influence Style
- ___Problem:___
  - System can be described as a hierarchy of functions
  - Natural outcome of the functional decomposition of the system
  - Top level module acts as a main program and invokes the other modules in the right order
  - Single thread of control
- ___Context:___
  - Language with nested procedures
- ___Solution:___
  - _System Model:_
    - Procedures and modules are defined in a hierarchy
    - Higher level modules call lower level modules
    - Hierarchy may be strict or weak
  - _Components:_
    - Procedures which can are residing in the main program
    - Have their own local and global data
  - _Connectors:_
    - Procedure call and shared access to global data
  - _Control Structure:_
    - Single centralized thread of control
    - Main program pulls all the strings

## Architectural Pattern
- Is a proven potential solution of structuring and functioning to a recurring architectural problem
- Typically discovered
- Is a named collection of architectural decisions that
  - Has resulted in successful solution in a given development context
  - Constrain architectural design decisions that are specific to a particular system in that context
  - Brings out beneficial qualities in each resulting system
  - Good starting point solution to the problem
  - Could be looked at from the perspective of number of layers between the user and data

### Tiered Architecture
- Number of layers betwwen user and the data

#### Monolithic
- Also called as single tier architecture
- Consists of a single application layer that supports the user interface, business rules and all the manipulations in one structure

#### Two Tiered Architecture
- Business rules and user interface remain at the client side
- Data retrieval and manipulation is done by another application, present in a separate system

### Model View Controller
- ___Model:___
  - It is the central component and consists of application data, business rules, logic and functions
  - Abstraction layer for features
- ___View:___
  - View is the graphics design and layout
  - Gets information from the model as prompted by controller
- ___Controller:___
  - Accepts input and converts it into commands for the model or view
- MVC will be useful when User Interface changes more frequently than the Business Logic
- If an application needs to display the same data in different ways
- Designing visally appealing UI requires different skill set when compared to what is needed for developing complex business logic
- UI code tends to be more device dependent than the business logic
- Keeping these two independent, it will ensure migration and minimizes the risk of introducing errors into the business logic

## Design
### Design Principle
- Further decomposition of the components being developed if necessary
- Description of the behaviour of components identified as part of Architectural Design
- Description of how the interfaces will actually be realized using the appropriate algorithms and data structures
- Description on how the system will facilitate interaction with user via the User Interface
- Use of appropriate structural and behavioral design patterns
- Consideration of maintainance and reuse as couple of goals of the project

### Techniques that enable Design
- ___Abstraction:___ Focus on essential properties
- ___Modularity:___ Degree or extent to which the larger module can be decomposed
- ___Cohesion:___ Extent to which components are dependent on each other. Strong cohesion good
- ___Coupling:___ Extent to which how strongly the modules are connected to other modules. Low coupling is good
- ___Types of Coupling:___
  - Content
  - Common
  - External
  - Control
  - Stamp
  - Data
- ___Types of Cohesion:___
  - Adhoc
  - Logical
  - Temporal
  - Sequential
  - Procedural
  - Functional
- ___Information Hiding:___
  - Design involves a series of decisions and for each such decision, we need to consider who needs to know what
  - This is done through:
    - ___Encapsulation:___
      - Hides data and allows access to data only through specific functions
    - ___Separation:___
      - Information hiding strategy which involves defining a component by specifyin public interface
      - Separating the details of how the component is actually realized
- ___Limiting Complexity:___
  - Refers to the amount of effort required for building the solution
  - Can be intra-modular or inter-modular
  - Higher value => Higher Complexity => Higher Effort required => Worse design
- ___Hierarchical Structure:___
  - Views the whole structure as a hierarchy

### Key Issues
- Concurrency
- Event Handling
- Distribution of components
- Non-functional requirements
- Error, Excpetion Handling, Fault Tolerance
- Interaction and Presentation
- Data Persistence

## Design Methods
- Detailed design methods support us in decomposing the components representing the system requirement into components/subcomponents

### Data Flow Diagram
- It is a two step process
  - ___Structured Analysis:___ Resulting in logical design, drawn as a set of data flow diagrams
  - ___Structured Design:___ Transforming the logical design into a program structure drawn as a set of structure charts

#### Components in DFD
- ___External Entity:___ Source and Destination of a transaction. Depicted as __squares__
- ___Process:___ Transforms the data. Depicted as __circles__
- ___Data Stores:___ Lie between processes and are places where data structures reside. Depicted as __two parallel lines__
- ___Data Flows:___ Paths where data structures travel between processes and entities and data stores. Depicted as __arrows__

#### Minispecs
- Once the DFDs become sufficiently straight forwards, and cannot be broken down further, these are processes are described as "minispecs"

#### Data Dictionary Entries
- Contents of the DFDs after are at a logical decomposed state are recorded in a data dictionary
- Precise description of the structure of the data

#### Transform-Centred Desgin
- Trace the input through the data flow diagram until it can no longer be considered as an input

### Design Pattern
- Provides solution to a recurring problem
- Provides abstraction above the level of a single component
- Means of documentation both descriptive and prescriptive

|Pattern|What it does|
|:--:|:--:|
|Structural Decomposition Pattern|Breaks down large system into subsystems and complex components|
|Organization of work pattern|Defines how components work together|
|Access Control Pattern|Describes how access to services and components is controlled|
|Management Pattern|Defines how to handle homogeneous collections in their entirety|
|Communcation Pattern|Defines how to organize communication among components|

#### Singleton Pattern
- Ensures that only one instance of a class is created
- Provides a global point of access to the object
- Useful when only one object is needed to coordinate actions
- Involves only one class which is responisble to instantiate itself

#### Anti Pattern
- Describe situations that should be avoided
- In Agile Approach, refactoring is applied whenever an anti pattern has been introduced

## Structured and Object Oriented
- Just read the slides
- I can't be bothered with this table

## Service Oriented Architecture
- Architectural style that supports a way to make software components reusable via service interfaces
- Each service in an SOA embodies the code and data integration required to execute a complete, discrete business function
- Services are exposed using standard network protocols like HTTP or JSON/HTTP
- Design methodology basesd on structured collection, called services
- SOA originates from concept of breaking down a large problem into a series of smaller, individual problems

### Benefits of SOA
- Greater business agility
- Faster time to marker
- Ability to leverage legacy functions in new markets
- Service Reusability
- Improved collab between business and IT

### Service
- Service is a logical representation of a repeatable business activity that has a specified outcome
- Implemented as discrete pieces of software or components written in any langage capable of performing a task
- Implemented as callable entities
- Could also be application functionality with wrappers, which can communicate through messages

#### Characteristics of Services
- Adhere to service contract
- Loosely cooupled
- Stateless
- Autonomous
- Abstraction
- Reusable
- Open standards
- Facilitate interoparability
- Can be discovered
- Can be composed to form larger services

### SOA Roles
- ___Service Provider:___ Creates web services and provides them to a service registry
- ___Service Registry/Broker:___ Responisble for providing information about the service to a requester
- ___Service Requester:___ Finds a service in a service broker then will connect with the service provider to receive the service

### Architecture
- Typical architecture with two layers of services, communicating through service bus, with an orchestration layer
- There is a service bus through with the communication takes place












