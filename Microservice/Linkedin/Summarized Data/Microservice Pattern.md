Link: https://www.linkedin.com/learning/microservices-design-patterns-23454771/solving-microservices-problems-with-patterns?contextUrn=urn%3Ali%3AlyndaLearningPath%3A645bcd56498e6459e79b3c71&u=0
Name: Microservices: Design Patterns
Solving microservices problems with patterns
### Key Concepts from Microservices Study Material

#### Introduction
- **Context**: Emphasizes common challenges faced in building, converting, and operating microservices.
- **Collective Solution**: Utilization of design patterns to address these issues efficiently.

#### Speaker Information
- **Name**: Frank Moley
- **Roles**: Cloud native developer, architect, teacher, perpetual student

#### Core Message
- **Objective**: To introduce design patterns that will help save time and energy while focusing on business needs.
- **Approach**: Encourages the application of these patterns to streamline microservices development.

#### Summary Structure
1. **Challenge Identification**:
   - Common issues in microservices development, conversion, and operation are not unique.

2. **Solution Propagation**:
   - As a collective, software engineers create design patterns to solve problems once and apply them repeatedly.

3. **Expert Insight**:
   - Frank Moley’s background as a cloud native developer, architect, teacher, and perpetual student highlights his expertise in this field.

4. **Learning Objective**:
   - Participants will learn design patterns that can save time and energy while enabling focused attention on business needs.
Vernacular of microservices
### Microservices Terminology Overview

#### Service Types:
1. **Data Services**:
   - Connect to data sources within the system.
   - Not limited to databases; any valid source that can be served through a microservice.
   - Bound by domains defined in the global architecture.

2. **Business Services/Business Process Services**:
   - Higher level of abstraction built on top of data services.
   - Define business domains that may transcend individual data services for better business perspective alignment.

3. **Translation Services**:
   - Abstraction on third-party operations encapsulated under a custom facade.

4. **Edge Services**:
   - Serve data to users and external systems.
     - Example: Web view, content delivery service, mobile device service.

#### Platform Definition:
- An all-encompassing arena for multiple service operations across different data centers.
- Includes infrastructure, runtime, ancillary services, networking, storage, etc.
- Operational components should not be overlooked.
- Diagnostic components are also critical.
Microservices and cloud native
### Key Concepts on Microservices and Cloud Native

#### Introduction
- **Microservices vs. Cloud Native**: Microservices do not inherently make a system cloud native, and cloud native does not require microservices.

#### What is Cloud Native?
- **Architectural Style**: Cloud native is an architectural approach, not a specific pattern for solving problems.
- **Primary Goal**: Facilitating operations in the cloud with enhanced portability, scalability, and resilience.
- **Key Features**:
  - Externalizing configuration
  - Focusing on scalability
  - Fast application startup and graceful shutdowns

#### Cloud Native Applications
- **Portability**: Applications should work seamlessly across different environments (cloud or data center) without additional code.
- **Scalability**: Ability to run as a single unit or multiple units based on system needs, with support for auto-scaling.

#### Microservices
- **Personal Interpretation and Definition**: No clear definition; microservices are generally smaller, scoped units of work compared to monoliths.
- **Monoliths**: Large applications that expose many services in one artifact, making scaling complex.
- **Microservices Benefits**: Breaking down endpoints into distinct units for independent scalability.

#### Relationship Between Microservices and Cloud Native
- **Common Practices**: Both emphasize building scalable systems.
- **Interdependence Misconception**: While microservices often align with cloud native principles, they are not inherently required. Conversely, one can build cloud native applications without using microservices.
- **Coexistence**: Despite distinct definitions, they work well together to solve common challenges.

#### Conclusion
- Emphasize the importance of clarity in distinguishing between these concepts and their respective roles in system architecture.
Decomposition Patterns Decomposition of a system
### Overview of Microservices Decomposition and Patterns

#### 1. Service Types in Microservices:
   - **Service Types**: Microservices are designed to provide very specific functionalities within a broader system.
   - **Domain-Based Services**: These services are created based on functional domains identified through domain-driven design, breaking down the overall problem into manageable parts.

#### 2. Decomposition Patterns:
   - **Business Processes as Boundaries**: Complex business processes can serve as clear delineation points in microservices architecture due to their inherent coupling.
   - **Atomic Transaction Focused Decomposition**: For systems requiring strict consistency, decomposition is based on atomic transactions rather than broader business processes.

#### 3. Migration Strategies:
   - **Strangler Pattern**: A common strategy for migrating from a monolithic system to a microservices architecture by incrementally wrapping existing services in new microservice layers.
   - **Sidecar Pattern**: This pattern involves deploying operational functions as separate components alongside the main service, promoting separation of concerns and cleaner code.

