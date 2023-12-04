# Unit 1

- __Software:__ Collection of execuatble computer programs, their configuration files and associated libraries and documentations serving a computational purpose
- __Software Product:__ Software made for a specific or specific group of requirements
- __Engineering:__ Acquiring and using well defined scientific principles and systematic methodsfor developing products with practical considerations
- __Software Engineering:__ Systematic, disciplined, quantifiable approach towards the development, operation and maintainance of software products
- __Software Engineering Principle:__ Drives usage of appropriate tools and techniques depending on the problem to be solved, whileconsidering the constraints and resources available

|Software Engineering|Computer Science|
|:--:|:--:|
|- Software Architecture|- Algorithms|
|- Project Management|- Theories of computation|
|- Technical Planning|- Compilers|
|- Risk Management|- Operating Systems|
|- Software Assurance|- Artifical Intelligence|


## Fundamental Drivers of SE
### Industrial Strength Software
- Needs to be operational
- Capable of being moved
- Needs to be maintainable
- Should have elaborate documentation
- Absence or minimal number of bugs
- Impactful to the business

### Software is Expensive
- Software labor is expensive
- Each line of code can cost between $5 and $35
- Maintainance and rework costs money

### Can influence life or death
- Radiation Therapy
- One bug causeds over exposure of radiation, causing the death of 6 people

### Heterogeneity
- Systems should work as distributed systems

### Diversity
- Different types of software systems

### Business and Social Changes
- Ability to change existing software and develop a new software
- Organizations are becoming global

### Security and Trust
- Trust the software

### Scale
- Scale easily with size

### Quality and Productivity
- Quality as FLURPS + Protability + Efficiency/Maintainability

## Summary of Why SE is required
- Development of big programs
- Mastering complexity of big programs
- Ensuring software process supports users effectively & Right choices and decisions are made
- Ensuring visibility and continuity
- Supporting large teams and team work
- Efficient development of evolving software

## SDLC
- Software Development Life Cycle
1. Requirement Analysis
  - Feasibility Study
  - Requirements
2. Design
  - Architecture
  - Design
3. Implementation
4. Testing
5. Maintainance
(Loop it back)

## PDLC

---------------------- Add later ----------------------

1. Intorduction
2. Growth
3. Maturity
4. Discontinuance
5. Obsoloscence

- The first three are increasing sales/revenues, while the last two are decline phase
- Investment will be high in the first two phases, then slowly decline at maturity, then has a sharp decline to discontinuance and obsoloscence

## Legacy SDLCs

### Waterfall Model
1. Requirement Analysis
2. Architecture
3. Detailed Design
4. Implementation
5. Testing
6. Deployment
7. Maintainance

- All these steps come one after the other. There is no overlap in any step

|Advantages|Disadvantages|
|:--:|:--:|
|Simple|Assumes requirements are frozen|
|Clear identified phases|Difficult to change and is sequential|
|Easy to manage, because rigid|Poor model for long projects|
|Each phase has specific deliverables|Big Bang Approach|
|Easy to departmentalize|High Risk|

- __Usage:__
  - Pure form: Short projects where requirements are well known
  - Product definition is stable and technology is understood
  - Variant from: High level in long projects. Used in large developed projects along with other lifecycle models

### V Model
#### Verification Phase
- This is the Developer's Life Cycle
1. Business Requirements
2. System Requirements Specification
3. High Level Design
4. Low Level Design
5. Coding/Unit Testing
#### Validation Phase
- This is the Tester's Life Cycle
1. Unit Testing
2. Component Testing
3. System Integration Testing
4. Ssytem Testing
5. Acceptance Testing

|Advantages|Disadvantages|
|:--:|:--:|
|Test development activities happen before coding and formal testing lifecycle|Software is developed during implementation, so no early prototypes are available|
|Higher probability of success + Increased effectiveness of usage of resources|Change through the process, necessitates changes in test document too|

### Prototype Model
- Prototypes is a relatively cheap process
- Instead of freezing the requirements before a design or coding can proceed, complete system prototype is built to understand the requirements
- __Types:__ Throw-away and evolutionary prototypes

