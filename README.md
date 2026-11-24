# Scalable Microservices Course

RocketSeat course on scalable microservices

## Theory

Microservices are:

- Independently deployed services
- Architecture models
- Infrastructure architecture, not code architecture

The biggest mistake when splitting microservices is to split them by modules instead of by business language

### Advantages of microservices

1. Infrastructure specific to each service's needs
2. Language, database and tools specific to each need
3. Targeted scalability
4. Parallel development in large teams

### Disadvantages of microservices

1. Data replication with eventual consistency
2. Operational overhead (any configuration has to be replicated)

## Glossary

### Message Broker

Asynchronous messaging system (RabbitMQ or Kafka)

### API Gateway

Application that sits between the frontend and all the microservices
Like a BFF

### Distributed Tracing

A traceId created on the first request and carried along with every message until processing ends

### Idempotency

A way to stop a request from being processed more than once when something fails

### SAGA pattern

Transactions that span multiple services must be broken into micro-transactions

### Circuit Breaker

Proxy that checks whether the next microservice is available before sending requests to it, like a rate limiter inside the application

### BFF (Backend For Frontend)

Service that combines requests to several services into a single response to the frontend
Diego's recommendation: GraphQL
