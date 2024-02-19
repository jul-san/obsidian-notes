## Architectural Design
- Concerned with:
    - Understanding how a software system should be organized and designing the overall structure of that system
- Is the critical link between design and requirements engineering:
    - Identifies the main structural components in a systema and the relationships between them
- Output of the architectural process
    - An architectural model that describes how the system is organized as a set of communicating components

## Architectural Abstraction
- Architecture in the small:
    - The architecture of the individual programs
    - Concerned with the way that an individual program is decomposed into components
- Architecture in large:
    - The architecture of a complex enterprise system the include other systems, programs, and program components
    - Enterprise systems may be distributed over different computers, which may be owned and managed by different companies


## Advantages of Explicit Architecture
- Stakeholder Communication:
    - Architecture may be used as a focus of discussion by system stakeholders
- System Analysis:
    - Means that the analysis of whether the system can meet its non-functional requirements is possible
- Documenting an architecture that has been designed:
    - A complete system model that shows different components in a system, interfaces and their connections
- Large-scale Resuse:
    - Systems in the same domain often have similar architectures
    - Systems may be architected around one or more architectural patters

## Architectural Representations
- Informal block diagrams:
    - Shows entities and relationships
    - Most frequently used method
- Have been criticized because:
    - Lacks semantics
    - Does not show the types of relationships between entities nor the visible properties of entities in the architecture
- Depends of the use of architectural models
    - Requirements for the model semantics depend on how the models are used
- Useful for communication with stakeholders and project planning

## Architectural Design Decisions
![Diagram](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fimage.slidesharecdn.com%2Fch6architecturaldesign-150102101849-conversion-gate02%2F95%2Fch6-architectural-design-13-638.jpg%3Fcb%3D1420194054&f=1&nofb=1&ipt=f08a2cdfd38621ca0395b04d5a208d010204e26c813831b9beeaedb35beacb8a&ipo=images)

## Architecture and System Charcteristics
- Performance
    - Localize critical operations and minimize communications.
    - Use large rather than fine-grain components.
- Security
    - Use a layered architecture with critical assets in the inner layers.
- Safety
    - Localize safety-critical features in a small number of sub-systems.
- Availability
    - Include redundant components and mechanisms for fault tolerance.
- Maintainability
    - Use fine-grain, replaceable components

## Architectural Views
- Views or perspectives are useful when designing and documenting a system's architecture.
    - Notations should be used.
- Each model only shows one view or perspective of the system.
    - Might show how a system id decomposed into modules.
    - How the run-time processes interact.
    - For both design and documentation, you usually need to present multiple views of the architecture

![Diagram](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e6/4%2B1_Architectural_View_Model.svg/1200px-4%2B1_Architectural_View_Model.svg.png)
