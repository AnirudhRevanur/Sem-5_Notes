# Unit 1

## Applications of AI
1. AI in E-Commerce:
  - Revolutionizes retail with personalized recommendation engines
  - Chatbots offer human-like shopping experience using Natural Language Processing
  - Detecting Fraud

2. AI in Education
  - Grading, Feedback Facilitations, Enrollment Management, HR-Related tasks
  - Digitizes video lectures, conferences and guides
  - Monitoring Student's data, study habits and generating customized lesson plan, reminders, and study guides

3. AI in Automobile
  - Self-driving cars, having cameras, radars, GPS and control signals, also include emergency braking, blind spot monitoring
  - Automobile assembly, Supply Chain management
  - Reducing distractions, analyze behaviours and providing in car delivery services

4. Misc applications
  - AI powered robots use real time updates to plan journeys
  - AI-driven software for blind hiring
  - Revolutionizing healthcare by faster diagnosis, personalized treatment plans and drug discovery

## Features of Machine Learning
1. Uses the data to detect patterns in a dataset and adjust program actions accordingly
2. Focuses on the development of computer programs that can teach themselves to grow and change when exposed to new data
3. Enables computers to find hidden insights using iterative algorithms without being explicitly programmed
4. Automates analytical model building using statistical and machine learning algorithms

## Types of ML
1. __Supervised Learning:__ Algorithm is trained on a labeled dataset, where it learns to map input data to corresponding output labels. Classification and Regression
2. __Unsupervised Learning:__ Algo is given unlabeled dataset and it tries to find patterns and relationships within the data
3. __Semi-supervied Learning:__ Combines elements of both the above categories. Small labeled set and a larger unlabeled dataset
4. __Reinforcement Learning:__ Agent learns to interact with the environment to achieve a goal. Feedback in rewards or penalties and adjusts actions.

## Advantages of AI
1. __Reduction in Human Error__
2. __Takes risks instead of humans:__ Send bots with AI to Chernobyl
3. __Repetetive Tasks:__ Can redo the same stuff without complaining of beingn bored
4. __Digital Assistance:__ Setup a voice bot or chat bot that helps customers
5. __Daily Applications:__ Siri, Cortana, Alexa are used in daily routine
6. __New Inventions:__ Doctors can now predict cancer in earlier stages with help of AI

## Disadvantages of Ai
1. __High Costs of Creation:__ Hardware and software updates to meet latest requirements, causing significant expenses
2. __Unemployment:__ Replacing human taskforce with AI
3. __Lack of Creativity:__ Machines can only do what they are programmed and cannot be asked to think
4. __Lack of Emotions:__ They cannot replace the connection that humans have when they are in a team

## Four Views of Intelligence

### Thinking Humanly
- Understand how humans think and model this process
- Cognitive Science
- Creating AI systems that emulate human cognition, reasoning etc.
- Develop machines that can understand and respond to information in a manner that is similar to humans

### Acting Humanly
- Turing Test
- Knowledge, Reasoning, Language, Learning
- Perform tasks and exhibit behaviour that is indistinguishable from a human
- Emulate human-like behaviours, reasoning and decision making

### Thinking Rationally
- Rational - Thinking and doing the right thing
- Use logic to encode the right thing and process inputs with framework
- Reason logically and make decisions based on formal rules and principles
- Using well-defined algorithms and deductive reasoning to arrive at conclusions that are logically valid

### Acting Rationally
- "Maximize the goal achievement"
- Rational Agent gives the best outcome
- Most appropriate course of action based on available information and the expected outcomes rather than strictly following predefined rules, or mimicking human behaviour


## Types of AI

### Narrow AI
- AI systems designed for specific tasks or domains
- Examples include virtuall assistants, image recognition software and recommendation systems

### General AI
- Possess human-like intelligence, allowing it to understand, learn and perform any intellectual task that a human can
- Still a theoretical concept

### Super AI
- Surpasses human intelligence and capabilities with potential to outperform humans in every aspect
- Speculative concept and its development raises ethical and existential considerations

## Agent
- Agent is an independent program that interacts with environment with the help of sensors, then acting to actuators
- Agent runs in the cycle of perceiving, thinking and acting
- __Agent = Architecture(Hardware) + Software Systems__

### Intelligent Agents
- Autonomous entities that act upon an environment using sensors and actuators that achieve their goals
- May learn from the environment to achieve these goals
- ___Software:___ Agent has file contents,  keystrokes and received network packages that function sensory input, and display output on a screen
- ___Human:___ Humans have eyes, ears and other organs that act as sensors, while other organs like hands, legs and other body parts are actuators
- ___Robotic:___ Robotic Agents have cameras  and infrared range finders that act as sensors, and parts like motors and servos act as actuators

