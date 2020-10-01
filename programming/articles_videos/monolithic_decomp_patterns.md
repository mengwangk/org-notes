# [ Monolith Decomposition Patterns ](https://www.youtube.com/watch?v=9I9GdSQ1bbM&t=5s)

- Single process monolith
- Modular monolith
- 3rd party monolith - e.g. SAAS product. Limited ability to change
- Distributed monolith - high cost of change.. larger scoped deployment...more to go wrong.. release
    coordination

You won't appreciate the true horror, pain and suffering of microservices until you are running
them in production.

**Migration Patterns**

HTTP Proxy
- Wrapping the service

Branch by abstraction
- Create abstraction point
- Start work on new service implementation
- Switch over
- Clean up
- Composite abstraction
  - existing implementation
  - new service calling implementation

Parallel Run
  - https://github.com/github/scientist

Our new service needs data
- directly access the data... but coupling... for short period of time is okay for code extraction.
- Use APIs to access the db.. make sense if data belongs to the monolith.
- Monolith needs to be changed to source data from the new service, if data belongs to the new
    service.

Database Refactoring

Join across tables
- Use REST to pull the data, e.g. /item/123
- No referential integrity.. use soft delete
- More network hops - latency can suffer
- Lost enforcement of data consistency

Splitting tables
- CAP theory - in partition you have to trade off between consistency and availability...

