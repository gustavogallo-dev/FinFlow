# FinFlow

## System Architecture

### Overview

FinFlow follows a client-server architecture, where the frontend communicates with the backend through a RESTful API.

The application is designed to be modular, maintainable, and scalable, following industry best practices and a layered architecture.

---

## Technology Stack

### Frontend

- React
- TypeScript
- Vite
- Tailwind CSS
- React Router
- Axios
- TanStack Query

### Backend

- Java 21
- Spring Boot
- Spring Security
- Spring Data JPA
- JWT Authentication
- Flyway
- Maven

### Database

- PostgreSQL

### Infrastructure

- Docker
- Docker Compose

---

## High-Level Architecture

```text
┌─────────────────────┐
│      Frontend       │
│  React + TypeScript │
└──────────┬──────────┘
           │ HTTP / HTTPS
           ▼
┌─────────────────────┐
│    REST API         │
│    Spring Boot      │
└──────────┬──────────┘
           ▼
┌─────────────────────┐
│ Business Services   │
└──────────┬──────────┘
           ▼
┌─────────────────────┐
│   Data Access       │
│ Spring Data JPA     │
└──────────┬──────────┘
           ▼
┌─────────────────────┐
│    PostgreSQL       │
└─────────────────────┘
```

---

## Backend Architecture

The backend follows a layered architecture.

```text
Controller
    ↓
Service
    ↓
Repository
    ↓
Database
```

### Controller

Handles HTTP requests and responses.

Responsibilities:

- Receive requests
- Validate input
- Return HTTP responses

---

### Service

Contains the application's business rules.

Responsibilities:

- Business logic
- Validations
- Authorization
- Data processing

---

### Repository

Responsible for database access.

Responsibilities:

- CRUD operations
- Database queries
- Persistence

---

## Security

Authentication will be implemented using:

- Spring Security
- JWT Authentication
- BCrypt Password Encryption

Authorization will be role-based.

---

## Database

The application uses PostgreSQL as its primary relational database.

Database schema changes will be managed through Flyway migrations.

---

## API Design

The backend exposes a RESTful API following standard HTTP methods.

Examples:

- GET
- POST
- PUT
- PATCH
- DELETE

JSON will be used as the communication format.

---

## Scalability

The architecture is designed to support future features, including:

- Multi-company support
- Role-based access control (RBAC)
- File uploads
- Email notifications
- Financial reports
- Third-party integrations

---

## Design Principles

The project follows these principles:

- Separation of Concerns
- Single Responsibility Principle (SRP)
- DRY (Don't Repeat Yourself)
- KISS (Keep It Simple)
- RESTful API Design
- Clean Code
