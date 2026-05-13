# ms-java-notification-service

Microserviço responsável pelo envio de notificações do sistema e-commerce.

## Tecnologias
- Java 21
- Spring Boot 4.0.6
- Spring AMQP (RabbitMQ)
- Maven

## Pré-requisitos
- Java 21 instalado
- infra-local rodando (`docker-compose up`)

## Como rodar
```bash
./mvnw spring-boot:run
```

## Porta
Roda na porta `8083`

## Fluxo
1. Consome evento `StockUpdatedEvent` do RabbitMQ
2. Simula envio de notificação ao cliente (log no console)

## Eventos consumidos
| Fila | Evento | Ação |
|---|---|---|
| stock-updated | StockUpdatedEvent | Notifica cliente sobre status do pedido |