|Advantages|Disadvantages|
|:--:|:--:|
|Active involvement of users|May increase the complexity of system as scope of system may expand beyond original plans|
|Risk mitigation, Reduced time and cost, resulting system is full featured, more stable system|Performance of resulting system may not be optimal|

- __Usage:__ 
  - When requirements are not clear
  - Users are actively involved

### Incremental Model
- Requirements are partitioned
- Working version of software is produced during the first module, so we have a working software early
- Each subsequent release adds functionality to the previous module
- Continuous integration is donw until entire system is achieved

|Advantages|Disadvantages|
|:--:|:--:|
|Customer value and more flexible|Needs good planning and design|
|Easier to test and debug|Needs clear and complete definition of full system|
|Easier to manage risk|More expensive than waterfall|
|Continuous increments than monolithic|Hard to identify common functionalitoes across increments|
|Reduces over functionality|Management visibility is reduced|

- __Usage:__
  - Major requirements are defined
  - Product needs to get to market early
  - New tech is used
  - Resources with required skillset are unavilable
  - High risk features and goals

  
### Iterative Model
- Initial implementation starts from skeleton of product
- This is followed by refinement through user feedback and evolution
- Built with dummy modules
- Rapid prototyping
- Successive refinement

|Advantages|Disadvantages|
|:--:|:--:|
|Help identify requirement and solution visualisation|Each phase is rigid with overlaps|
|Support risk mitigation, rework is reduced, incremental investment, increased customer engagement|Costly system architecture may arise|

- __Usage:__ Large projects which may get extended

|Iterative|Incremental|
|:--:|:--:|
|Revisit and refine everything|No need to go back and change delivered things|
|Focus on details|Focus on things that are not implemented yet|
|Leverage on learnings|Does not leverage on experience or knowledge|

### Limitations of Legacy Models
- Predictive software development needs
- Upfront planning
- Don't facilitate periodic customer interactions
- Suited for very large complex projects
- Regulatory Perspectives
- Global or distributed organizations
- Product life cycle and ecosystem
- People and skill
- Suitable projects with clear definition
- Suitable when things are not changing fast

## Agile
- Agile is an umbrella term to describe many methods
- Encourage:
  - Continual realignment of development goals with needs and expectations of the customer
  - Reducing massive planning overhead to allow fast reactions to change
- __Agile is not a process, it is a set of values and philosophy__
- Agile is:
  - Rapid
  - Adaptable
  - Quality Driven
  - Iterative
  - Cooperative

### Agile Manifesto
- Individuals and interactions over Processes and tools
- Working software is valued more than documentation
- Customer collaboration is more than contract negotiation
- Responding to change is more than Following a plan
- Focus on simplicity in both product and process

|Pros|Cons|
|:--:|:--:|
|Realistic approach to software development|Not suitable for handling complex dependencies|
|Teamwork and cross training|Risk of sustainability, maintainability and extensibility|
|Functionality can be developed rapidly and demoed|Overall plan, agile leader, agile PM practices are a must|
|Resource requirements are minimum|Strict delivery management dictates the scope, functionality to be delivered, and adjustment to meet deadlines|
|Good for environments that change|Depends heavily on customer interaction|
|Minimal rules and docs|Individual dependency since there is minimum docs|

### Scrum
- Methodology or framework for developing, delivering and sustaining software components and products
- Iterative apporach towards software development
- Provides mechanisms to apply agile practices
- Scrum is defined by:
  - Roles
  - Events
  - Artifacts
  - Rules

#### Scrum Teams
- Cross functional and self organizing
- Consists of contributors to deliverable
- Responsible for delivering shippable increments

#### Scrum Master
- Is a facilitator
- Removes impediments and facilitates meetings
- Ensures team sticks to scrum theory and practices

#### Product Owner
- Voice of stakeholder/team
- Creates or manages product backlog

### Product Backlog
- Product Backlog includes:
  - New features
  - Changes to existing geatures
  - Bug fixes
  - Infrastructure setupes
- Product Backlog is broken down into user stories
- Then they are weighted and ranked, which results in the Roadmap
- Stories are ranked by importance by estimating the amount of work needed to be done by the Scrum Team

