## Product/Order Management API – Portfolio Case Study  
**Project Title:** *Scalable E-commerce Backend with Django REST Framework*  
**Category:** Python Projects · E-commerce · REST API  
**Tools & Tech:** Django · PostgreSQL · Celery · Stripe · JWT · Postman

---

### Context & Objective  
As part of your personal Python projects, you built a feature-rich backend API for an e-commerce platform. This API enables secure and scalable management of product listings, customer orders, and payment transactions.

You designed the system using **Django REST Framework**, integrating third-party services like **Stripe** for payments and **Celery** for asynchronous processing.

---

### Architecture Overview

```
            ┌───────────────────────────────┐
            │ Frontend Client (React/App)   │
            └─────────────┬─────────────────┘
                          ▼
               ┌──────────────────────┐
               │ Django REST API      │
               │ ─ Product Endpoints  │
               │ ─ Order Endpoints    │
               │ ─ JWT Authentication │
               └──────┬───────────────┘
                      ▼
         ┌────────────────────────────┐
         │ PostgreSQL Database        │
         │ ─ Products / Orders / Users│
         └────────────────────────────┘
                      ▲
           Async Tasks (Inventory + Emails)
                      │
               ┌────────────┐
               │   Celery   │
               └────┬───────┘
                    ▼
            ┌──────────────────────┐
            │ Stripe Webhooks      │
            │ ─ Payments + Refunds │
            └──────────────────────┘
```

---

### Features & Highlights
- **Product Management**: CRUD operations for products with price, stock, category, and metadata.
- **Order Processing**:
  - Create orders with line items and totals
  - Track status: pending, confirmed, shipped, cancelled
- **JWT Authentication**: Protects order-related endpoints and manages user roles.
- **Stripe Integration**: Handles payment workflows and webhooks for status updates.
- **Celery Async Tasks**: Offloads long-running jobs (email confirmations, inventory sync).
- **Documentation**: Included a Postman collection and Swagger/OpenAPI for easy onboarding.

---

### Performance & Reliability
- Scales with 1K+ requests per minute across endpoints
- Robust error handling for webhook retries
- Test coverage with **pytest** and **factory_boy**

