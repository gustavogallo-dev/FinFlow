# FinFlow

## Database Design

### Overview

The FinFlow database is designed using a relational model to ensure data integrity, scalability, and maintainability.

The first version focuses on supporting multi-company financial management while keeping the schema simple and extensible.

---

## Database Management System

- PostgreSQL

---

## Entity Relationship Overview

User
│
├── CompanyMember
│ │
│ ▼
│ Company
│
├── Transaction
│
└── PasswordResetToken

Transaction
│
└── Category

---

## Main Entities

### User

Represents a registered platform user.

Responsibilities:

- Authentication
- Profile information
- Account ownership

---

### Company

Represents a business managed within FinFlow.

Responsibilities:

- Store company information
- Own financial records
- Manage members

---

### CompanyMember

Represents the relationship between users and companies.

Responsibilities:

- User permissions
- User roles
- Company membership

---

### Category

Represents financial transaction categories.

Examples:

- Salary
- Rent
- Taxes
- Marketing
- Utilities

---

### Transaction

Represents any financial movement.

Types:

- Income
- Expense

Each transaction belongs to:

- One company
- One category

---

### PasswordResetToken

Stores temporary password recovery tokens.

---

## Relationships

User
1:N
CompanyMember

Company
1:N
CompanyMember

Company
1:N
Transaction

Category
1:N
Transaction

User
1:N
PasswordResetToken

---

## Future Expansion

The current database design allows future implementation of:

- Multi-company support
- Role-based access control
- Financial reports
- File attachments
- Bank integrations
- Audit logs
