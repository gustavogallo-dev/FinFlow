# FinFlow

## Software Requirements Specification (SRS)

### Product Scope

FinFlow is a Software as a Service (SaaS) platform designed to help small and medium-sized businesses manage their financial operations through a modern, secure, and intuitive web application.

The first version focuses on essential financial management features, allowing users to monitor cash flow, manage transactions, and visualize financial performance in real time.

---

## Functional Requirements

### Authentication

**FR-001**
The system shall allow users to register using their full name, email address, and password.

**FR-002**
The system shall allow registered users to sign in using their email address and password.

**FR-003**
The system shall allow authenticated users to sign out securely.

**FR-004**
The system shall allow users to recover their password via email.

**FR-005**
The system shall allow authenticated users to change their password.

---

### Company Management

**FR-006**
The system shall allow users to create one or more companies.

**FR-007**
The system shall allow users to edit company information.

**FR-008**
The system shall associate all financial data with a specific company.

---

### Financial Management

**FR-009**
The system shall allow users to register income transactions.

**FR-010**
The system shall allow users to register expense transactions.

**FR-011**
The system shall allow users to organize transactions using categories.

**FR-012**
The system shall allow users to edit transactions.

**FR-013**
The system shall allow users to delete transactions.

---

### Dashboard

**FR-014**
The system shall display the current account balance.

**FR-015**
The system shall display total income.

**FR-016**
The system shall display total expenses.

**FR-017**
The system shall display recent financial transactions.

**FR-018**
The system shall display financial charts and key performance indicators.

---

## Non-Functional Requirements

**NFR-001**
The application shall provide a responsive user interface.

**NFR-002**
Passwords shall be securely encrypted.

**NFR-003**
Authentication shall use JWT.

**NFR-004**
The backend shall expose a RESTful API.

**NFR-005**
The application shall use PostgreSQL as its primary database.

**NFR-006**
The project shall be containerized using Docker.

---

## User Roles

### Owner

Has full access to all company resources.

### Administrator

Can manage financial data and company information.

### Employee

Can access only the resources explicitly granted by the Owner or Administrator.

---

## Business Rules

- Every transaction must belong to a company.
- Every company must have at least one owner.
- Users may belong to multiple companies.
- Users may only access companies they are members of.
- Every transaction must have a category.
- Transaction values must be greater than zero.

---

## Assumptions

- Internet access is required.
- Users must have a valid email address.
- Each company manages its own financial data independently.

---

## Out of Scope

The first version does not include:

- Bank integrations
- PIX integration
- Invoice generation
- Mobile application
- AI-powered financial analysis
- Accounting integrations