### Scrum Events
- __Sprint:__
  - Short fixed iterations (usually 2-4 weeks)
  - Potentially shippable code demonstrated after each iteration
- Total effort each iteration can accomodate leads to the number of user story per iteration
- One release may contain multiple iterations
- __Sprint Planning Meeting:__
  - Used to determine which of the product backlog items will be worked on and delivered in the next iteration
- __Daily Scrum Meeting:__
  - Also called as stand up meetings
  - Usually go on for 15 minutes
  - The things discussed:
    - What did you do yesterday?
    - What will you do today?
    - Are there any obstacles?
- __Pre Planning Meeting:__
  - Enables the businnes and stakeholders to focus on prioritization and preparation of requirements far in advance before the sprint planning session
  - Every sprint will need to have one prioritized list of requirements so there can be a focus on and deliver the most valuable and needed requirements in a short time
  - Product Owner needs to talk and align requirements of multiple stakeholders which is not easy as every stakeholder has their own priorities that influence the plan of other stakeholders
  - There can be one or couple of these Pre Planning Sessions
  - __Outcomes:__
    - Scope for the next sprint agreed
    - The readiness of the requirements is indicated to the product owner
    - Reough estimation in story-points
- __Sprint Planning:__
  - Event that kicks starts the sprint
  - Agenda: Defines the scope of delivery and how to accomplish that work
  - Sets a common goal for the team during the sprint
  - __Scrum Master:__
    - Facilitate the Sprint planning meeting
    - Ensures agreement on the sprint goal and the product backlog items
  - __Inputs:__
    - Product backlog
    - Sprint team capacity
    - Past performance of Dev team
- __Sprint Review:__
  - Used to demo story features
  - Product owner does the following:
    - Evaluates against preset criteria
    - Feedback from clients and stakeholders
    - Ensures the delivered increment meets the business need
    - Helps support reprioritizing of the backlog
    - Optimize the release plan if needed

## Extreme Agile Programming (XP)
- Dev team estimates, plans and delivers the highest priority user stories in the form of working & tested software

|Scrum|XP|
|:--:|:--:|
|Framework for management of project|Specifies engineering practices like pair programming|
||Requirement change granularity is once|Requirement change granularity is anytime|
|Features not developed in strict order|Features developed in strict order|

## Lean Agile
|Agile|Lean|
|- Small batches|- Elimintaing Waste|
|- Iterative and continuous course correction and delivering components|- Continuous inspectino to adapt and improve|
|- Focused on course corrections during development|- Looks to boost performance|
|- Focus is develop a product which addresses the customer needs and expectations|Focus to provide a product which addresses the customer needs and expectations in the most efficient fashion|

### Lean Principles
- Eliminate waste
- Amplify learning using active feedback
- Decide as late as possible
- Deliver as fast as possible
- Empower the team to follow a controlled low overhead plan
- Build integrity in as processes
- Consider the whole system

## CBSE
- Component Based Software Engineering is a reuse approach
- Select components from the shelf and integrate it into your project
- __Advantages:__
  - Black box usage of components
  - Reduced development time
  - Increases quality
  - Increases productivity
- __Disadvantages:__
  - Trusting components
  - Component certification
  - Emergent property prediction
  - Requirement trade off

### Essentials of CBSE
- Independent components that are completely specified by the public interfaces
- Component standards that facilitate the integration of components
- Middleware that provides support for component integration
- Development process that is geared up to CBSE

### Software Component
- Independent executable entity that can be made up of one or more executable objects
- It has explicit dependencies through "required" interfaces and "provides" interfaces
- It implements a functionality without regard to where the component is executing or its programming language
- ___Identifying the Component:___
  1. Search for component
  2. Select Component
  3. Compose component from existing ones
  4. Adadpters or "glue" is used to reconcile different component interfaces
  5. Validate the output
- ___Development Stages:___
  1. Development = UML
  2. Packaging = .zip
  3. Distribution
  4. Deployment
  5. Execution = Blocks of Code and Data
