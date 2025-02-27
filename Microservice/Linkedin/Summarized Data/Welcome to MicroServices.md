Link: https://www.linkedin.com/learning/microservices-foundations-23469069?contextUrn=urn%3Ali%3AlyndaLearningPath%3A645bcd56498e6459e79b3c71&u=0
Name: WelCome of Microserices:
History of service-based architectures
**Key Concepts:**
- **Architecture Evolution**: From monolithic applications to microservices
- **Monolithic Applications**: Tightly coupled components, long development cycles
- **Service-Oriented Architecture (SOA)**: Smaller modules but issues with SOAP technology and aggregation layer
- **Microservices Architecture**: Agile framework for cloud native applications, HTTP at heart when using REST.

**Monolithic Applications:**
- Norm in the past
- Single binary web artifact with internal layers (data access, process, presentation)
- Layered architecture causes complex pass through layers
- Separation of concerns but tight coupling issues
- Long development cycles and difficult changes

**Service-Oriented Architecture (SOA):**
- Decomposition into smaller modules brought issues
- SOAP technology compromises HTTP design principles
- Aggregation layer adds new level of coupling

**Microservices:**
- Agile framework for cloud native applications
- Based on HTTP and REST, fits well with web developers
- Trade-offs in implementation.

The monolithic application
**Monolithic Applications: Internal Issues and Impact on Delivery**

**Monolithic Applications**:
- Large single file deployments (e.g., Java packages) containing both related and unrelated components
- Deployment issues: internal data access, business processes, web applications, web services, remote procedure calls packaged into one large artifact
- Code issues: developers are lazy and often use objects outside their use case without writing a lot of code, leading to tightly coupled and fragile code

**Impact on Delivery**:
- Changes in highly coupled components can break unexpectedly downstream, requiring testing of the entire deployment as part of the release
- Long deployment times (days) and production validation
- Difficulty scaling out a monolithic application, as it requires deploying the entire package even for small changes
- High infrastructure costs compared to microservices

Service-oriented architecture
**Key Concepts:**
- Spent significant time on SOAP services, writing and consuming them
- No inherent issues with SOAP as a communication mechanism
- XML provides validation benefits that are often overlooked
- Criticism towards how SOAP was implemented
- Strong contracts provided by WSDL, essential for business processing
- Inadequate response codes in SOAP leading to lack of flow control
- Promise of SOA offered amazing potential but faced issues with scaling and complexity.

**SOAP:**
- Significant part of professional career
- Communication mechanism between systems, not inherently bad
- Criticisms come from implementation issues

**XML:**
- No issue with verbosity as it adds validation value

**WSDL:**
- Single best part of SOAP
- Provides strong contract and documentation layer

**SOAP Envelope:**
- Wasted space on the wire, could have been handled more efficiently

**Criticisms:**
- Limited response codes leading to lack of granularity in flow control
- Promise of SOA offered amazing potential but faced issues with scaling and complexity

**Implications:**
- Deployment issues and monolith limitations led to the decline of SOA's popularity.

Microservices: The new kid on the block
**Microservices-Based Architectures: A Deeper Look**

**Introduction:**
- Microservices are a new trend in software development, but they build upon concepts from SOA and other service-based architecture patterns.
- No silver bullet solution exists for all problems; this course discusses microservices' core principles.

**Microservices Overview:**
- Decomposing systems into smaller units of work
- Building services according to use cases
- Embracing protocol awareness and heterogeneous interoperability, usually through REST communication
- Flexibility in calling any service within the system

**Popularity of Microservices:**
- Gained popularity due to affordability and ease of implementation compared to SOA.
- Open-source software and commodity hardware can be used for execution and proxy environments.

**Benefits of Microservices:**
- Agility in solving problems at a component level
- Scalability and flexibility due to the ability to call any service within the system

**Microservices vs. SOA:**
- Microservices provide more flexibility than traditional enterprise software architectures, such as SOA.
- Lower costs for implementation and execution with open-source software and commodity hardware.

