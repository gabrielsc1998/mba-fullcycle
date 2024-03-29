## MBA Full Cycle - Patterns of Enterprise Application Architecture

- Base: https://martinfowler.com/books/eaa.html
- There are many patterns that can be used to solve problems in software development;

- Layering:
    - Separation of responsibilities;
    - Abstration;
        - how much more abstract, more complex, but more flexible (in general);
        - how much coupling, more complex and less flexible;
    - Layer vs Tier:
        - Layer:
            - Logical separation;
            - Ex: Presentation, Business, Data;
        - Tier:
            - Physical separation;
            - Ex: Web, Application, Database;
    - 3 layers architecture:
        - Layers:
            - Presentation:
                - User interface;
                    - Ex: Web, Mobile, Desktop;
                - Formats:
                    - Ex: HTML, JSON, XML;
            - Domain:
                - Business rules;
                    - Ex: Business rules, Business services;
            - Data:
                - Data persistence;
                    - Ex: Database, File, Cache;
                - Message:
                    - Ex: Kafka, RabbitMQ;
        - Flux: Presentation -> Domain -> Data -> Domain -> Presentation;
            - Domain and data should never depend on presentation;
            - If domain depends on presentation, it will generate instability in the core of the system;
    - Transaction script:
        - Each request is a script;
        - Each script is a transaction;
        - advantages:
            - Simple;
            - Easy to understand;
            - Easy to implement;
        - disadvantages:
            - Difficult to maintain;
            - Difficult to reuse;
            - Difficult to test;
    - Domain model:
        - The domain of the application is divided into objects;
        - The bussiness rules are in the objects (encapsulated);
        - advantages:
            - Easy to maintain;
            - Easy to reuse;
            - Easy to test;
        - disadvantages:
            - Initial complexity;
            - Difficult to understand;
            - Difficult with scale and performance;
    - Table module:
        - Each module is a table in the database;
        - advantages:
            - Simple;
            - Easy to map;
            - Easy to maintain;
            - Easy to do CRUDs;
        - disadvantages:
            - High coupling with the database;
            - Duplication of code;
            - Low reuse;
    - Service Layer:
        - Intermediate layer between the presentation and the domain;
        - Expose functionalities of high level for the clients;
            - clients: presentation, other services, etc;
        - There are a defined interface;
        - Encapsulates the business rules;
        - Organizes the order of execution of the operations;
        - Has access to the data layer;
    - Gateway:
        - Objects that encapsulate access to external systems;
        - Row Data Gateway:
            - Each row in the database has a gateway;
            - Ex: ORM;
        - Table Data Gateway:
            - Each table in the database has a gateway;
            - Ex: DAO;
    - Active Record:
        - An object that encapsulates access to the database and the business rules;
        - Used by many frameworks like Django, Rails, etc;
        - There is a coupling between the object and the database;
    - Data mapper:
        - An object that encapsulates access to the database and does a interface between the domain object and the database;
    - Atomicity:
        - The transaction must be atomic;
        - If an error occurs, the transaction must be rolled back;
    - Unit of work:
        - Object that encapsulates the transaction;
        - It is responsible for managing the transaction;
        - There are some methods like:
            -  registerNew();
            -  registerDirty();
            -  registerClean();
            -  registerRemoved();
            -  commit();
            -  rollback();
    - Identity map:
        - Object that stores the objects that have already been loaded;
        - If the object is already loaded, it is not necessary to load it again;
        - It is used to avoid duplication of objects;
    - Repository:
        - Object that encapsulates access to the database;
        - Receives a domain object and returns a domain object;
        - Usually does different combinations by especifications;