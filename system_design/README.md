## MBA Full Cycle - System design and Design Docs

### System Design

- Definition: is the process of defining the architecture, modules, interfaces, and data for a system to satisfy specified requirements.
- Importance:
  - it's the process of intentionally thinking about architecture;
  - it's the process of thinking about the definitions that really matter;
  - it's the process of exploring possible solutions;
  - it's the process of thinking about the present and the future of the software;
  - exercise the way of thinking about different software solutions;
- Techniques and methodologies:
  - understand the problem and requirements;
  - estimate the capacity:
    - throughput, latency, storage, etc;
  - data modeling:
    - helps to define the database;
  - API design:
    - helps to define the main functionalities;
  - system design:
    - helps to define the architecture;
  - exploration:
    - helps to define the best solution from the confrontation on the justification of the choices;
- Requirements:
  - core features:
    - the domain of the application and the main functionalities;
  - support features:
    - the features that support the core features;
  - functional requirements:
    - what the system should do (features and functionalities);
  - non-functional requirements:
    - how the system should do (components, architecture, etc);
  - constraints:
    - what the system can't do;

## Practical example

- Problem: a system to send tickets to events;
- Functional Requirements:

  - Core functionalities:
    - buy a ticket;
    - show the ticket to get access to the event;
    - partners to manage the events;
  - Support functionalities:
    - payment (split payment);
    - search events;
    - graphical exibition of available seats/places;
    - guarantee that a ticket is not sold to more than one person;

- Non-Functional Requirements:

  - characteristics (CAP theorem):
    - low latency;
    - high availability;
    - scalable;
    - data consistency;
  - important data (we need of data or estimates to make the system design):
    - DAU (daily active users) - one million;
    - each user will do 5 requests;
    - each request will result in 50KB of data;
    - 5% of the users buy ticket (convertion rate);
    - read/write ratio: 90/10;
    - may have peak hits;
  - calcs:
    - 1M (DAU) * 5(requests) = 5M (5*10^6) requests per day;
    - we will assume that a day has 100.00 (10^5) seconds, for calculation purposes;
    - 5*10^6 / 10^5 = 5*10^(6-5) = 5\*10^1 = 50 requests per second (rps);
    - shopping per day -> 5% of 1M = 5*10^4 shoppings per day;
    - shopping per seconds -> 5*10^4 / 10^5 = 0.5 shoppings per second;
    - bandwidth = 50rps * 50kb = 2.500Kb/s = 2.5Mb/s;

- CAP theorem:

  - Consistency: all nodes see the same data at the same time;
  - Availability: every request receives a response, without the guarantee that it contains the most recent write;
  - Partition tolerance: the system continues to operate despite an arbitrary number of messages being dropped;
  - Theorem: it's not possible to have all three guarantees at the same time;
  - Solution: choose two of the three guarantees;

- Eventual consistency:

  - it's a consistency model that allows the system, eventually, have duplicate data, for a period of time, but, when the central system realizes the duplicity, it takes action;

- Capacity plan (Exercise):

![Capacity plan](./img/capacity-plan.png "Capacity plan")
  