### Component Model:
- Defines the type of building blocks that can be composed with other components to make a software system
- __Interfaces:__ Defines how component can interact and also defines operation names, parameters and exceptions
- __Usage:__ In order for components to be distributed and accessed remotely, they need to have a globaly unique name or handle associated with them
- __Deployment:__ Specification of how components should be packaged for deplyment as independent, executable entitites

### Software Product Lines:
- A product line defines a family of manufactured products
- Product line architecture explicitly captures the commonality and  variability of a product line components and their compositions
- Software Product Lines refers to engineering techniques for creating a portfolio of similar software systems from a shared set of software assets
- Makes it possible to
  - Create software for different products
  - Use variability to customize software to each different product
- ___Key Drivers:___  
  - Software porduct lines enhance reuse through predictive software reuse
  - Software artifacts are created when reuse is predicted in one or more products in a well defined product line
  - Artifacts could be built as components which are reusable or could be looked at as patterns which could be built using some fine grained components for a particular solution

### Product Line Engineering Framework
- ___Domain Engineering:___ Define and realize the commonality and variability. Goal is to establish a reusable platform
- ___Application Engineering:___ Reuse domain artifacts


## Requirement Engineering
- Requirement is the property which must be exhibited by the software developed/adapted to solve a particular problem
- Requirement should specify the externally visible behaviour of what and not how
- First step in any software intensive development lifecycle irrespective of the SDLC
  - Difficult, Error Prone and Costly
  - Critical for successful development of all down stream activities
  - Requirement Errors are expensive to fix

### Requirement
- It is a property which must be exhibited by software developed/adapted to solve a particular problem
- Should specify the externally visible behaviour of __what__
- Can be:
  - Individual requirements
  - Set of requirements

#### Individual Requirements
- __Concise:__ Requirements should describe a single property
- __Unambiguous:__ Should have only one interpretation
- __Verifiable:__ Requirements must have a clear, testable criterion and cost effective process to check it
- __Quantifiable:__ Requirement should be quantifiable
- __Traceable:__ Backward sto stakeholder request and forward to software to components
- __Clear:__ Written Preciselu
- __Consistent:__ No requirements should contradict each other
- __Feasible:__ Realizable with a specified time frame
- __Prioritized:__ Requirements should be prioritized

#### Set of Requirements
- Realistic
- Complete
- Ranked for Importance or Stability
- Modifiable
- Correct

### Feasibility Study
- Short, low-cost study to assess the praticality of the project and whether or not it should be done
- It is done before the beginning of a project

#### Activities in a Feasibility Study
- Find the client that will have a stake in this project
- Find current solution to the problem
- Targeted customers and the future marketplace
- Potential Benefits
- Scope
- High level understanding of the solution
- Considerations to technology
- Marketing Strategy
- Financial Projection
- Schedule and high level planning and budget requirements
- Issues, assumptions, risks and constraints
- Alternatives and their consideration
- Potential Project Organization
- ___Ends with GO or NO-GO___

#### Requirements Engineering Process
It is a "four+one" set of activities to produce specifications or requirements 
1. __Requirements Elicitation:__ To gather and discover requirements
2. __Requirements Analysis:__ Process of reviewing requirements
3. __Requirements Specifications:__ Process of creating software and system specification documents suitable for further designing and maintainance
4. __Requirements Validation:__ Helps ensure the right requirements are realized

## Requirement Elicitation
- Process of working proactively with all stakeholders gathering their needs, articulating their problem, identify and negotiate potential conflicts thereby establishing a clear scope and boundary for a project
- Involves:
  - Understanding the problem
  - Understanding the domain
  - Identifying clear objectives
  - Understanding needs
  - Understanding constraints of systme
  - Writing business objectives for the project

#### Active Techniques
- Ongoing interaction between stakeholder and user
1. Interviews
2. Facilitated meetings
3. Roleplaying
4. Prototypes
5. Ethnography
6. Scenarios

#### Passive
- Infrequent interaction between the stakeholders and users
1. Use cases
2. Business process analysis & modelling
3. Workflows
4. Questionnaires
5. Checklists
6. Documentation