#### 4. Domain-Based Services:
   - Focus on decomposing the overall problem into smaller, reusable functional domains to enhance maintainability and scalability.

This structured format provides a clear overview of key concepts in microservices decomposition and strategies for transitioning from monolithic architectures.
Domain-based microservices
### Domain Based Microservices Overview

#### Key Concepts:
1. **Domain Driven Design (DDD):**
   - Focuses on understanding the core business domains and their boundaries.
   - Helps in creating services that are aligned with the business logic.

2. **Data Domain Decomposition:**
   - **Purpose:** To enhance scalability by decomposing the system into smaller, focused microservices based on data domains.
   - **Benefits:** Makes services more manageable and easier to scale.
   - **Focus:** Data access patterns rather than underlying schema details.

3. **Service Design Principles:**
   - **Data Focus:** Services should focus solely on logic within their domain, ignoring external logic.
   - **Decomposition Strategy:** Split domains based on data usage and interactions.
   - **Aggregation:** Merge domains when there is enough shared functionality; split them to avoid redundancy.

4. **Domain Model Design:**
   - Begin with the domain model, representing the business logic outside the database schema.
   - Consider how models are represented, utilized, and consumed.

5. **Action Evaluation:**
   - Define actions needed on these models (beyond CRUD operations).
   - Incorporate actions relevant to the API contract.

6. **Service Definition & Implementation:**
   - Create service boundaries based on defined actions.
   - Expose these services via APIs.
   - Implement data storage and translation functions as required.

7. **Visualization of Service Building Steps:**
   - **Model Design:** Define attributes of the model.
   - **Action Definitions:** Identify necessary operations.
   - **Service Boundary Definition & API Exposure:** Outline service actions as APIs.
   - **Data Storage & Implementation:** Implement data storage or build functions for existing data stores.

#### Key Takeaways:
- The core focus is on understanding and aligning with the business domains.
- Use telemetry for making informed decisions where experience alone might be insufficient.
- Domain driven design is essential but goes beyond this course’s scope.
- Iteration, trial and error, combined with experience, are crucial in designing effective domain services.
Business process-based microservices
### Key Concepts of Business Process-Based Microservices

#### 1. **Purpose and Structure**
   - **Complex Processes**: Often, processes are more complex and don't fit into a single domain.
   - **Business Process Service (BPS)**: Helps in building structured microservices architecture by encapsulating specific business functionality.

#### 2. **Implementation Considerations**
   - **Don't Repeat Yourself Principle**: Avoids duplicating code logic across different components, especially when processes span multiple domains.
   - **Higher Level of Abstraction**: Provides a more structured way to handle cross-domain functionalities.
   - **Domain Encapsulation**: BPS helps encapsulate related domains but warns against adding unnecessary layers that increase network traffic.

#### 3. **Architecture and Design**
   - **No Data Access Layer**: Business process services typically do not have their own data access, keeping the separation between business logic and data management clean.
   - **Boundary Clarity**: Maintain clear boundaries to avoid monolithic structures.

#### 4. **Building a Business Process Service**
   - **Identify the Process**: Gather detailed requirements and define the specific business rules before starting.
   - **Data Domains**: Identify which domains are needed for each process.
   - **API Definition**: Define APIs that represent the processes, focusing on contracts rather than underlying models.
     - **RESTful Action Pattern**: Useful in providing a clear abstraction layer.

#### 5. **Development and Deployment**
   - **Modular Design**: Encapsulate business process code into its own module for easier maintenance.
   - **Implementation Steps**:
     - Define the processes.
     - Identify required data domains.
     - Define APIs corresponding to each process.
     - Implement the service, ensuring it is a "black box" to the outside world.

#### 6. **Visual Representation**
   - **Process Definition**: Expose multiple related but distinct business processes.
   - **Domain Identification**: Determine which domains interact with these processes.
   - **API Definition**: Define APIs for each process.
   - **Service Implementation**: Wire up services and modules to ensure seamless interaction.

### Summary
- **Purpose**: To simplify cross-domain functionalities through structured microservices.
- **Design Considerations**: Avoid code duplication, maintain clear boundaries, and focus on a clean separation between business logic and data access.
- **Implementation Steps**: Identify processes, define domains, create APIs, and implement modularly designed services.
Atomic transaction-based microservices
### Key Concepts in Microservices Architecture with Atomic Transactions

#### 1. **Necessity for True Atomic Transactions**
   - In microservices architectures, there may be situations where eventual consistency is insufficient.
   - When atomic transactions span multiple data domains, special logic and systems are needed to handle these cases.

#### 2. **ACID Compliance Across Data Domains**
   - These services must guarantee ACID (Atomicity, Consistency, Isolation, Durability) compliance across more than one data domain.
   - If only a single domain requires atomic transactions, no special service is needed due to the hidden underlying implementation.

