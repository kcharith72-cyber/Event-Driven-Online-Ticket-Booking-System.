event-driven-ticket-booking/
├── README.md                          # Project overview and setup guide
├── pom.xml                            # Parent Maven POM with dependency management
│
├── eureka-server/                     # Service Discovery Server
│   ├── pom.xml
│   ├── src/main/java/...
│   └── src/main/resources/
│
├── config-server/                     # Centralized Configuration Server
│   ├── pom.xml
│   ├── src/main/java/...
│   └── src/main/resources/
│
├── api-gateway/                       # API Gateway with routing & JWT authentication
│   ├── pom.xml
│   ├── src/main/java/...
│   └── src/main/resources/
│
├── booking-service/                   # Ticket Booking Microservice
│   ├── pom.xml
│   ├── src/main/java/...
│   └── src/main/resources/
│
├── seat-inventory-service/            # Seat Inventory & Reservation Microservice
│   ├── pom.xml
│   ├── src/main/java/...
│   └── src/main/resources/
│
├── payment-service/                   # Payment Processing Microservice
│   ├── pom.xml
│   ├── src/main/java/...
│   └── src/main/resources/
│
├── pricing-service/                   # Dynamic Pricing & Offers Microservice
│   ├── pom.xml
│   ├── src/main/java/...
│   └── src/main/resources/
│
├── notification-service/              # User Notification Microservice
│   ├── pom.xml
│   ├── src/main/java/...
│   └── src/main/resources/
│
├── docker-compose.yml                 # Local development stack (Kafka, services)
│
├── kubernetes/                        # Kubernetes deployment manifests
│   ├── booking-deployment.yml
│   ├── inventory-deployment.yml
│   ├── payment-deployment.yml
│   ├── pricing-deployment.yml
│   ├── notification-deployment.yml
│   ├── gateway-deployment.yml
│   ├── service.yml
│   └── configmap.yml
│
├── helm-charts/                       # Helm charts for production deployment
│   └── event-driven-ticket-booking/
│       ├── Chart.yaml
│       ├── values.yaml
│       └── templates/
│
├── .github/workflows/                 # GitHub Actions CI/CD pipeline
│   └── build-and-test.yml
│
├── docs/                              # Project documentation
│   ├── architecture.md
│   ├── event-flow.md
│   ├── kafka-topics.md
│   └── api-specs.md
