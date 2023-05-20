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

