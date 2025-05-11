# Event-Driven Order Management System

## 🧾 Project Title: **Event-Driven Order Management System (OMS)**

---

## 📌 Summary
This Event-Driven Order Management System is designed to handle complex order lifecycles with high scalability, resiliency, and extensibility. It uses **Domain-Driven Design (DDD)** principles, **Event Sourcing**, and **CQRS** patterns to ensure separation of concerns and traceability. The system is built using **Java (Spring Boot)** and leverages **Apache Kafka** for asynchronous messaging between bounded contexts.

---

## 🚀 Features

### ✅ Core Functionalities
- **Place Order**: Handles new orders with validation and persistence.
- **Order Fulfillment**: Orchestrates payment, inventory, and shipping.
- **Saga Pattern**: Coordinates distributed transactions with rollback.
- **Event Replayability**: Recover read models from stored events.
- **Audit Trail**: Immutable event store for compliance and debugging.

### 🔁 Event Types
- `OrderPlacedEvent`
- `PaymentProcessedEvent`
- `InventoryReservedEvent`
- `OrderShippedEvent`
- `OrderCompletedEvent`
- `OrderFailedEvent`

### ⚙️ Architecture
- Microservices: Order, Payment, Inventory, Shipping, Notification
- Kafka Topics: per event type or aggregate
- Event Store: PostgreSQL or Kafka log retention
- Projections: MongoDB for query side (CQRS)

---

## 🏗️ Tech Stack
- **Java 21**, **Spring Boot 3**
- **Apache Kafka** for messaging
- **MongoDB** for read models
- **PostgreSQL** for event store
- **Docker** and **Docker Compose** for local development
- **Swagger / OpenAPI** for API docs
- **Testcontainers** for integration testing
- **Prometheus + Grafana** for observability

---

## 🧠 Design Principles
- **Domain-Driven Design (DDD)** with Aggregates, Entities, Value Objects
- **CQRS**: Separate read/write models
- **Event Sourcing**: Persist state transitions as events
- **Saga Orchestration**: Using state machine or orchestrator pattern
- **Idempotent Consumers**: Safe event re-processing

---

## 📦 Modules
```bash
/order-service
/payment-service
/inventory-service
/shipping-service
/notification-service
/common-library
/docker-compose.yml
/kafka-setup
```

---

## 🧪 Test Strategy
- Unit tests for Aggregates and Event Handlers
- Integration tests with Kafka Testcontainers
- Contract testing for service APIs

---

## 📈 Observability
- Kafka Consumer Lag Monitoring
- Prometheus Metrics (event throughput, saga failures, retries)
- Grafana Dashboards (order latency, failure trends)



## 📸 Screenshots (Optional)
- Architecture Diagram
- Kafka Topic View
- Sample Event Flow in Grafana

---



---

## 🧩 Future Enhancements
- Add GraphQL API for querying across services
- Implement outbox pattern for reliable event publishing
- Add retry and DLQ (Dead Letter Queue) for failed events
- Role-based Access Control (RBAC)

---

## 🔗 License
MIT

---
