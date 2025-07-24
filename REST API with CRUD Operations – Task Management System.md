## REST API with CRUD Operations – Task Management System  
**Project Title:** *FastAPI-Based Backend for Task & Workflow Automation*  
**Type:** Python Project  
**Technologies:** FastAPI · PostgreSQL · Redis · JWT · Pydantic · pytest

---

### Project Context  
In your Task Management System, you designed and implemented a production-grade **REST API** using **FastAPI**, supporting complete **CRUD operations** for task lifecycle management. The system allowed users to create, view, update, and delete tasks securely — with blazing-fast performance and scalability.

---

### Architecture Overview

```
        ┌──────────────┐
        │ Frontend App │
        │  (React, etc)│
        └─────┬────────┘
              │
         RESTful API Request
              ▼
      ┌───────────────────┐
      │  FastAPI Backend  │
      │ ─ Task Endpoints  │
      │ ─ Auth Middleware │
      └─────┬─────────────┘
            ▼
  ┌──────────────────────────┐
  │ PostgreSQL Database      │
  │ ─ Task Metadata          │
  │ ─ User Permissions       │
  └──────────────────────────┘
            ▲
    Redis Caching Layer
    (Frequently queried tasks)

```

---

### Key Features & Implementation
- **CRUD Endpoints**: Implemented Create, Read, Update, and Delete routes for task objects with Pydantic-based validation.
- **Secure Auth Layer**: Integrated **JWT authentication** to restrict access, with role-based checks for modifying tasks.
- **Redis Caching**: Frequently accessed tasks served from Redis (92% hit rate in other projects) to improve responsiveness.
- **Full-Text Search**: Enabled efficient querying of tasks via **PostgreSQL FTS** (ideal for large datasets).
- **Robust Testing**: Achieved **>90% pytest coverage** across routes and edge cases.
- **Well-Documented**: Created **Postman collections** for developer onboarding and QA testing.

