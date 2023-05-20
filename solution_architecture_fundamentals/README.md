## MBA Full Cycle - Solution Architecture Fundamentals

- Scalability;
- Availability;
- Security;
- Customization / Modularization;
- Integration;
- Observability;

### Layers of Solution Architecture:

1. Business;
2. Technical;
3. Deployment;

### SAD (Solution Architecture Document)

- Document that describes the architecture of a solution;
- It usually includes:
    - Components;
    - Modules;
    - Interfaces;
    - Data flow;
- Takes into account the project's context;
- Generated during the project planning phase;
- Provides clarity to those involved about the solution as a whole;
- Serves as a reference for various stakeholders.
- The SAD not necessarily needs to have the same structure for all projects;
- It's documentated what is important/relevant for the project;
- The greater the risk of the project, the greater the documentation;

- Structure:
    - Introduction:
        - Purpose of the document;
        - Scope of the solution;
        - Restrictions;
        - Assumption;
    - Architecture overview:
        - Descriptive with main points;
        - High-level diagram;
        - Main components;
        - Flow diagrams;
    - Requirements:
        - Functional
            - Resources, functionalities, features that add value to the business;
        - Non-functional
            - Ex: Performance, scalability, security, availability + cross-cutting;
    - Architecture design:
        - Detailed diagrams as well as their description;
        - Technologies to be used;
        - Integration between systems;
    - Implementation:
        - Development methodologies and tools;
        - Deployment processes and infrastructure;
        - Testing and quality processes;
    - Operation and maintenance:
        - Monitoring;
        - Maintenance processes;
        - Disaster recovery;
        - Change management process;
    - Risks and mitigation strategies:
        - Potential risks;
        - High impact risks;
        - Contingency plans;
    - Costs, technology and personnel:
        - Cost estimate for implementation;
        - Recommendation of teams and personnel;
        - It is the responsibility of the solution architect to indicate operational and technological costs in the SAD in addition to project aspects;
    - Next steps
        - Execution order suggestion;
        - General observations;

### Lehmans Laws

- Laws that describe the evolution of software systems;
- The laws are based on the observation of the evolution of software systems;

    1. Law of Continuing Change
        - A software system must change or become progressively less useful in a changing environment;
    2. Law of Increasing Complexity
        - As a software system evolves, its complexity increases unless work is done to maintain or reduce it;
    3. Law of Self-Regulation
        - Software evolution is a self-regulating process. Software evolution processes are feedback systems that maintain an equilibrium state expressed in terms of a measure of the software;
    4. Law of Conservation of Organizational Stability
        - The average effective global activity rate in a large system is invariant over the lifetime of the system;
    5. Law of Conservation of Familiarity
        - The incremental change in each release of a software system is roughly constant for a given system;
    6. Law of Continuing Growth
        - The functional content of a software system must be continually increased to maintain user satisfaction over its lifetime;
    7. Law of Declining Quality
        - The quality of a software system will appear to be declining unless it is rigorously maintained and adapted to operational environment changes;
    8. Law of Feedback System
        - Software evolution processes are multi-level, multi-loop, multi-agent feedback systems and must be treated as such to achieve significant improvement over any reasonable base;

### Coupling

- afferent: incoming (more stable);
- efferent: outgoing (less stable because it depends on the afferent);