Microservices: Solver of problems but not the silver bullet
**Costs of Moving to Microservices Architecture**

**Complexity**:
- More deployed artifacts compared to monolithic system
- Increased complexity in managing and deploying multiple components
- Deployment process may need updates if complicated

**Deployment Complexity**:
- Difficulty determining where code lives and operates
- Increase in overall deployment costs

**Distribution Tax**:
- Dramatic increase in network communications between services
- Total latency of calls across the network increases
- Risk of congestion causing catastrophic latency

**Reliability**:
- Reduction in overall system reliability with more moving parts
- Critical to evaluate core services' ability to handle unreliability
- Technologies can help mitigate but not eliminate risks.

**Conclusion**:
- Organizations need to consider benefits of microservices against the costs, especially complexity and deployment challenges
- Understanding potential pitfalls is essential for success in implementing microservices architecture.

Microservices and cloud native
**Microservices vs Cloud Native Architecture**

**Understanding Microservices and Cloud Native**
- Microservices: Focus of current course, not always coupled with cloud native
- Based on principles like 12 or 15 factor methodologies (loosely)
- Can be monolithic or cloud based
- Easily transitions into a cloud native architecture

**Cloud Native Architecture**
- Based on patterns for designing systems for cloud infrastructure
- Loose term, can include public, private, or hybrid cloud
- Focuses on increased uptime, scalability, and distribution
- Microservices fit well due to ease of transitioning

**Differences Between Microservices and Cloud Native**
- Two distinct concepts
- Monolithic applications can be cloud native, and vice versa
- Important to keep delineation clear for clarity

**Integration of Microservices and Cloud Native Architecture**
- In professional life: microservices aim towards a cloud native platform
- Single codebase in microservices (12 factor requirement)
- Self-contained units, easy transition with few changes
- Challenges include managing dependencies and leveraging backing services.

Microserice core Concept The services
**Microservices Overview**
- **Definition**: Microservice isn't based on size, but operation
- **Communication**: Utilizes HTTP (mostly REST), unified documentation and service discovery important
- **Size**: Handles one set of related functions with minimal cross-domain operations
- **Domain-focused design**: Similar to good object-oriented programming practices
  - Service operates on a well-defined domain
  - Domain spans multiple data objects or business processes
  - Low level, data-focused services may be provided
- **Experimentation**: Smaller size aids in faster experimentation and deployment

The communication dance
**Microservices Architecture and Communications: Key Concepts**

**Advantages:**
- Interservice communications enable growth
- Flexibility in using any coding language or framework for development
- Team members can work in their preferred languages and deliver code quickly

**Communication Strategy:**
- All communication between services is over HTTP
- Protocol-aware heterogeneous interoperability: services are bound to protocol, execute communications without learning new technologies

**Challenges:**
- Potential for system failure if no clear delineation or versioning strategy exists
- Every service can call any other service, making orchestration essential and API passivity crucial.

**Microservices Architecture:**
- Agile development approach with teams working in their preferred languages and frameworks
- Quick delivery of code due to minimal constraints imposed by architecture pattern

**RESTful Services:**
- Preferred communication method for microservices architecture
- All modern frameworks support RESTful services, unlike other communication protocols like SOAP.

Distribution and scale
**Key Concepts:**
- **Microservices Architecture**: Provides a distributed model for software communication with potential global distribution
- **Benefits**: Scalability and distribution
- **Distribution**: Each service can be accessed over remote network calls, allowing placement anywhere globally
- **Reality Perspective**: Costly in infrastructure and latency; benefits include solving distribution issues without making entire system global
- **Enterprise Perspective**: Allows for regional or global distribution of customer-facing applications and services while keeping enterprise-focused ones local
- **Scalability**: Each service is independent, allowing it to be individually scaled horizont or vertically
- **Horizontal Scaling**: Increasing instances of a service during high load periods
- **Vertical Scaling**: Allowing infrastructure planning for average day traffic with scalability handling increases and decreases in volume

