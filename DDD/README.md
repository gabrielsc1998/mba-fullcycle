## MBA Full Cycle - Domain Driven Design

- In DDD, a domain is a sphere of knowledge;
- DDD has a goal to modelate the domain for complex situations;

- When/Why use?
    - According the Conway's law, the software architecture reflects the communication structure of the organization that created it;
    - Bigs organizations with many teams (thinking about software) tend to divide the software in many domains, the famous microservices;
    - DDD is a good choice to modelate the domain of each microservice, because DDD is contextual and each microservice is a context (bounded contexts);

- Ubiquitous Language:
    - DDD is contextual, so, there so many different contexts (domains - spheres of knowledge) and each one has its own language;
    - The language used in the domain should be the same used in the code and in the documentation;

- Bounded Context:
    - A bounded context is a space that has its own language (ubiquitous language) and models;
    - It's a space in a big and complex "problem" that have things in common and cover an area of ​​knowledge;
    - Bounded contexts have a loose coupling;

- Domain:
    - Is a sphere of knowledge;
    - Is a space of a problem;

- Subdomain:
    - Is a part of a domain;
    - Is a space of a problem;

    - Types of subdomain:
        - Core Domain:
            - is a subdomain that has primary importance for the organization;
            - must be implemented perfectly, as it provides a business advantage;
        - Supporting Domain:
            - important aspects of the business, but not the core;
            - suports the core domain;
        - Generic Domain:
            - is a subdomain that has no strategic importance for the organization;

- Context Mapping:
    - Is a technique to map the bounded contexts and their relationships;
    - Types of relationships:
        - Partnership:
            - is a relationship between two bounded coordinated in an ad hoc manner;
            - example: a team can notify a second one about a change in the API, and the second team will cooperate and adapt, without conflicts;
        - Shared Kernel:
            - is a relationship between two bounded contexts that share an at least a model;
            - can be have some problems, because can be conflicts in the model between the teams;
            - example: a team can use a model from another team;
        - Customer-Supplier:
            - is a relationship between two bounded contexts that one is the customer of the other;
            - the suplier is the upstream and of the customer and the customer is the downstream of the supplier;
            - in general, the downstream has to wait the upstream to make changes;
            - in general, they provide an interface to allow the communication;
            - example: one team consume an API from another team;
        - Conformist:
            - is a customer-supplier relationship, but the upstream model is complex;
            - in general, the downstream has to conform to the upstream as it is;
            - example: a team can use a third party API, but the team can't change the API;
        - Anticorruption Layer:
            - is a layer that protects the bounded context from a third party bounded context;
            - example: a team can use a third party API, but the team can't change the API, so, the team can create an anticorruption layer to protect the bounded context of possible changes in the third party API or until the change o third party API for a new one;
        - Open Host Service:
            - is a integration style as a relationship where there is one upstream and many downstreams;
            - example: a team can provide an API to many teams;
        