### Rational Agent
- Agent that has a clear preference and acts in a way to maximize its performance measure with all possible actions
- Performs the right things
- Rational action is most important because it receives positive rewards for good behavious and negative rewards for bad behavious
- Self driving cars, Game Playing AI, Siri/Alexa, Stock trading algorithms, Industrial robots


|Intelligent Agent|Rational Agent|
|:--:|:--:|
|System that can perceive its environment and take actions to a specific goal|Makes decisions based on logical reasoning and optimizes its behaviour to achieve a goal|
|Perceive environment through sensors|Based on information available and logical reasoning|
|Decisions basd on set of rules or pre-defined algorithm|Decisions based on logical reasoning|
|Learn from environment and changes behavior|Learns from environment, but changes behaviour based on logical reasoning|
|Operate independently of humans|Operates autonomously, but based on logical reasoning|

### Rules
1. AI Agent must be able to perceive the environment
2. Environmental observations must be used to make decisions
3. Decisions should result in an action
4. Action taken should be rational

### Structure of an AI Agent
- Structure of an Intelligent Agent is a combination of architecture and agent program
- Can be viewed as __Agent = Architecture + Agent Program__
- __Architecture:__ Machinery that AI agents executes on
- __Agent function:__ Map a percept to an action
- __Agent program:__ Implementation of agent function

### Agent Cycle
- __Perciving:__ Inputs from the environment are received by intelligent agents through sensors
- __Decision making:__ Uses AI to make decisions
- __Acting:__ Actions are triggered through actuators

### Characterizing an Intelligent Agent
- __PEAS__ is used for high-level characterization. It stands for:
  - __P__ = Performance Measure
  - __E__ = Environment
  - __A__ = Actuators
  - __S__ = Sensors
- AI Algorithms can be written more effectively by identifying PEAS

### Terminologies

#### Agent Function
- Is a map from the precept square to an action
- _Input:_ Entire percept history
- _Output:_ Provides behaviour of agent

#### Agent Program
- Implementation of an agent function
- _Input:_ Current Precept Only
- _Output:_ Returns Action to the Actuators

#### State
- Configuration of an agent and its environment
- Enables the agent to remember past experiences, reason about the current situation and plan for future

#### Initial State
- Starting Point of agent's interaction with the environment
- Represents the agent's knowledge, beliefs and information about the environment at the beginning of a task or problem solving process

#### Actions
- Represents different choices or moves that an agent can make
- Essential for the agent to adapt and respond appropriately to changes in the environment and work towards its goals effectively


## Environments

### Observability
#### Full Observable
- If an agent's sensors give it access to the complete state of the environment, the environment is observable
- State of the system can be determined at all times
#### Partially Observable
- Entire state is not fully visible to the sensor
- Observer may utilize a memory system in order to add information to the observer's understanding of the system

### Determinism
#### Deterministic
- If an agent's current state and selected action can completely determine the next state of the environment, then it is deterministic
#### Stochastic
- Stochastic environment is random in nature, partially observable and cannot be determined completely by an agent

### Episodicity
#### Episodic
- Agent's experience is divided into atomic episodes
- In each episode, the AI Agent observes and performs one action, and the choice is solely based on that specific episode, independent of the previous actions
#### Sequential
- Environment where next state is dependent on the current action
- Current decision affects all future decision

### Dynamism
#### Static Environment
- Idle environment with no change in its state is called static environment
- Does not change from one state to the next when agent is considering its course of action
- Agent need not keep looking at the world when it is deciding, nor the passage of time
#### Dynamic Environment
- Environment can change while an agent is thinking

### Continuity
#### Discrete Environment
- Consists of finite number of actions that can be deliberated in the environment to obtain output
#### Continuous Environment
- Actions performed cannot be numbered

## Traditional Modelling vs  Machine Learning

|Traditional Modelling|Machine Learning|
|:--:|:--:|
|Take data and rules as input and apply the rules to the data, to come up with answers as output|In machine learning, the computer finds patterns and rules and creates a model. This model is output|

- ___Machine Learning:___  It is the study of algorithms that
  - Improve their performance "P"
  - at some task "T"
  - with experience "E"(Training data)

- __7 steps in Machine Learning:__
  1. Data Collection
  2. Data Preparation
  3. Choosing a model
  4. Training
  5. Evaluation
  6. Parameter Tuning
  7. Prediction

### Supervised Learning









