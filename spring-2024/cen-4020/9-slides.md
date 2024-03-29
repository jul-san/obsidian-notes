## Application Architectures
- Applications systems are designed to meet an organizational need.
- As businesses have much in common, their application systems also tend to have a common architecture tht reflects the application requirements
- Geneeric application

## Use of Application Architectures
- As a *starting point* for architectural design.
- As a design *checklist*
- As a way of *organizing the work* of the development team.
- As a means of *assessing components* for reuse.
- As a *vocabulary* for talking about application types.

## Examples of Application Types
- Data processing applications
    - Data driven apps that process data in bathes wihout explicit user intervention during the processing.
- Transaction processing application
    - Data-centered applications that process user requests and update information in a system database.
- Event Processing Systems
    - Apps where system actions depend on interpreting events from the systems environment.
- Language processing systems
    - Apps where the users' intentions are specified in a formal language that is processed and interpreted by the system.

## Application Type Examples
- Two very widely used generic app architectures are transaction processing systems and language processing systems.
- Transaction Processing Systems:
    - E-commerce systems
    - Reservation systems
- Language Processing Systems
    - Compilers
    - Commadn line interpreters

## Transaction Processing System
- Process user requests for information from a database or requests to update the database.
- From a user perspective a transaction is:
    - Any coherent sequence of operations that satisfies a goal
    - e.g. -find the times of flights from TLH to SEA
- Users make asychronous requests for service which are then processed by a transaction manager

## Structure of Transaction Processing Applications
![visual](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fimage1.slideserve.com%2F2403136%2Ffigure-6-14-the-structure-of-transaction-processing-applications-l.jpg&f=1&nofb=1&ipt=fc35e50ccd05fd4576b0f8f15052ef1106e65985224612d63ed4379623c65ded&ipo=images)

## Information Systems Architecture
- Information systems have a generic architecture that can be organized as a layered architecture.
- Transaction-bases systems as interaction with these systems generally involves databse transactions.
- Layers include:
    - User interface.
    - User communications.
    - Information retrieval.
    - System database.

## Web-based Information Systems
- Information and resource management systems are now usually web-based systems.
    - Where the user interfaces are implemented using a web browser.
- For example, e-commerce systems are internet-based resource management systems
    - They accept electronic orders for goods or services and then arrange delivery of these good or services to the customer.
- A 'shopping car' functionality
    - In the application-specific layer, to support the placement of iterms in separate transaction, then payment for them all together in a single transaction.

## Server Implementation
- These systems are often implemented as multi-tier client server/architectres
    - Web server is responsible for all user communications, with the user interface implemented using a web browser.
    - The application server is responsible for implementing application-specific logis as well as information storage and retrieval requests.
    - The database server moves information to and from the database and handles transaction management.

## Language Processing Systems
- Accept a natural or artifical language as imput and generate some other representation of that lanaguage.
- May include an interpreter to act on the instructions in the language that is being processed.
- Used in situations where the easiest way to solve a problem is to describe an algorithm or describe the system data.
    - Meta-case tools and process tool descriptions, method rules, etc and generate tools.

## Architecture of a Language Processing System
![Model](https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fcsis.pace.edu%2F~marchese%2FSE616_New%2FL6%2FL6_files%2Fimage026.png&f=1&nofb=1&ipt=0a4b85addd65b41348c5c13bd75d0a8a2837d94294d5879a95b8c929f4132f18&ipo=images)