The dangers of latency and gridlock
**Microservices Architecture: Understanding Latency and Gridlock Risks**

**Costs of Microservices:**
- Improved scalability and distribution come with costs
- Unacknowledged costs can lead to catastrophic failure

**Latency in Microservices:**
- Each service call is a remote network request
  - Connection setup, tear down, wire latency
- Latency insignificant for single calls but problematic in complex code paths
- Increased traffic and load heighten risk of response time delays
- Latency can cause gridlock and system failure

**Circular Calls:**
- Services can call any other service in microservices architecture
- Circular call stack can lead to latency issues and faster failure

**Controlling Negative Reactions to Latency:**
- Use circuit breakers: trip and execute default behavior during latency or timeout
  * Netflix's Hystrix implementation
- Implement strong timeout logic throughout system
- Global distribution, scaling of individual services under load
- Leverage patterns like circuit breaker to alleviate issues.

Bounded context
**Key Concepts:**
- **Microservices decomposition strategy**: Leverage domain-driven design to focus on bounded contexts when decomposing a large multi-domain system into individual services.
- **Importance of proper microservice decomposition**: Avoiding mistakes in migrating monolithic applications to microservices architecture by finding the sweet spot in granularity through domain-driven design.
- **Determining bounded contexts for domains:** Analyze traffic patterns based on real-world use cases and telemetry data, reduce crossed domain calls where appropriate.
- **Reducing latency**: Minimize unnecessary calls between services to improve system health and overall performance.
- **Better contracts between services**: Well-defined boundaries help consumers find the correct location for needed services and improve agility in development processes.

Data domains as a service boundary
**Key Concepts:**
- **Bounded contexts and microservices:**
  - Discussing data access layer challenges
  - Transactions in the data layer
  - Base vs acid discussions to follow
  - Difficulty of removing transactional boundaries in existing databases
  - Importance of considering data transactions

- **Building data domains for low level services:**
  - Hardest part of microservices architecture
  - Two strategies:
    1. Break up database into smaller databases and build associated services (quick but risky)
    2. Build services first and connect to monolithic database, then decompose databases (recommended)
  - Minimizing cross-domain calls and enforcing transaction boundaries
  - Solidifying data domains for efficient operations throughout the system

- **Telemetry and tracing pattern:**
  - Viable tool when building data domains
  - Helps ensure efficient operations.

No ACID, only BASE
**Distributed Transactions vs ACID vs BASE in Microservices Architecture**

**ACID Properties**:
- Atomic: operation succeeds or fails completely with no gray area
- Consistent: all constraints and data model rules are enforced
- Isolated: visibility rules are well-defined, preventing other transactions from reading incorrect data
- Durable: once completed, data is guaranteed to be in the data store permanently

**Challenges of ACID in Microservices**:
- Difficult to manage in distributed systems
- Impossible to achieve strict ACID properties due to distributed nature

**BASE Model in Microservices Architecture**:
- Strive for eventual consistency across highly available distributed platform
- Not guaranteed immediate, atomic, or isolated consistent transactions
- Aim to eventually achieve the end state across all nodes in distributed data store

**Advantages of BASE Model**:
- Suited for microservices architecture and eventual consistency
- Improves system health as a whole by aiming for eventual consistency

**ACID Transactions vs Microservices**:
- Identify where truly needed, wrap service boundaries around those operations
- Evaluate if perceived need for immediacy is just an unnatural expectation

**When to Use ACID Transactions**:
- In specific use cases like balance transfer in a banking system
- Model domains and services to allow atomic transactions

**Alternatives to ACID Transactions**:
- Synchronous design patterns or eventual consistency models for asynchronous operations.

