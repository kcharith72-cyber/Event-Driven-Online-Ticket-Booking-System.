# Event-Driven Online Ticket Booking System

An event-driven, cloud-native online ticket booking platform built using **Spring Boot, Spring Cloud, Apache Kafka, Docker, and Kubernetes**.  
The system demonstrates how modern microservices architectures can achieve **scalability, resilience, and fault isolation** during high-traffic booking scenarios.

---

## Project Overview

Traditional ticket booking systems are often monolithic, tightly coupled, and difficult to scale during peak demand events such as movie releases, concerts, or airline flash sales.  
This project solves these challenges by implementing an **event-driven microservices architecture** where each service owns its domain and communicates asynchronously using Apache Kafka.

The system supports:
- Seat reservation with timeout handling
- Asynchronous payment processing
- Dynamic pricing
- Real-time notifications
- Independent deployment and scaling of services

---

## System Architecture

The platform is composed of **five autonomous microservices**, each with its own database, configuration, and deployment lifecycle:

| Service | Responsibility |
|-------|----------------|
| Booking Service | Handles ticket booking requests and booking lifecycle |
| Seat Inventory Service | Manages seat availability and reservations |
| Payment Service | Processes payments asynchronously |
| Pricing Service | Calculates dynamic ticket pricing |
| Notification Service | Sends booking and payment notifications |

Services communicate via **Apache Kafka event streams**, ensuring loose coupling and fault isolation.

---

## Event-Driven Workflow

1. Customer initiates a ticket booking
2. Booking Service publishes a `BookingCreated` event
3. Seat Inventory Service reserves seats and emits a `SeatsReserved` event
4. Pricing Service calculates final price
5. Payment Service processes payment asynchronously
6. Notification Service sends confirmation or failure messages
7. Seats are released automatically if payment times out

---

## Key Features

-  Event-driven microservices using Apache Kafka  
-  Asynchronous seat reservation & payment processing  
- Fault isolation and resilience using Resilience4j  
- Centralized configuration management  
- API Gateway with JWT authentication  
- Distributed tracing and observability  
- Containerized deployment using Docker  
-  Kubernetes orchestration with Helm  
- CI/CD pipeline using GitHub Actions  

---
