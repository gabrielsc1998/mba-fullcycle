## MBA Full Cycle - Software Architecture Fundamentals

- Is directly linked to the development of the software itself;
- Affects the structure of the teams in an organization (Conway's Law);
- It's the relationship between the components of a software and the business rules;
- Is thinking about solving problems and evolving with time and demands;

### Software Architect

- Translates the business requirements into technical requirements and architectural patterns;
- Manages the developers and domain experts;

### Architecture vs Design

- Software architecture is always about design, but design is not always about architecture;

- Architecture:
    - High level;
    - Big picture;
    - Structure;
    - Components;
    - Relationships;
    - Patterns;
    - Decisions;

- Design:
    - Low level;
    - Details;
    - Implementation;
    - Classes;
    - Methods;
    - Functions;
    - Variables;

### Structures

- Conectors and components (ports and adapters);
- Modules;
- Allocation;

### Middle out (start with the core)

- Focus on the development of the core and most critical components of a software;
- Provides flexibility, allowing changes that do not affect the core of the system;
- Incremental development;

### Architectural Dimensions

- Multidimensional architecture:
    - Technical:
        - Technology;
        - Frameworks;
        - Components;
        - Libraries;
        - Tests;
        - Abstractions;
    - Data:
        - Storage;
        - Formats;
        - Models;
        - Traffic;
        - Sinchronization;
    - Security:
        - Authentication;
        - Authorization;
        - Encryption;
        - Certificates;
        - Tokens;
        - Policies;
        - Proxy;
        - Logs;
    - Operation:
        - Deploy;
        - Provisioning;
        - Monitoring;
        - Logging;
        - Metrics;
        - Scaling;
        - Resilience;
        - Tests;

- Fitness functions:
    - It's a mechanism to measure and accompany what is important to the evolution of the architecture with the time;
    - It's about measuring and accompany elements of an architecture over time, elements like:
        - Auditibility;
        - Performance;
        - Security;
        - Data;
        - Legality;
        - Scalability;
    - Is important to define the critical aspects of the architecture and to define the metrics to measure them;
    - TDR: Technical Debit Ratio;
    - Consolidation: is a technique to understand which points of improvement you consider most important to measure your fitness functions;

   