#### 3. **Blocking API Calls for Transactions**
   - Cross-domain services require synchronous and blocking API calls until the commit is successful.
   - While asynchronous methods could be considered, they often need guarantees of success or errors, necessitating synchronous behavior.

#### 4. **Avoiding Distributed Transactions with Data Domains**
   - Using data domains with distributed transactions is complex and generally not recommended due to added system complexity.
   - Atomic services are simpler but require careful planning and definition of transaction rules.

#### 5. **Preparation for Building Atomic Services**
   - Ensure underlying data domains share a database; if they don't, merge them into a single shared database.
   - Define clear and concise rules for the transaction process, including rollback conditions.

#### 6. **Implementation Considerations**
   - Document rules in code comments or readme files for future reference.
   - Implement rollback handlers to handle potential bottlenecks in confirmations to remote systems.
   - Exit functions with a complete commit or rollback; avoid partial states as much as possible.

#### 7. **Complexity and Recommendations**
   - Atomic process services are complex to implement but essential when required.
   - Collect extensive data before deciding on implementing such services to ensure they are truly needed.
   - Consider alternatives like eventual consistency or simulated rollbacks, explaining their risks and benefits.

### Conclusion
- While atomic transactions across multiple data domains are necessary in certain scenarios, the complexity involved should be carefully weighed against simpler alternatives.
Strangler pattern
### Strangler Pattern Overview

#### Key Concepts:
1. **Pattern Definition**:
   - The strangler pattern involves decomposing a monolithic application into microservices by "carving" dependencies off of it over time.
   
2. **Decomposition Strategy**:
   - Start with the monolith and gradually move functionality to new microservice endpoints while replacing old functionalities in the monolith.

3. **Two Decomposition Strategies**:
   - **Top-down Approach**: 
     - Begin by building out API layers, then move down to data stores.
     - Example: Build a new API and service for each piece of functionality, eventually moving databases behind them.
   - **Bottom-up Approach**:
     - Start with the database and work your way up through data domains, business processes, etc.
     - Example: Define data access areas (data domains), create separate databases for each domain.

4. **Step-by-step Bottom-up Process**:
   1. Identify Business Processes in Monolith.
   2. Define Data Access Areas as Data Domains.
   3. Create New Database for a Single Data Domain.
   4. Build the Corresponding Data Domain Service.
   5. Migrate Client Usage to Use New Data Domain.
   6. Remove Old Data Access Block and Data from Original Database.
   7. Sync Logic (if necessary).
   8. Repeat Process for Other Data Domains.

5. **Final Outcome**:
   - The monolith is completely strangled, with all its functionalities replaced by microservices.
   - Deprecate the monolithic system once it no longer serves any clients or processes data.

### Summary
- **Pattern**: Strangler pattern decomposes a monolithic application into microservices by systematically replacing old functionalities with new ones.
- **Strategies**:
  - **Top-down**: Start from APIs and move to databases.
  - **Bottom-up**: Begin with databases and move up through domains and processes.
- **Process**: Gradually migrate clients, replace data access blocks, and sync data as necessary.
- **Outcome**: Monolith is fully replaced by microservices.
Sidecar pattern
### Sidecar Pattern Overview

#### Definition:
- **Purpose**: Offload processing tasks to a separate module (sidecar).
- **Deployment**: Deployed alongside each applicable microservice.
- **Isolation**: Processes run in an isolated environment but benefit from unified functionality.

#### Key Concepts:
1. **Reduction of Repetitive Code**:
   - Focus on removing redundant code paths within services.
   - Example functionalities: logging, monitoring, and network services.

2. **Design Considerations**:
   - Design the sidecar module to be specific for immediate needs while generic enough for broader use.
   - Challenges: Initial implementation might require iterative refinement.

3. **Deployment Process**:
   - **Step 1**: Define the design of the sidecar, ensuring it’s modular and reusable.
   - **Step 2**: Write the code for the sidecar.
   - **Step 3**: Schedule deployment via service manifest or definition.
   - **Result**: Sidecar functionality appears without modifying the main application.

4. **Benefits**:
   - **Modularity**: Independent processes can be added or removed as needed.
   - **Scalability**: Sidecars scale with their parent services.
   - **Maintainability**: Centralized management of shared functionalities like logging and monitoring.

5. **Visualization Example**:
   - **Initial Setup**: Three microservices in a virtual network.
   - **Logging Sidecar Addition**: Applied to all three services, providing unified logging functionality.
   - **Monitoring Sidecar Addition**: Applied similarly for centralized monitoring.
   - **Security Sidecar Addition**: Applied selectively (to one service) based on specific requirements.

