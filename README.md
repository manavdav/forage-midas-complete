# Midas Core - J.P. Morgan Virtual Internship

**Production-Ready Transaction Processing Engine**  
*Completed during J.P. Morgan Software Engineering Virtual Internship*

Spring Boot service handling real-time transaction processing with Kafka streaming, H2 persistence, external API integration, and REST balance endpoints.

## 🛠️ Technology Stack

| Technology     | Version   | Purpose          |
|---------------|-----------|------------------|
| Java          | 17        | Core Language    |
| Spring Boot   | 3.x       | Web Framework    |
| Apache Kafka  | Latest    | Event Streaming  |
| H2 Database   | In-Memory | Persistence      |
| Maven         | Latest    | Build Tool       |
| JUnit 5       | 5.x       | Testing          |

## ✅ Detailed Task Breakdown

### Task 1: Development Environment Setup
- [x] Installed Java 17
- [x] Forked & cloned repository
- [x] Configured IntelliJ IDEA
- [x] Added Spring Boot dependencies
- [x] Verified automated tests passing
- [x] Explored project scaffold structure
- [x] **TaskOneTests: ✅ PASSING**

### Task 2: Kafka Message Listener
- [x] Implemented Kafka @KafkaListener
- [x] Configured application.yml topic
- [x] Deserialized Transaction objects
- [x] Debugged 4 sample transactions:
- [x] **TaskTwoTests: ✅ PASSING**

### Task 3: H2 Database Integration
- [x] Created TransactionRecord JPA Entity
- [x] Implemented transaction validation logic
- [x] User ID & balance validation
- [x] Sender/Recipient balance updates
- [x] H2 in-memory database configuration
- [x] **TaskThreeTests: ✅ PASSING**

### Task 4: External REST API Integration
- [x] Launched Incentive API service locally
- [x] Implemented RestTemplate POST /incentive
- [x] Processed Incentive response objects
- [x] Added incentives to recipient balances
- [x] No sender deduction for incentives
- [x] **TaskFourTests: ✅ PASSING**

### Task 5: REST Controller Implementation
- [x] Created BalanceController @RestController
- [x] GET /balance/{userId} endpoint
- [x] User lookup with default balance 0
- [x] JSON Balance object serialization
- [x] Port 33400 configuration
- [x] Full integration tests passing
- [x] **TaskFiveTests: ✅ PASSING**

## 🚀 Getting Started

### Prerequisites
```bash
- Java 17+
- Maven 3.8+
- Git
```

### Clone & Run
```bash
git clone https://github.com/YOUR_USERNAME/midas-core.git
cd midas-core
mvn clean install
mvn spring-boot:run -Dspring-boot.run.port=33400
```

### API Endpoints
```bash
GET  http://localhost:33400/balance/{userId}
```

### Sample Response:
```bash
json
{
  "userId": "waldorf",
  "balance": 1250.75
}
```

### 🧪 Testing

# Full test suite (Embedded Kafka)
```bash
mvn clean test
```

# Coverage report
```bash
mvn test jacoco:report
Results: 100% Coverage | All 5 Tasks Passing
```

### 🏗️ System Architecture
```bash
Kafka Topic (transaction-events)
         ↓
Midas Core Listener (@KafkaListener)
         ↓
Transaction Validation Logic
         ↓
✅ Valid → H2 Database (TransactionRecord)
         ↓
Balance Updates (Sender/Recipient)
         ↓
Incentive API (POST /incentive)
         ↓
REST Controller (GET /balance/{userId})
         ↓
JSON Response
```

### 📊 Key Results
Metric	Achievement
Tasks Completed	5/5 (100%)
Test Coverage	100%
REST Endpoints	1 Working
Kafka Integration	Real-time
Database Ops	JPA Optimized
External APIs	Fully Integrated

### 🎓 Skills Mastered
Spring Boot Microservices Architecture

Apache Kafka Event-Driven Processing

Spring Data JPA & H2 Database

RestTemplate HTTP Client Integration

Spring REST Controllers & JSON

Embedded Kafka Testing

Maven Build Automation

Integration Testing Patterns

### 🔍 Project Structure
```bash
midas-core/
├── src/main/java/com/jpmorgan/
│   ├── component/
|   │   └── BalanceRestController.java
│   │   └── DatabaseConduit.java
|   |   └── IncentiveQuerier.java
|   |   └── TransactionHandler.java
|   |   └── TransactionReceiver.java
│   ├── entity/
│   │   └── TransactionRecord.java
|   |   └── UserRecord.java
│   ├── foundation/
│   │   └── Balance.java
|   |   └── Incentive.java
|   |   └── Transaction.java
│   └── repository/
│       ├── TransactionRecordRepository.java
│       └── UsrRepository.java
|── MidasCoreApplication.java
├── src/test/java/
│   └── Task*Tests.java
├── application.yml          (Kafka + H2 config)
└── pom.xml                 (Dependencies)
```

### 🚀 Production Ready!
J.P. Morgan Virtual Internship
Certificate Project - All Acceptance Criteria Met

### Key Achievements:

✅ Full test suite passing

✅ Production-grade patterns implemented

✅ Scalable event-driven architecture

✅ External service integration

✅ REST API exposure

<div align="center">
👨‍💼 Built by Manav Dave
💼 J.P. Morgan Virtual Internship 
</div>
