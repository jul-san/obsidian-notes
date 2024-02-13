## Requirements Engineering (Recap)
**- Process of establishing the services that a customer requires from a system and the constraints under which it operates and is developed**

## Functional Vs. Non-functional

### Functional 
- Method *m* always terminates
- If the input is positive number, the program returns its inverse
- Variable *x* always stores the value 0
- This input runs into a race condition
- The program crashes with input 3

### Non-functional
- There are no loops in method *m*
- The code is indented using tabs
- There are 3 lines of comments for every executable line
- Each class has at least 3 subclasses
- This class only has integer attributes

## Requirements Elicitation
- Software engineers work with a range of system stakeholders:
    - To find out about the application domain
    - The services that the system should provide
    - The required system performance
    - Hardware constraints
    - Other systems, etc.
- Stages Include:
    - Discovery
    - Classification and organization
    - Prioritization and negotiation
    - Specification

## Problems of Requirement Elicitation
- Stakeholder don't know what they really want
- Stakeholders express requirements in their own terms
- Different stakeholders may have conflicting requirements
- Organizational and political factors may influence the system requirements
- Requirements change during the analysis process
- New stakeholders may emerge and the business environment may change

## Requirements Elicitation and Analysis Process
![Process](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse1.mm.bing.net%2Fth%3Fid%3DOIP.1T9uxuBE5O9rZA_vgYRgEAHaEp%26pid%3DApi&f=1&ipt=8f3e86d30fe687fc99b14e6ad791b1834c6dca960f9c575ccf8c7cc39e86501b&ipo=images)

### Requirements Discovery
- Interacting with stakeholders to discover their requirements
- Domain requirements are also discovered at this stage

### Requirements Classification and Organization
- Groups related requirements and organizes them into coherent clusters

### Requirements Prioritization and Negotiation
- Prioritizing requirements and resolving requirements conflicts

### Requirements Specification
- Requirements are documented and input into the next round of the spiral

## Requirements Discovery: Interviewing
- Formal or informal interviews with stakeholders are part of most RE prcoesses
- Types of interviews:
    - Closed interviews based on pre-determined list of questions
    - Open interviews where various issues are explored with stakeholders
- Effective interviewing:
    - Be open-minded, avoid pre-conceived ideas about the requirements and are willing to listen to stakeholders
    - Prompt the interviewee to get a discussion going by using:
        - A springboard question
        - A requirements proposal
        - Working together to prototype of system

## Interviews In Practice
- Normally a mixed of closed and open-ended interviewing
- Interviews are good for getting an overall understanding of what stakeholders do and how they might interact with the system
- Interviewers need to be open-minded without pre-conceived ideas of what the system should do
- Need to prompt the use to talk about the system by suggesting requirements rather than simply asking them what they want

## Problems with Interviews
- Specialists may use language that may not be easy for an engineer to understand
- Interviews are not good for understanding domain requirements:
    - Requirements engineers cannot understand specific domain technology
    - Some domain knowledge is so familiar that people find it hard to articulate or think that it isn't worth articulating

## Requirements Discovery: Ethnography
- Social scientist spends a considerable time observing and analyzing how people actually work
- People do not have to explain or articulate their work
- Social and organization factors of importance may be observed
- Ethnographic studies have shown that work is usually richer and more complex than suggested by simple sytem models

## Ethnography and Prototyping for Requirements Analysis
![Graph](https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fcsis.pace.edu%2F~marchese%2FSE616_New%2FL4%2FL4_files%2Fimage024.png&f=1&nofb=1&ipt=e94cc5cbfe983ff0a3bdf1a9b02649857a4fedc0c708e402f1b7f3209a0d35c0&ipo=images)

## Requirements Discovery: Stories and Scenario
- Scenario and User Stories:
    - Real-life examples of how a system can be used
    - Description of how a system may be used for a particular task
    - Stakeholders can relate to them and can comment on their situation
- Scenarios:
    - A structured form of user story
- Scenarios should include:
    - Description of starting situation
    - Description of normal flow of events
    - Description of what can go wrong
    - Information about other concurrent activities
    - Description of the state when the scenario finishes

## Requirements Specification
- Process of writing down the user and the system requirements in a requirements document
- User requirements have to be understandable by end-user and customers who do not have a technical background
- System requirements are more detailed requirements and may include more technical information
- Requirements may be part of a contract for system development
    - It is important that these are complete as possible

## Writing Specification
|Notation   |Description    |
|Natural Language| <ul><li>Requirements are written using numbered sentences in natural language</li><li>Each sentence should express one requirement</li></ul> |
|Structured Natural Language| <ul><li>Requirements are written in natural language on a standard form or template</li><li>Each field provides information about an aspect of the requirement</li></ul>|
|Design Description Language| <ul><li>Uses lanaguage like a programming language, but with more abstract features</li><li>Rarely used, although it can be useful for interface specifications</li></ul>|