#### Summary:
The sidecar pattern optimizes microservices by offloading common functionalities to separate modules. These sidecars enhance modularity, scalability, and maintainability while reducing redundant code paths within services.
Integration Patterns Gateway pattern
### Gateway Pattern for API Integration

#### Overview:
The **Gateway Pattern** is an ingress pattern designed to manage and control access to system services from external clients, providing a buffer and enhancing orchestration.

#### Problem Statement:
- Without a gateway, any client can directly access underlying services.
- Operations and maintenance needs escalate with more clients, especially third-party vendors.
- Potential for chaos increases as the number of clients grows.

#### Key Features:

1. **Buffer Between Services and Clients:**
   - Acts as a facade or simple proxy to manage external requests.
   - Can mutate or limit calls based on client-specific requirements.

2. **Single Point of Failure Risk:**
   - Care must be taken to ensure scalability and robustness.
   - Potential for single point of failure, so design should prioritize reliability.

3. **Payload Mutation:**
   - Allows customizing payloads to fit specific client needs.
   - Enables consistent application of security and authorization logic.
   - Useful for adding common headers or other metadata not relevant to the underlying service.

4. **Aggregation Capabilities:**
   - Aggregates data from multiple sources into a single payload for complex clients (e.g., high-bandwidth desktop clients).
   - Focus on simple aggregations; avoid applying business logic here.
   - Recommended pattern for more complex rules is the Process Aggregator Pattern.

5. **Access Limitation:**
   - Controls data sent to low-bandwidth or less capable clients (e.g., mobile devices).

6. **Contract-Driven API Point:**
   - Provides a static contract that can evolve independently of internal services.
   - Allows for multiple client types (web, desktop, mobile) and managed public APIs.

7. **Strategy for Building Gateway:**

   - **Define Contracts:** 
     - Start with small, static contracts as public touchpoints.
     - Tailor API sets to specific clients or focus on dynamic core APIs.
     
   - **Implement Version Control:**
     - Use strict version control (e.g., semantic versioning) to ensure backward compatibility.
     - Ensure that changes are passive and do not break the contract.

   - **Isolate Backend Changes:**
     - Implement internal client code in distinct modules for easier management.
     - Consume these modules within the gateway implementation to isolate backend changes from public contracts.

#### Conclusion:
The Gateway Pattern is crucial for managing external access, ensuring security, and maintaining a stable interface between clients and underlying services. Careful design and implementation are essential to leverage its benefits while mitigating risks.
Process aggregator pattern
### Process Aggregator Pattern Summary

#### Key Concepts:
1. **Purpose and Use Case:**
   - **Orchestration of Business Processes:** Used to integrate multiple business processes into a single API call.
   - **Complex Business Scenarios:** When multiple data domains need to be called within a business process.

2. **Aggregator Functionality:**
   - **Single API Call:** Clients make one API call that handles underlying calls and assembles the payload for the client system.
   - **Processing Logic Introduction:** Aggregators should introduce their own processing logic, encapsulating rules and consolidating payloads relevant to the model.

3. **Value and Best Practices:**
   - **Encapsulates Business Logic:** Reduces redundancy by encapsulating common business rules across multiple calls, adhering to the DRY principle.
   - **Design Considerations:**
     - Determine which business processes are needed behind the aggregator.
     - Define processing rules based on understanding the process and its requirements.
     - Design a new model for the aggregator that accounts for internal processing rules.

4. **Implementation Steps:**
   - **Model Definition:** The model should not be a simple pass-through but should reflect internal processing rules.
   - **API Implementation:** Use standard REST verbs if possible, or use action patterns as needed.
   - **Service Wiring and Internal Processing:** Implement the service by wiring together the necessary components and adding internal processing features.

5. **Challenges and Considerations:**
   - **System Choke Point:** Long-running processes can cause delays, making API calls blocking and potentially leading to system performance issues.
   - **Asynchronous Patterns:** For large data processing operations, asynchronous patterns may be more suitable to avoid choke points.
   - **Risk Management:** Encapsulate internal business processing rules to maintain design integrity and prevent future maintenance issues.

6. **Conclusion:**
   - The aggregator pattern is useful in specific scenarios but should be used with caution to avoid introducing potential bottlenecks in the system.
   - Abstracting for abstraction's sake can lead to network issues in distributed microservices architectures, so consider these implications carefully before implementation.
Edge pattern
### Edge Pattern Overview

#### Key Concepts:
1. **Subset of Gateway Pattern**: 
   - The edge pattern is a specialized subset of the gateway pattern, focusing on specific clients.

2. **Scalability Concerns**:
   - When client types like mobile contribute significantly to request volume, scaling a single gateway can become wasteful.
   - Edge services handle this by targeting individual clients more efficiently.

3. **Client-Specific Business Logic**:
   - Provides special business logic tailored for specific clients (e.g., mobile).
   - These services act as highly client-specific gateways.

