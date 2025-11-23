# 🛒 E-Commerce Platform — Spring Boot Microservices Architecture

## 📌 Overview

This project is a distributed **E-Commerce platform** designed using **Spring Boot** and a complete **Spring Cloud Microservices architecture**.  
The system is fully modular, scalable, and based on domain-driven separation.  
Several microservices communicate synchronously through REST APIs and asynchronously through **Apache Kafka** for event-driven workflows.

The architecture aims to provide high scalability, resilience, maintainability, and cloud-native deployment readiness.

---

## 🧩 Microservices Overview

### **Core Business Microservices**

- **Client Service** – Manages customers and authentication with JWT.
- **Product Service** – Handles product information and product metadata.
- **Catalog Service** – Manages product categories and catalog structure.
- **Inventory Service** – Real-time stock tracking with Kafka events.
- **Cart Service** – Shopping cart logic and state synchronization.
- **Order Service** – Creation and management of customer orders.
- **Payment Service** – Processes payments and transaction validation.
- **Notification Service** – Sends email/SMS notifications for orders and updates.

---

## 🧱 Infrastructure Microservices (Spring Cloud)

### **Config Server**

Centralized configuration management for all microservices.  
Configurations are externalized and version-controlled.

### **Eureka Server**

Service registry managing dynamic service discovery.  
All microservices register automatically.

### **API Gateway**

Single entry point for all external clients.  
Handles routing, load balancing, filters, security, and request management.

### **Resilience4j**

Provides:

- Circuit breakers
- Retry mechanisms
- Rate limiting
- Fallback strategies

Ensures microservice resilience under heavy load or partial failure.

---

## 🔁 Communication Model

### **Synchronous (REST)**

Used for:

- Product information
- Cart updates
- Authentication
- Catalog browsing

### **Asynchronous (Kafka)**

Used for:

- Stock reservation and updates
- Order lifecycle events
- Notification triggers
- Payment events

This event-driven approach improves scalability and decoupling between microservices.

---

## 🛠️ Tech Stack

### **Backend**

- Spring Boot
- Spring MVC
- Spring Data JPA
- Spring Security + JWT
- Lombok

### **Spring Cloud**

- Config Server
- Eureka Discovery
- Spring Cloud Gateway
- OpenFeign
- Actuator
- Resilience4j

### **Messaging**

- Apache Kafka

### **Databases**

- MySQL / PostgreSQL
- One database per microservice following the **database-per-service** pattern

---

## 🧰 DevOps & Deployment

### **Containerization**

All microservices include Docker configurations.  
Images are built and orchestrated consistently across environments.

### **Orchestration**

The platform supports deployment on **Kubernetes**, including:

- Deployments
- Services
- Ingress
- ConfigMaps
- Secrets

Microservices are designed to run seamlessly in distributed cloud environments.

### **CI/CD**

Pipeline includes:

- Build automation  
- Testing  
- Docker image creation  
- Deployment to Kubernetes  
- Monitoring & alerting integration  


---

## 📈 Observability

### **Monitoring**

- **Prometheus** for metrics collection
- **Grafana** dashboards for microservice health visualization

### **Logging**

Optional integration with:

- Loki
- ELK Stack (Elasticsearch, Logstash, Kibana)

Provides a centralized log management layer for the entire platform.

---

## 📁 Project Structure
```
ecommerce-spring-microservices/
│
├── config-server/
├── eureka-server/
├── api-gateway/
│
├── client-service/
├── product-service/
├── catalog-service/
├── inventory-service/
├── cart-service/
├── order-service/
├── payment-service/
├── notification-service/
│
├── kafka/
├── docker/
├── k8s/
├── monitoring/
│   ├── prometheus/
│   └── grafana/
│
└── README.md
```

---

## ⭐ Key Features

- Spring Boot Microservices
- Centralized configuration
- Dynamic service discovery
- API Gateway abstraction
- Asynchronous communication with Kafka
- Resilience4j patterns
- Domain-driven decomposition
- Docker & Kubernetes orchestration
- Monitoring with Prometheus & Grafana
- Production-ready microservices architecture

---


