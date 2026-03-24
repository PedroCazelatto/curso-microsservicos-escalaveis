# Curso sobre Microsserviços Escaláveis

Curso sobre microsserviços escaláveis da RocketSeat

## Teoria

Microsserviços são:

- Serviços implantados independentemente
- modelos de arquitetura
- Arquitetura de infraestrutura, não de código

O maior erro em separar microsserviços é separar por módulos, e não por linguagem de negócio

### Vantagens dos microsserviços

1. Infraestrutura específica por necessecidade de serviço
2. Linguagem, banco de dados, ferramentas específicas por necessidade
3. Escalabilidade direcionada
4. Desenvolvimento paralelo em grandes times

### Desvantagens dos microsserviços

1. Replicação de dados com consistência eventual
2. Overhead operacional (qualquer configuração precisa ser replicada)

## Glossário

### Message Broker

Sistema de mensageria assíncrono (RabbitMQ ou Kafka)

### API Gateway

Aplicação que vive entre o frontend e todos os microsserviços
Como se fosse um BFF

### Distributed Tracing

Criação de um traceId na primeira requisição e trafegado junto com todas as mensagens até o fim do processamento

### Idempotência

Forma de evitar que uma requisição seja processada mais de uma vez em caso de falhas

### SAGA pattern

Transações que contemplam múltiplos serviços devem ser quebradas em micro-transações

### Circuit Breaker

Proxy que valida se o próximo microsserviço está disponível antes de enviar as requisições, como um rate-limitter interno a aplicação

### BFF (Backend For Frontend)

Serviço que unifica requisições de vários serviços para um único retorno ao frontend
Recomendação do Diego: GraphQL
