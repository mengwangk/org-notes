# Microservice

## [Handling distributed transactions](https://medium.com/swlh/handling-transactions-in-the-microservice-world-c77b275813e0)
- How to keep transactions atomic
- How do handle concurrent requests

Possible Solutions
- 2pc - 2-phase commit
- Eventual consistency and compensation / SAGA

### 2pc 
- 2 stages - prepare and commit phase. Transaction Coordinator maintains the lifecyle of transaction.
- Synchronous call where the client would be notified of success or failure.
- Is slow and highly dependent on transaction coordinator.
- Locking of database rows. Possible deadlock.

### Eventual consistency and compenstation / SAGA
- Each service publishes an event whenever it updates its data. Other service subscribe to events. When an event is received, a service updates its data.
- distrbuted transaction is fulfilled by async local transactions on related microservice. The microservices communicate with each other through an event bus.
- Use Compensating Transaction
- Async event based solution.
- Advantage - each microservice focuses only on its own atomic transaction. Microservices are not blocked if another service is taking a longer time. No db lock required.
- Disadvantages - does not have read isolation. Client sees order created and removed. harder to debug and maintain when number of microservices increase.

First alternative - avoid needing distributed transactions.  If a new app,
start with a monolith

A more common approach is to start with a monolith and gradually peel off
microservices at the edges. Such an approach can leave a substantial monolith
at the heart of the microservices architecture, but with most new development
occurring in the microservices while the monolith is relatively quiescent. —
Martin Fowler

Eventual Consistency and Compensating is preferred over 2pc. Main reason 2pc
does not scale in a distributed environment. SAGA also introduces a new set of
problems, such as how to atomically update the db and emit and event. Adoption
of this approach requires a change in mindset for both development and testing
teams.