4. **Isolation and Flexibility**:
   - Focus on a single client, allowing for more dedicated energy on that specific need.
   - Aggregation, consolidation, and isolation are handled based solely on the client's requirements.
   - Flexible in handling increases or decreases in client load without affecting other systems.

5. **Design Process**:
   - Identify the client and its needs, constraints.
   - Build contracts and associated models for APIs and services.
   - Scale appropriately as needed, driven by specific client usage.
   - Reduce passive concerns to a version scope tied to the client.

6. **Maintenance Considerations**:
   - Gateway pattern offers consolidation of modules and processes, improving maintainability.
   - Edge services reduce impact on other systems when deploying new versions or addressing new clients.

7. **Security Benefits**:
   - Enhanced security through OAuth integration, providing a good security footprint for edge services.
   - Targeted deployment minimizes the risk of exposing unapproved APIs to the system.

8. **Conclusion**:
   - The author prefers using only edge services over gateways due to their client-specific focus and flexibility in handling various client needs without impacting other systems.

This summary captures the essence of the edge pattern, its advantages, and the reasoning behind preferring it over gateway patterns for specific use cases.
Data Patterns Single service database
### Key Concepts: Single Service Single Database Pattern in Microservices Architecture

#### Overview:
- **Primary Use Case**: Commonly used for data-domain-based services.
- **Core Concept**: Each microservice has its own dedicated database.
- **Scalability Considerations**:
  - Service scalability should be proportional to the database's scaling needs.
  - Sizing databases based on peak usage of a single service can lead to inefficiencies.

#### Benefits:
1. **Isolation and Independence**:
   - Data domains are isolated, allowing independent scaling of services and data stores.
2. **Scalability Flexibility**:
   - Services and their associated databases can be scaled independently without impacting the entire system.
3. **Regional Isolation (Advanced)**:
   - Potential to isolate data per region while maintaining overall system functionality.

#### Implementation:
1. **Initial Setup**: A single microservice with its dedicated database.
2. **Service Expansion**:
   - Adding more services, each with their own databases.
   - Example: Two new services added, each with its own database.
3. **Load and Scaling**:
   - Increased load on a service leads to additional instances of that service.
   - Concomitant increase in database load necessitates scaling the database as well.
4. **Scaling Mechanism**:
   - Typically achieved by increasing the size of the database (e.g., more IOPS).

#### Limitations and Considerations:
- **Cost Implications**: Proprietary databases or improperly sized databases can be costly.
- **Atomic Transactions**: Need to consider if data domains include atomic transactions, which might require less fine-grained scaling.

### Summary
The single-service single-database pattern is a fundamental approach in microservices architecture. It ensures that each service has its own dedicated database, allowing for independent scalability and efficient resource management. While not perfect, this model offers significant benefits in terms of isolation, flexibility, and scalability when implemented correctly.
Shared service database
### Shared Database Pattern Overview

#### Key Concepts:
1. **Pattern Usage**:
   - The single service, single database pattern is generally preferred.
   - However, there are scenarios where a shared database must be used (e.g., due to signed contracts).
   - Startups can benefit from this pattern as it allows focus on product-market fit and reduces overhead.

2. **Data Domain Handling**:
   - Even though all data domains exist within one database instance, they should still be treated as separate databases for logical and coding purposes.
   - Data distribution should ideally be managed by the database itself to avoid issues with code synchronization.

3. **Database Synchronization**:
   - When deploying across multiple data centers, ensure the database handles synchronization; otherwise, manual code management can lead to out-of-sync databases.
   - Modern databases often have poor support for WAN replication, which can compromise functionality.

4. **Choosing Databases**:
   - Select appropriate databases carefully, considering scalability and future-proofing needs.

5. **Data Structure Strategy**:
   - Leverage distinct databases within a single engine or use schemas, key spaces, etc., to logically isolate data.
   - This approach allows for writing code with a single database isolation model despite shared storage.

6. **Schema Segmentation**:
   - Each service consuming a schema should have unique credentials that do not span logical breaks.
   - Users connecting to multiple schemas might as well stick to the existing model.

7. **Data Domain Connectivity**:
   - Ensure data domains connect to single schemas, maintaining logical isolation even with shared storage.

8. **Future Scalability Considerations**:
   - By enforcing these patterns during startup phase, it becomes easier to break up databases logically later when scaling demands arise.
   - Good isolation practices at the outset can simplify future database management and scalability efforts.
Command Query Responsibility Segregation
### Key Concepts of Command Query Responsibility Segregation (CQRS) Pattern

#### Introduction
- **Complexity**: CQRS is among the most complex data patterns for microservices.
- **Ethereality**: It's a sophisticated concept in data management that can significantly enhance system behavior when implemented effectively.

