# releaseflow-devops-release-management-platform
Enterprise-grade microservices-based DevOps Release Management Platform built with Spring Boot, Spring Cloud Gateway, Eureka, PostgreSQL, H2, JWT Authentication, and Swagger.
# ReleaseFlow – DevOps Release Management Platform

ReleaseFlow is an enterprise-style microservices-based DevOps Release Management Platform designed to streamline software release planning, deployment approvals, environment management, auditing, notifications, and webhook integrations.

This project demonstrates scalable backend architecture using Spring Boot microservices, API Gateway routing, service discovery, JWT authentication, and distributed service communication.

---

## Features

- JWT-based authentication & authorization
- API Gateway routing
- Eureka service discovery
- Release pipeline management
- Deployment execution management
- Environment configuration management
- Approval workflows
- Audit logging
- Notification service
- Webhook integrations
- Swagger API documentation
- PostgreSQL persistence
- H2 in-memory database for lightweight services
- Config Server integration support
- CORS support
- Role-based access preparation

---

## Microservices Architecture

### Core Services

| Service | Port | Purpose |
|--------|------|---------|
| Auth Service | 8081 | User authentication, JWT token generation |
| Pipeline Service | 8082 | Deployment pipeline management |
| Deployment Service | 8083 | Deployment execution workflows |
| Approval Service | 8084 | Approval workflows |
| Audit Service | 8085 | Audit logging |
| Environment Service | 8086 | Environment management |
| Notification Service | 8087 | Notifications |
| Webhook Service | 8088 | Webhook integrations |
| Eureka Server | 8761 | Service discovery |
| API Gateway | 8090 | Central routing |

---

## Tech Stack

### Backend
- Java 21
- Spring Boot 3
- Spring Security
- Spring Cloud Gateway
- Spring Cloud Eureka
- Spring Data JPA
- Hibernate

### Databases
- PostgreSQL
- H2 Database

### Authentication
- JWT

### Build Tools
- Maven

### API Documentation
- Swagger / OpenAPI

---

## Architecture

Client Requests pass through:

API Gateway → Authentication → Microservices → Database

Services register with Eureka for service discovery.

JWT-secured routes are validated through API Gateway filters.

---

## Project Structure

```bash
releaseflow/
│
├── releaseflow-auth-service
├── releaseflow-pipeline-service
├── releaseflow-deployment-service
├── releaseflow-approval-service
├── releaseflow-audit-service
├── releaseflow-environment-service
├── releaseflow-notification-service
├── releaseflow-webhook-service
├── releaseflow-api-gateway
├── releaseflow-eureka-server
└── releaseflow-config-server