The API layer
**Microservices Architecture and API Layer:**
- In microservices architecture, an API layer acts as a proxy for all service offerings (shielding clients from complexities)
- Standardized interface, exposing endpoints and operations with no transformation needed
- Useful in scaling systems under load or during lulls by hiding direct IP addresses and ports of services
- Isolates clients from change by providing a stable interface for accessing various services
- Facilitates versioning through proxy configuration
- Minimizes impact on clients during refactoring or addition of new service offerings.

Microserice advanced Concepts: Asynchronous communications
**Asynchronous Communications in Microservices Architecture**
- Relying on synchronous communication model for reducing latency is not effective
- Event-driven asynchronous communications improve system health and enable large data transfers
- Asynchronous communications require handling errors correctly and ensuring proper processing
- Event-driven microservices: services put messages into an asynchronous message broker or temporary store, downstream event processors handle data
- Stream data platforms can be useful for large systems with multiple operations, events trigger multiple activities
- Transitioning from synchronous to asynchronous processing reduces latency and increases throughput
- Important considerations: handling errors correctly, monitoring error queues and data correctness.

Logging and tracing in a microservices architecture
**Microservices Architecture Challenges and Solutions for Logging:**
* Difficulties in evaluating call chains and aggregating logging in microservices architecture (multiple virtual machines or containers)
* Importance of planning observability early in design process
* Unified approach to logging recommended across entire organization

**Logging in Microservices:**
* Critical for day-to-day operations, troubleshooting, maintenance, investigations
* Noiser in microservices environment due to larger volume and varied team logging strategies
* Increased need for convergence in logging behaviors as system grows
* Use of log aggregators with uniformity important for scanning and coalescing logs efficiently

**Tracing:**
* Solution for determining flow through services and system as a whole
* Based on creating unique token (trace) and embedding it in all internal logging events for call stack
* Trace ID passed downstream to all services throughout the system, making log aggregation simpler.

Continuous delivery as a requirement
**Key Concepts:**
1. **Agility of development teams**: maintaining team agility in a microservices architecture becomes challenging as the system grows in size. Smaller artifacts make deployment easier but can lead to difficulties.
2. **Continuous Integration and Continuous Delivery (CI/CD) pipeline**: an essential component for building and deploying microservices, automating the process from committed code to production.
3. **Build step**: compiles code and executes unit tests to ensure readiness for further testing and deployment.
4. **Automated deployment**: moves compiled artifacts to non-production environments for integration, system, and security tests before production release.
5. **Production deployment**: once validated, new code is deployed to production using techniques like blue-green deployment.
6. **Automation**: the end goal is automating as much of the process as possible to improve agility in microservices development.
7. **Starting small**: focus on building, deploying, and basic testing when moving to microservices before expanding to advanced automation.
8. **Priority**: considering CI/CD pipeline automation a requirement for reaping the benefits of agility offered by microservices architecture.

Hybrid architectures: Hierarchy and service-based
**Key Concepts:**
- **Microservices Architecture**: A daunting task for teams, with challenges like database segmentation and service boundaries
- **Hybrid Architectures**: Offer benefits of microservices without fully transitioning
- **Hierarchical Service Model**: Defines rules about which services can consume others; prevents circular dependencies in the network
- **N-tier Hierarchy Model**: Classes of services include data, business process, gateway, edge; builds out rules for service consumption
- **Risks of Hybrid Architectures**: Accommodating artificial rules may lead to pass-through services and complications
- **Service-Based Architecture**: Leaves databases untouched, offers agility improvements without sharding data into separate stores
- **Monolith of Monoliths**: Can occur when service offering extends beyond original scope in a hybrid model

Making Architectures CHoices: Design considerations
**Key Concepts:**
- **Continuous Integration and Delivery Pipelines**: Plan before writing any code
- **Logging, Tracing, and Telemetry Frameworks**: Primary function of every service, design early
- **Domain-Driven Design**: Analyze system to define service boundaries
- **Data Services**: Consider leveraging dedicated data services or wrapping access into business processes
- **Latency Management**: Evaluate non-blocking code and standardize stack
- **Asynchronous Architecture**: Create asynchronous operations first, reduce error rates and improve skills.