#### Core Problem
- **Divergence from CRUD**: Traditional CRUD operations unify reading and writing rules, whereas CQRS introduces multiple models (queries and writes) within the same bounded context.
  - **Queries**: Transform and aggregate schema to represent a specific use case.
  - **Writes**: Inject behavior and infer characteristics based on different rules.

#### Complexity
- **Eventual Consistency**: The underlying data remains consistent over time, but immediate reads after writes may not reflect the latest state due to delays in updating queries.
- **Increased Complexity**: Requires special handling for business processes beyond CRUD models.

#### Use Cases
1. **Task-Based User Interfaces**
   - Focus on tasks during write operations.
   - Read models are based on system state post-interactions from these tasks.
2. **Event-Driven Models**
   - Integrates well with event-driven architectures where triggers and events occur from write operations, making it ideal for scenarios where immediate read access to recently written data is not required.

#### Implementation Considerations
- **Initial Design**: Requires significant design effort before implementing.
- **Maintainability**: Can become a nightmare if implemented poorly.
- **Use Case Matching**: Suitable when use cases inherently involve eventual consistency and event-driven behavior.

#### Conclusion
- **Powerful Tool**: CQRS can dramatically reduce complexity in access patterns when done correctly, despite the added complexity of its implementation.
- **Homework Required**: Extensive research and design are necessary before embarking on a CQRS project to ensure successful integration.
Asynchronous eventing
### Summary of Asynchronous Eventing in Microservices

#### Key Concepts:
1. **Definition**:
   - **Asynchronous Eventing**: A method used to handle long-running transactions or complex workflows that cannot fit into a single blocking API call.
   
2. **Use Cases**:
   - Situations where real-time processing through blocking calls is impractical or impossible.
   - Processes that require non-real-time handling, such as business processing, auditing, security, eventing, infrastructure creation, and configurations.

3. **Pattern Characteristics**:
   - A service API triggers the event.
   - The event cascades asynchronously from the API, leading to a series of actions executed behind the scenes after the client receives an accepted message.
   - Often involves making a single blocking call to put a message on a messaging system, then returning control to the client while processing occurs in the background.

4. **Benefits in Distributed Systems**:
   - Highly effective for solving complex problems within distributed systems.
   - Not a silver bullet but addresses many critical issues effectively.

5. **Learning Resources**:
   - Further details are available in the course "Microservices: Asynchronous Messaging" for a comprehensive understanding of both the why and how.

6. **Importance**:
   - Considered one of the most important patterns to learn, especially when managing data domains.
   - Widely used by the speaker in various system-building scenarios, underscoring its practical value.

This summary captures the essence of asynchronous eventing as a critical pattern in microservices architecture and highlights its significance in addressing complex workflows.
Opearation Patterns Log aggregation patterns
### Operational Patterns: Log Aggregation

#### Key Concepts:

- **Purpose**: To provide detailed information about the runtime behavior of microservices for quick diagnosis and resolution of operational issues.

- **Problem**: 
  - In microservice architectures, logs are scattered across multiple services.
  - Lack of consistent structure and taxonomy makes it difficult to aggregate and analyze logs effectively.

#### Structure and Format:
- **Consistency Across Services**: Logs must be consistent in structure and format across the entire system for effective aggregation.
- **Polyglot Programming Challenges**: While polyglot programming can complicate consistency, making log output uniform is crucial.

#### Aggregation Process:
- **Aggregation**: 
  - Consolidates logs from different services into a single stream of data.
  - This involves standardizing output locations and using common taxonomy for identifiers and key values.
  
- **Parsing**: 
  - Structured logs require less parsing due to well-defined rules, making the aggregation process more efficient.

#### Importance:
- **Correlation**: Proper structure allows for better correlation of log messages, aiding in the identification and resolution of issues.
- **Tracing Identifiers**: Ensuring consistent injection of tracing identifiers across services enables call stack recreation.

#### Implementation:
- **Tools and Frameworks**: Utilize off-the-shelf components such as structured logging frameworks available in most programming languages.
- **Common Taxonomy**: Establish a shared taxonomy for log messages to ensure clarity and ease of interpretation by all consumers.

### Summary
Log aggregation is essential in microservice architectures to provide consistent, structured logs that can be efficiently aggregated, parsed, and analyzed. By ensuring consistency across services and using common taxonomy, log data becomes invaluable for diagnosing issues quickly. Utilizing existing tools and frameworks simplifies this process significantly.
Metrics aggregation patterns
### Key Concepts Summary

#### Metrics vs Logging
- **Usefulness**: Metrics can be more operationally useful than logging if used correctly.
- **Ease of Implementation**: Metrics require less human interaction and minimal development effort compared to logging.

