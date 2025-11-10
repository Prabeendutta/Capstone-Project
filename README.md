---

# E-Commerce Backend Platform

This project is a **scalable E-Commerce Backend** built using **Spring Boot, MySQL, MongoDB, Redis, and Elasticsearch**, following **clean microservices architecture principles**.

---

## Project Overview

The goal of this project is to develop a **high-performance backend** system for an e-commerce platform, handling core functionality such as:

- User Registration and Authentication
- Product Browsing and Search
- Shopping Cart Management
- Order Placement and Tracking
- Secure Payment Processing
- Real-Time Notifications

While designed for microservices, this submission implements a modular monolithic structure, keeping future decoupling into microservices in mind.

---

## 🛠 Technologies Used

- **Spring Boot** — Java backend framework
- **MySQL** — Relational database (users, products, orders)
- **MongoDB** — Flexible cart management
- **Redis** — Caching frequently accessed data
- **Elasticsearch** — Fast product search
- **Swagger / SpringDoc** — API documentation
- **Docker (Optional)** — Running MongoDB and Redis containers
- **AWS (Planned)** — Deployment architecture for EC2, RDS, Elastic Beanstalk

---

## Modules Implemented

| Module | Functionality |
|:------|:--------------|
| **User Management** | Registration, Login, Profile Management |
| **Product Catalog** | Browse products, View details, Search |
| **Cart Management** | Add to cart, Remove, View cart summary |
| **Order Management** | Checkout, Place orders, Track orders |
| **Payment Management** | Payment gateway simulation, Order payments |
| **Notifications** | Confirmation emails/messages on events |

---

## Security

- JWT-based Authentication and Authorization
- Secure Password Encoding with BCrypt
- Role-based Access Control
- Session expiration and token management

---

## Search

- Full-text and typo-tolerant product search using **Elasticsearch**
- Optimized indexes for fast response times (~100 ms average)

## API Documentation

- **Swagger UI** can be enabled at:
- http://localhost:8080/swagger-ui.html
- Automatically generated from controller annotations.
- Supports API testing from browser.

## Future Improvements

- Separate services into independent deployable **microservices**
- Introduce Kafka-based **Event-Driven Architecture** (order events, payment success)
- Integrate AWS services fully (EC2, RDS, ElasticCache, MSK)
- Implement CI/CD pipelines using GitHub Actions or AWS CodePipeline
- Add frontend UI for user interactions

---

## System Architecture (Designed)

- Spring Boot REST APIs
- MySQL → User, Product, Order, Payment Data
- MongoDB → Dynamic Cart Data
- Redis → Cache layer for cart and popular products
- Elasticsearch → Product Search
- Kafka → Event communication (future scope)
- AWS → Deployment (future scope)

---

## Developer

**Prabeen Dutta**  
M.Sc. Computer Science (Scaler Neovarsity - Woolf)  
Email: `prabeendutta@gmail.com`

Supervisor: **Naman Bhalla**

---

## License

This project is a part of academic submission and intended for educational use.

---


## Sample application.properties (Not included for security reasons)

# ================================
# Database Configuration (MySQL)
# ================================
spring.datasource.url=jdbc:mysql://localhost:3306/{your-mysql-database-name}
spring.datasource.username={your-mysql-username}
spring.datasource.password={your-mysql-password}
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

# ================================
# JPA and Hibernate Configuration
# ================================
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

# ================================
# MongoDB Configuration (Cart Data)
# ================================
spring.data.mongodb.uri=mongodb://localhost:27017/{your-mongodb-database-name}
spring.data.mongodb.database={your-mongodb-database-name}

# ================================
# Redis Configuration (Cache Layer)
# ================================
spring.data.redis.host=127.0.0.1
spring.data.redis.port=6379

# ================================
# Elasticsearch Configuration (Product Search)
# ================================
spring.elasticsearch.uris=http://localhost:9200
spring.elasticsearch.username={your-elasticsearch-username}
spring.elasticsearch.password={your-elasticsearch-password}

# ================================
# Server Configuration
# ================================
server.port=8080
spring.application.name={your-application-name}

# ================================
# Swagger / Springdoc OpenAPI
# ================================
springdoc.api-docs.path=/api-docs
springdoc.swagger-ui.path=/swagger-ui.html

---