The tradeoffs
**Microservices Architecture: Trade-offs**

**Discussion on Microservices**:
- Building a microservices architecture is not a silver bullet for software development
- Talking about issues that can arise from this model, focusing on trade-offs
- Applying personal experience and information gathered from thought leaders

**Benefits of Distributed System**:
- Well-defined module boundaries
  - Harder to write tightly coupled code with service boundary calls
- Easier path for scaling system
  - Critical for companies like Amazon that operate globally

**Deployment Complexity in Microservices**:
- Ability to scale increases deployment complexity
- Managing many moving parts is a challenge, even with continuous delivery
- Polyglot development can lead to operational costs in managing diverse technologies

**Technological Diversity in Microservices**:
- Heterogeneous model allows using any technology for services
- Embracing polyglot development comes with real operational challenges
- Better to embrace a smaller set of technologies for easier management

**Conclusion**:
- Evaluate trade-offs within your system carefully
- Play to strengths and control weaknesses to achieve better results

An argument for edge services
**Microservices Architecture vs SOA (Service Oriented Architecture)**
- **SOA**: Beep layer allowed exposure of services over a common bus, leading to code bloat and infrastructure management issues
- **Microservices Architecture**: API proxy used to hide service implementations, preventing code bloat but risking transformation for client needs

**Edge Services**
- Two distinct types: outbound and inbound
- **Outbound Edge Services**: expose client's specific needs to the outside world (e.g., email marketing)
- **Inbound or Translation Services**: abstract you from third party dependencies (e.g., SMTP operations)

**Benefits of Inbound Edge Services:**
- Control impact of vendor API changes in one place
- Provide a path for vendor replacement if needed
- Minimize impact on system health with single service implementation
- Manage transformation risks through asynchronous operations

**Inbound Edge Service Example:** Email Marketing Scenario
- Company uses third party send system to handle email communications
- Build edge service to interact with the third party, controlling impact of changes and providing a path for replacement

**Benefits of Outbound Edge Services:**
- Managing transformations in code is easier than managing in proxy or API gateway layers
- Provide consistent client interface even if underlying services change
- Isolating services from changes is crucial for the system's health.

Embracing DevOps
**Key Concepts:**
- Microservices architecture: managing trade-offs and improvements, potential impacts, operational costs, continuous delivery model, culture
- DevOps culture: bringing development and operations into the same sphere, automation, monitoring, logistics, response times, agility
- Complexities in microservices: distribution tax, increased deployment counts, manual deployments, need for automation
- Benefits of DevOps and microservices integration: mitigating weaknesses, complementing strengths, improved communication, automated responses, continuous monitoring, faster response times.

Monolithic microservices
**Monolithic Architecture vs. Microservices: Preparing a Monolith for Future Breakup**

**Monolithic Architecture**:
- Not every use case is ready for microservices
- In early-stage startups, the concept of microservices may be too much for the small team to deal with
- Steps to prepare a monolith for an eventual breakup:
  - **Plan and Strategy**: Focus on using all strategies discussed, except breaking up components
    - Build out data services that can be broken apart in future
    - Domain-driven design, expose domains with solid APIs
    - Extracting these domains later is easier, even database schemas
  - **Encapsulate Services**: Encapsulate as many potential services as possible
    - Not all may be needed, but testable components are always beneficial

**Arguments for Monolithic Architecture**:
- **Unknown Unknowns in Startups**: Spend energy on product-market fit and keeping system scalable/distributable
  - Complex microservices architecture can wait
- **Resources and Team Size**: Monolithic approach is simpler when the team and application are small
  - Added complexity of microservices to gain agility is moot at that stage
- **Focus on Principles**: Good observability, solid APIs/UIs, encapsulation, CI/CD work well in monoliths

**Transitioning to Microservices**:
- When the system gains popularity and use, focus on key principles for scalability
- Breaking up a monolith into microservices is easier when it was designed that way