#### Purpose of Metrics
- **System-Wide Monitoring**: To understand the overall health and performance of a system, while also being able to drill down into individual services.
- **Non-Codified Data**: Focuses on system-level data rather than code output.

#### Taxonomy and Consistency
- **Standardization**: Use consistent and descriptive keys for metrics to ensure clarity in dashboards.
- **Common Keys with Logs**: Aligning common keys between metrics and logs can enhance the interpretability of both.

#### Metrics Collection and Shipping
- **Libraries and Tools**: Leverage existing standard libraries in most programming languages.
- **Aggregation Solutions**: Use established shipping standards for metrics aggregation solutions.
- **Visualization**: View collected metrics graphically through dashboards provided by these solutions.

#### Dashboard Design
- **High-Level Dashboards**: Create broad, high-level dashboards to detect potential issues early.
- **Service-Specific Dashboards**: Develop detailed dashboards for each service when specific issues arise.
- **Linkage**: Include links to log queries and event embeddings (system/user/deployment) in dashboards.

#### Alarm Points
- **Tracing Graphs**: Add traces on graphs at alarm points to visually aid in resolving issues.
- **Runbooks and Alarms**: Ensure runbooks are prepared for every alarm, detailing what metrics and logs to check.

#### Operational Best Practices
- **Early Detection**: Use high-level dashboards to quickly identify potential problems.
- **Resolving Issues**: Detailed dashboards can provide deeper insights into specific services.
- **Ease of On-Call Activity**: Embed necessary links (runbooks, log queries) in dashboards and pages for quick access.

#### Conclusion
- **Critical Importance**: Metrics are crucial for understanding system errors, health, and user experience.
- **Operational Efficiency**: Properly structured metrics help in quicker resolution times and better on-call management.
Tracing patterns
### Key Concepts of Tracing Patterns in Microservices-Based Systems

#### Introduction
- **Context**: In a microservices-based system, call stacks can quickly get lost.
- **Importance of Tracing**: Tracing is crucial for diagnosing issues and understanding the flow of service calls.

#### Monolithic vs. Microservices Architecture
- **Monolithic System**: Code execution from edge to database in a single process; stack traces are straightforward.
- **Microservices Architecture**: Calls span multiple processes and networks, making traditional stack tracing ineffective.

#### Tracing Mechanism
- **Trace Identifier Injection**:
  - Injects a trace identifier into every call to recreate the call stack.
  - Span from edge services to database calls (or directly).
  - Logs should include this trace ID for further diagnostics.

#### Implementation Guidelines
1. **Standards-Based Approach**:
   - Use open standards like OpenTracing or OpenTelemetry to ensure compatibility with off-the-shelf tools.
2. **Injection Points**:
   - Inject the trace ID at the entry point of your system (e.g., browser, edge service, ETL).
3. **Logging**:
   - Embed the trace ID in every log message using common taxonomy.
4. **Tools and APM**:
   - Leverage tracing tools and Application Performance Monitoring (APM) to visualize call stacks.

#### Best Practices
- **Avoid Homegrown Solutions**: Use existing, well-established patterns.
- **Consistency**: Ensure that all components honor the trace identifier.
- **Visualization**: Utilize tracing tools for better understanding of call stacks during troubleshooting.

By following these guidelines, you can effectively manage and trace calls in a microservices architecture.
External configuration
### Key Concepts in Externalized Configuration for Microservices

1. **Operational Importance**:
   - **Value Proposition**: The primary benefit of externalized configuration lies in operational efficiency rather than strict distribution requirements.
   - **Issue Resolution**: Having a clear spot to view and modify configurations outside the codebase can significantly reduce downtime during incidents.

2. **Externalization Mechanisms**:
   - **Runtimes and Frameworks**: External configuration is facilitated by tools like Kubernetes, Spring, etc., which inject environment variables into applications.
   - **Tooling**: Use tools that make it easy to find and manipulate external environment variables consistently.

3. **Consistent Naming**:
   - **Operational Patterns**: Consistent naming conventions are crucial for on-call engineers to resolve issues quickly.
   - **Resolution Time**: Inconsistent variable names can lead to longer resolution times during incidents.

4. **Configuration Exposure**:
   - **Default vs Externalization**: Always err on the side of externalizing configuration; however, ensure that critical secrets are protected through special constructs.
   - **Secure Access**: Provide secure paths for on-call teams to access secrets without exposing them publicly.

5. **Pattern and Implementation**:
   - **Configuration Injection**: Configurations are typically injected during startup or retrieved as part of the framework’s initialization routine.
   - **Language-Specific Mechanisms**: Each programming language has specific methods for accessing these values, but use common libraries and toolings to simplify this process.
   - **Default Values**: Use default values where they make sense; externalized config should be preferred when dynamic behavior is needed.

