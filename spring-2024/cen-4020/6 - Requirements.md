## Requirements Engineering
- Process of establishing services that the customer requires from a system
- Also establish the restraints of the system

## What is a Requirement?
- Descriptions of system services and constraints that are generated during the engineering process
- Can range from a high-level abstraction to a mathematical function specification
- Requirements may serve dual functions:
    - May be the basis for a bid contract; open to interpretation
    - May be the basis for a contract itself; defined in detail
    - Both of these may be requirements

## Types of Requirements
- User Requirements:
    - Statements in natural language
    - Diagrams of the service 
    - Written for customers
- System Requirements:
    - Structured document setting out detailed instructions of:
        - System functions
        - Services
        - Operational constraints
    - Defines what should be implemented
        - May be part of the contract between client and contractor

## Reader of Different Types of Requirements Specifications
![User and System Requirements](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse3.mm.bing.net%2Fth%3Fid%3DOIP.yIZqC10uq1JHxvn625hlrgHaEH%26pid%3DApi&f=1&ipt=9f2896e5bd2cb91719857b9f3a32f2a66f4b545d9d44ca5f6ef64ce4503e83f9&ipo=images)

## Stakeholders In the Mentcare System
- Patients
    - Whose information is recorded in the system
- Doctors
    - Responsible for assessing and treating patients
- Nurses
    - Coordinate the consultations with doctors and administer some treatments
- Medical Receptionists
    - Manage patients' appointments
- IT Staff
    - Responsible for installing and maintaining the system
- Medical Ethics Manager
    - Must ensure that the system meets currents ethical guidelines for patient care
- Health Care Managers
    - Obtain management information from the system
- Medical Records Staff
    - Responsible for ensuring that system information can be maintained and preserved
    - Make sure that record keeping procedures have been properly implemented

## Functional and Non-functional Requirements
- Functional Statements
    - Statements of service the system should provide
    - May state what the system should not do
- Non-function requirements
    - Constraints on the services or functions offered by the system
    - Often applies to the system as a whole
- Domain Requirements
    - Contraints on the system from the operation of the domain

## Functional Requirements
- Describe functionality or systerm services
- Depends on the system software, expected users, and the type of system where the software is used
- Functional user requirements may be high-level statements of what the system should do
- Requirements should describe the system services in detail

### Mentcare System: Functional Requirements
- User shall be able to search the appointments, lists for all clinics
- System shall generate each day, for each clinic, a list of patients who are expected to attend appointments that day
- Each staff member using the system shall be uniquely identified by his or her 8-digit employee number

### Requirements Imprecision
- Problems arise when functional requirements are not precisely stated
- Ambiguous requirements may be interpreted in different ways by developers and users
- Consider the term _search_ in requirement 1
    - User Intention - seach for a patient name across all appointments in all clinics
    - Developer Interpretation - search for a patient name in an individual clinic. User chooses clinic then search.

### Requirements Completeness and Consistency
- Requirements should be both complete and consistent
- Complete:
    - Should include descriptions of all facilities required
- Consistent:
    - Should be no conflicts or contradictions in the descriptions of system facilities
- Because of system and envrionmental complexity, it's impossible to produce a complete and consistent requirements document

## Non-functional Requirements
- Define system properties and constraints:
    - Reliability
    - Response time
    - Storage requirements

## Types of Non-functional Requirements
![Non-functional Requirements UML](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fcs.ccsu.edu%2F~stan%2Fclasses%2FCS410%2Fnotes16%2Fimages%2F04-nonfunctional_requirement_types.png&f=1&nofb=1&ipt=7adfccf723c5997a8fe397d63a151da6f34f6296c76b83e701a3e329f35a66d4&ipo=images)

## Non-functional Requirements Implementation
- May affect overall architecture of a system rather than individual components
- Single non-functional requirements may generate a number of related functional requirements that define system services

## Non-functional Classifications
- Product Requirements
    - Specifies that the delivered product must behave in a particular way
- Organizational Requirements
    - A consequence of organizational policies and procedures
- External Requirements
    - Arise from factors which are external to the system and its development process

### Goals and Requirements
- Requirements may be very difficult to state precisely and difficult to verify
- Goal:
    - General intention of the user such as ease of use
- Verifiable non-functional requirement:
    - Statement using some measure that can be objectively tested
- Goals are helpful since they convey the intention of the system

### Metrics for Specifying Nonfunctional Requirements
| Property | Measure |
|----------|---------|
|Speed      |<ul><li>Processed transactions/second</li>
                    <li>User/event response time</li>
                    <li>Screen refresh time</li></ul>|
|Size       | <ul><li>Mbytes</li>
                <li>Number of ROM chips</li><ul> |
