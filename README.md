# Patient Management System (Microservices)

## 📖 Overview
A **Spring Boot microservices-based Patient Management System** designed with modern software architecture principles. Each service is an independent Spring Boot application that can be developed, deployed, and scaled separately.

## 🚀 Features
- **Patient Service**: Manages patient registration, profiles, and medical data
- **Billing Service**: Handles billing, invoicing, and payment processing
- **Microservices Architecture**: Independent, loosely coupled services
- **Docker Containerization**: Easy deployment and scalability
- **RESTful APIs**: Clean, well-documented API endpoints



## 🏗️ Architecture


## 🧩 Services Overview

| Service | Description | Port | Health Check |
|---------|-------------|------|--------------|
| **patient-service** | Manages patient registration & medical data | 8081 | `http://localhost:8081/actuator/health` |
| **billing-service** | Handles billing & invoicing operations | 8082 | `http://localhost:8082/actuator/health` |

## 📋 Prerequisites

- **Java 17** or later
- **Maven 3.6+**
- **Docker** & **Docker Compose** (optional, for containerized deployment)
- **Git** for version control

## 🛠️ Installation & Setup

### 1. Clone Repository
```bash
git clone https://github.com/Pradeep717/PatientManagement.git
cd PatientManagement

```

## 🧩 Available Services

| Service Name     | Description                          | Port |
|------------------|--------------------------------------|------|
| patient-service  | Manage patient registration & data   | 8081 |
| billing-service  | Handle billing & invoicing            | 8082 |

---

## 🔗 GitHub Repository
https://github.com/Pradeep717/PatientManagement.git

---

## 🌿 Branching Strategy (Git Flow – Simple)

- **main** → Production-ready stable code
- **develop** → Active development
- **feature/*** → New features
  - Example: `feature/patient-api`
- **bugfix/*** → Bug fixes
  - Example: `bugfix/billing-calculation`

### Create a feature branch
```bash
git checkout develop
git checkout -b feature/patient-service

git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/Pradeep717/PatientManagement.git
git push -u origin main

# Create a feature branch
git checkout develop
git pull origin develop
git checkout -b feature/patient-api

# Work on feature, then:
git add .
git commit -m "Add patient registration API"
git push origin feature/patient-api

# Merge to develop (after PR approval)
git checkout develop
git merge --no-ff feature/patient-api
git push origin develop


### 1. Docker Build Instructions
```bash

# Patient Service
cd patient-service
docker build -t patient-service:latest .

# Billing Service
cd billing-service
docker build -t billing-service:latest .

# Patient Service
docker run -p 8081:8081 patient-service:latest

# Billing Service
docker run -p 8082:8082 billing-service:latest

docker-compose up --build

```
### 3. Run Services
```bash
# Patient Service
cd patient-service
mvn spring-boot:run

# Billing Service
cd billing-service
mvn spring-boot:run
```
### 2. Maven Build Instructions
```bash
# Patient Service
cd patient-service
mvn clean install

# Billing Service
cd billing-service
mvn clean install
```
### 4. Access APIs
- Patient Service: `http://localhost:8081/api/patients`
- Billing Service: `http://localhost:8082/api/billing`
- Health Checks:
  - Patient Service: `http://localhost:8081/actuator/health`
  - Billing Service: `http://localhost:8082/actuator/health`
  
## 🛠️ Technologies Used
- Spring Boot
- Spring Data JPA
- Spring Web
- Maven
- Docker
- Docker Compose
- H2 Database (in-memory for development)
- Java 17
- Git
- GitHub
- RESTful APIs
- Actuator
- JUnit & Mockito
- Lombok
- Swagger/OpenAPI
- Logback
- Flyway
- Postman





