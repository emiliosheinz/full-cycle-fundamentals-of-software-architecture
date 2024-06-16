# Fundamentals of Software Architecture

Software architecture is a crucial discipline that underpins the successful development, deployment, and maintenance of large and scalable software systems. It encompasses various specialties, each with a unique focus and role within the broader context of technology and business strategy.

## Types of Architecture

1. **Software:** Specialty that involves everything related to software development, including documentation, design, coding, testing, and deployment.
1. **Solution:** Specialty that focuses on the design of a system or application as whole. It is right between product and software.
1. **Technological:** Specialty in market-specific technologies such as Java, .NET, Elastic Stack, etc;
1. **Corporate:** Specialty in policies, procedures, and standards that strategically impact the organization as a whole.

## Why should you learn Software Architecture?

Learning software architecture is essential for developers, regardless of their aspirations to become software architects, as it allows for a broader and more detailed understanding of the functioning and evolution of systems. With knowledge in architecture, developers can make more informed decisions, evaluate different approaches, and choose the best solution for a given context. This understanding facilitates long-term maintenance, prevents excessive influence from new technologies, and allows for a more strategic view of the software's impact on the organization. Additionally, software architecture involves design patterns and best practices that contribute to efficiency and standardization in development. With this knowledge, developers gain confidence, make safer and more informed decisions, and better understand the value of their work, fostering a sense of belonging and motivation.

## Architecture vs Design

Learning software architecture and design are often viewed as the same, but they are actually distinct. **Architecture:** refers to the global scope of software, considering high-level aspects like componentization, communication methods, and abstractions. It ensures that quality attributes, high-level constraints, and business objectives are met. On the other hand, **Design** focuses on a more local scope, like reducing a class's responsibilities and implementing patterns to facilitate strategies. While all architectural activities involve design, not all design activities are architectural. For instance, high-level decisions like using Open Telemetry for logging are architectural, but the specific code implementation is a design decision. Architectural decisions impact the broader system, whereas design decisions may be more localized and not visible outside their component. This distinction is important, though not universally accepted.

## Pillars of Software Architecture

The pillars of software architecture are the fundamental concepts that guide the design and implementation of software systems. They include:

1. **Structure:** Refers to the organization of components and their relationships. It needs to be flexible, scalable, and maintainable, while attending the business requirements.
1. **Components:** Are the building blocks of the system. They should be cohesive, loosely coupled, and reusable.
1. **Relationship between systems:** Refers to how systems interact with each other. It should be clear, efficient, and secure.
1. **Governance:** Refers to the rules and policies that guide the architecture. It should ensure that the architecture is properly documented, implemented, and maintained.

## Architectural Requirements

Architectural requirements are the constraints and quality attributes that guide the design and implementation of a system. They include all the areas of the company that the system will touch. Some examples are:

1. **Performance:** Respond to user requests within a specific time frame.
1. **Data Storage:** Store and retrieve data efficiently, according to the business requirements. A given system could be enforced by law to store their data on a specific location, for example.
1. **Scalability:** Grow and handle increased demand.
1. **Security:** Protect data and resources from unauthorized access and have required security certifications.
1. **Legal and Compliance:** Comply with laws and regulations, such as GDPR, HIPAA, etc.
1. **Audit:** Track and log events for auditing purposes.
1. **Marketing:** Track and analyze user behavior, providing insights for marketing strategies.

## Architectural Characteristics

Every time you develop a system, it inherently possesses given characteristics, sometimes, they are poorly implemented, but **intentional design** can improve them. When designing a system, understanding its structure is crucial because it allows you to address impactful points **intentionally**. Without this vision, problems are often solved indirectly and accidentally, which is not ideal. For example, software resilience is necessary for adapting and recovering from crises. If resilience happens by chance due to libraries, it’s not reliable enough. Therefore the architectural characteristics, often non-functional requirements, ensure the system supports the load and remains online during a crisis and they can be divided into three main categories:

1. **Operational:** Operational characteristics envolve several aspects of the system which are vital for your application to be able to operate under non optimal conditions. Even if you aren’t directly managing these aspects, they still important to be aware of them. Some examples are:

   - **Ensuring software availability** involves setting SLAs and SLOs, managing uptime, and planning for system recovery;

   - **Observability** is crucial for tracking availability, and techniques like SRE can help manage downtime;

   - **Disaster recovery** plans are essential, especially for critical systems, and must include strategies for multi-region or multi-cloud deployments to handle failures;

   - **Performance** is another key aspect, involving considerations of latency and throughput. It's vital to design systems to handle the expected load, whether it's 50 or 5000 requests per second, affecting choices like database types;

   - **Backup strategies** and regular testing are crucial to ensure reliability, especially against ransomware attacks;

   - **Security and reliability** also require attention to prevent brute force attacks and manage user authentication securely;

   - **Robustness and scalability** are critical for handling unexpected loads and ensuring the system can grow horizontally and vertically.

1. **Structural:** These characteristics are more closely tied to the development process and how you will build the application. While operational characteristics help with the system's operation and growth, structural characteristics focus on making the software increasingly flexible.

   - **Configurability:** Ensure the software is easily configurable using environment variables or configuration files, and test it across different environments without altering the source code;

   - **Extensibility:** Design the application to easily incorporate third-party elements and adapt to new requirements using interfaces and adapters;

   - **Easy Installation:** Standardize the installation process using containers (e.g., Docker) and manage dependencies effectively;

   - **Component Reuse:** Utilize reusable components to streamline development, and maintain shared libraries to avoid redundancy in distributed systems;

   - **Internationalization:** Plan for currency conversions, payment gateways, and pricing policies. Ensure the frontend accommodates different languages and cultural contexts;

   - **Maintainability:** Follow principles like SOLID, use design patterns, and ensure proper testing to maintain and extend the system easily;

   - **Portability:** Design the system to be less dependent on specific vendors, making it easier to switch databases or observability tools;

   - **Observability:** Implement standardized logging, centralized logging, and metrics to support effective troubleshooting and system support;

   - **Reusability of Components:** Make use of shared libraries and frameworks, especially in monolithic systems, to facilitate the reuse of components and avoid duplicating efforts across teams;

   - **Supportability:** Implement effective logging and monitoring practices to quickly identify and resolve issues, ensuring smooth operation and support for the application.

1. **Cross-Cutting:** These are aspects of software architecture that affect multiple modules or components throughout the application. Therefore, they are essential for ensuring the system's overall quality and performance.

   - **Accessibility:** Ensure your app accommodates diverse user needs, including those with disabilities, using tools and standards for screen reader compatibility, for example.

   - **Data Management:** Efficiently handle data retention and recovery strategies to balance storage costs and compliance requirements.

   - **Authentication and Authorization:** Implement robust mechanisms for user authentication and authorization, leveraging identity providers and API Gateways in distributed systems.

   - **Legal Compliance and Privacy:** Ensure adherence to data protection laws (e.g., LGPD), segregate sensitive data, and employ encryption to safeguard user privacy.

   - **Security:** Integrate security measures across all application layers, utilizing web firewalls and adhering to open standards to mitigate vulnerabilities.

   - **Usability:** Enhance usability across Front End and Back End, employing tools for user behavior analysis and ensuring APIs are well-documented and user-friendly.

## Performance

Performance is a critical aspect of software architecture, as it directly impacts user experience. To ensure optimal performance, architects must first understand how to measure performance metrics. The key units used to measure performance include:

- **Latency or Response Time:** The time taken for a request to travel from the client to the server and back or the time taken to respond to a user request. It is typically measured in milliseconds.
- **Throughput:** The number of requests processed per unit of time, typically measured in requests per second.

And the main reasons for poor performance usually are:

- **Inefficient Algorithms:** Algorithms that are not optimized for performance can lead to slow response times.
- **Inadequate Hardware:** Insufficient hardware resources can limit the system's ability to handle high volume of requests efficiently.
- **Working with blocking I/O:** Blocking I/O operations can lead to performance bottlenecks, especially in systems with high concurrency.
- **Serial and Synchronous Processing:** Serial and synchronous processing can lead to poor performance, as each operation must wait for the previous one to complete.

But there are always ways to address these issues and improve performance:

- **Optimize computational capacity:** Identify and optimize the most resource-intensive parts of the system to improve overall performance (CPU, memory, disk, etc).
- **Optimize algorithms:** Use efficient algorithms and data structures to reduce the time complexity of operations.
- **Optimize I/O operations:** Use non-blocking I/O operations to improve system responsiveness and reduce latency. Embrace concurrency and parallelism to improve throughput.
- **Database optimization:** Make sure you are using the right Database for the problem, optimize queries, indexes, and caching strategies.
- **Caching:** Use caching mechanisms to store frequently accessed data and reduce the number of requests to the server.

## Scalability

Scalability is the ability of systems to support an increase (or decrease) in workloads by increasing (or decreasing) the cost in a proportionate or smaller manner.

### Scalability vs Performance

While performance focuses on reducing latency and increasing throughput, scalability aims to provide the ability to increase or decrease throughput by adding or removing computational capacity. In other words, scalability is a broader concept that encompasses performance and other aspects of system design.

### Types of Scalability

1. **Vertical Scalability:** Involves increasing the capacity of a single machine by adding more resources, such as CPU, memory, or storage. It is limited by the hardware's physical constraints and can be expensive.

1. **Horizontal Scalability:** Involves adding more machines to the system to distribute the workload. It is more cost-effective and can be scaled infinitely, but it requires additional complexity to manage the distributed system.

### Scaling your Database

Scaling a database is a complex task that requires careful planning and consideration of various factors. There are several strategies for scaling databases, including:

1. **Vertical Scaling:** By increasing the resources of a single machine, such as CPU, memory, or storage, you can improve the database's performance. However, this approach has limitations and can be more expensive.

1. **Segregating Responsibilities:** By separating read and write operations, you can distribute the workload across multiple database instances, improving performance and scalability. But it adds additional complexity to manage the data consistency across the instances.

1. **Horizontal Sharding:** This means you will split your data into smaller parts and distribute them across multiple database instances. But it requires careful planning to ensure data consistency and avoid data loss, corruption, or duplication.

1. **Serverless Databases:** By using serverless databases, you can scale your database automatically based on demand, reducing the need for manual intervention and improving cost efficiency. But usually this approach is the most expensive one and comes with risks such as vendor lock-in.

1. **Query Optimization:** This includes using indexes, avoiding full table scans, minimizing the number of queries, and optimizing the database schema to improve query performance.

## Resilience

Resilience is the ability of a system to adapt and recover from crises, ensuring that it remains operational and available to users, allowing us to minimize the risks of data loss, for example. It is a critical aspect of software architecture, especially in today's fast-paced and dynamic environments.

### Resilience strategies and best practices

1. **Health Checks:** Implement health checks to monitor the system's status and detect failures early, allowing you to take corrective actions before they impact users. It's important to mention that health checks should actually check the system's health, not just return a HTML with 200 status code.

1. **Rate Limiting:** Implement rate limiting to prevent abuse and protect the system from excessive traffic, ensuring that it remains responsive and available to legitimate users.

1. **Circuit Breaker:** Circuit breakers can be used to temporarily block requests to a failing service and redirect them to a fallback mechanism. Preventing cascading failures.

1. **API Gateway:** An API Gateway can be used to manage incoming requests, enforce policies, and provide a unified interface to the underlying services. It's important to mention that it can be use to implement rate limiting and circuit breakers, for example.

1. **Service Mesh:** A service mesh can be used to manage service-to-service communication, provide observability, and enforce security policies. It can also help with resilience by providing features like circuit breaking, retries, and timeouts.

1. **Redundancy:** By replicating critical components and data across multiple servers, you can ensure that the system remains operational even if one server fails. This approach can be costly but is effective in ensuring high availability.

## Conclusion

Software architecture is a critical topic that ensures the successful development, deployment, and maintenance of large and scalable software systems. By understanding the different types of architecture, the pillars of software architecture, and the architectural requirements, developers can make more informed decisions, evaluate different approaches, and choose the best solution for a given context and problem. Additionally, by focusing on the architectural characteristics, developers can ensure that the system supports the load and remains online during a crisis, while also making the software increasingly flexible and adaptable. That way improving user experience and ensure the system's long-term success.