6. **Basic Pattern**:
   - **Read Config, Flex Behavior, Act**: The core pattern involves reading the configuration, dynamically adjusting behavior based on those values, and acting accordingly.

### Summary
Externalizing configurations in microservices enhances operational efficiency by providing a clear and manageable way to handle environment-specific settings. While it is not strictly required like in cloud-native environments, it significantly improves incident response times. Consistent naming conventions, proper handling of secrets, and leveraging existing tooling are crucial for effective implementation. The fundamental pattern involves injecting configurations during startup, utilizing them dynamically, and ensuring secure access where necessary.
Service discovery
### Key Concepts of Service Discovery in Microservices Architecture

#### Problem Statement:
- As microservices architectures grow, managing and finding appropriate services to use becomes increasingly complex.
- Traditional configuration methods become less manageable as the number of microservices increases (e.g., hundreds or thousands).

#### Solution: Service Discovery
- **Purpose**: To simplify the process of locating and interacting with specific services in a dynamic runtime environment where service locations can change.

#### Core Concepts:
1. **Centralized Location for Discovery**:
   - A central registry or directory that services use to advertise their existence and capabilities.
   
2. **Service Advertisement**:
   - New services register themselves by advertising their URI (Uniform Resource Identifier) and the models or behaviors they expose.
   - Example: "At location foo, you can find services for bar."

3. **Querying the Central Registry**:
   - Services can query this central registry to discover other services that provide needed functionalities and retrieve their URIs.

4. **Dynamic Resolution**:
   - The central registry returns a URI based on the service's advertisement.
   - The client then calls the discovered service using this URI, rather than relying on static configuration.

#### Advantages:
- **Extensibility**: Easier to add or remove services without changing client configurations.
- **Flexibility**: Services can scale dynamically without affecting clients' ability to find and use them.

#### Implementation Considerations:
- **Use Off-the-Shelf Components**: Many companies, like Netflix, have open-sourced components for service discovery that can be leveraged if available.

#### Conclusion:
- While not essential for small systems, the value of service discovery becomes apparent as microservices scale.
- It provides flexibility and ease of management, making it a useful pattern to keep in one’s toolkit.
Continuous delivery
### Continuous Delivery Process Overview

- **Definition**: Continuous delivery involves constantly delivering new code to production with full automation.
- **Operational Pattern**: Effective outside of microservices as well.

### Strategy for Moving Artifacts Through Environments

1. **Artifact Publishing**:
   - Triggers: Code built and unit tests run.
   - Action: Artifact is published, triggering the movement into non-production environments.

2. **Seamless Automation**:
   - Process in non-prod should be fully automated and seamless.

### Non-Production Environment Testing

1. **Automated Integration Tests**:
   - Deploy integration test suites alongside code deployments.
   - Setup data conditions and execute against exposed APIs.
   - Generate extensive logs for easier debugging if needed.

2. **Security Testing**:
   - **Penetration Testing**: 
     - Execute on every deployed non-prod environment, including non-UI components.
     - Ensures changes do not negatively impact security.
   - **Internal Security Tests**:
     - Conducted via third-party tools.
     - Stress test likely areas of vulnerability.

3. **User Acceptance Testing (UAT)**:
   - Use external frameworks for UAT tests.
   - UIs change often, requiring significant care.
   - Benefits increase with increased effort invested.

### Production Environment Monitoring

- Drop UAT in production but implement continuous smoke testing using cron operations to test popular workloads.
- Maintain high confidence levels through ongoing automated testing.

### Importance of CI/CD for Microservices

- CI/CD is crucial for microservices, more so than other development methods.
- Investing time and energy into strong automation patterns is worthwhile.
Documentation
### Key Concepts for API Documentation in Microservices Architecture

1. **Importance of Documentation**:
   - Critical in microservices architecture due to multiple teams with different focus areas.
   - Facilitates inter-team communication and collaboration.

2. **Documentation Patterns**:
   - Use native patterns based on service definitions (e.g., Restful services).
   - Examples: OpenAPI for documenting contracts.
   - Flexibility in approach: Contract-first or code-first development.

3. **Consistent Documentation Sharing**:
   - Each service should expose its documentation at a consistent location, e.g., `/docs` via HTTP GET request.
   - Use tools and frameworks specific to the language and framework being used (e.g., OpenAPI).

4. **Centralized Documentation Repository**:
   - Automate the process of publishing documentation updates from individual services.
   - Utilize service discovery tools for crawling and aggregating documentation.

5. **Enhancing Documentation Quality**:
   - Include examples of API consumption to aid users in understanding usage.
   - Provide team contact information within documentation for support queries.

6. **Operational Impact and Best Practices**:
   - Improves operations, agility, and code reuse.
   - Integrates documentation into the development process through pull requests.
   - Ensures thorough discussion of code and APIs before implementation.
