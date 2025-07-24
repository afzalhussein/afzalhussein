## **RBAC Validation Service – Portfolio Case Study**  
**Project Title:** *Centralized RBAC Microservice for Scalable Authorization*

---

### **Project Overview**
During my time at **Informatica**, I designed and developed a standalone RBAC (Role-Based Access Control) validation microservice. It ensured consistent, secure permission handling across distributed microservices by validating user roles in real-time using in-memory caching and secure design practices.

This project played a key role in unifying permission logic and improving response time for authentication flows within the company’s platform ecosystem.

---

### **Tech Stack Used**
| Layer                | Technology/Tool        |
|----------------------|------------------------|
| Runtime              | Node.js                |
| Caching              | Redis                  |
| Security             | Encrypted Secrets      |
| Static Code Analysis | SonarQube              |
| Deployment           | AWS Lambda (Optional)  |

---

### **System Architecture**

```
Client → Auth Service → RBAC Validation Microservice
                             ↓
                     Redis Caching Layer
                             ↓
                  Role & Permission Evaluation
                             ↓
                 Allow / Deny Access Response
```

Key design elements:
- JWT token decoded by Auth Service
- Redis-backed permission rule cache reduces latency by 35%
- Secure endpoints validate role-action-resource mappings
- SonarQube enforced secure coding & code quality

---

### **Impact & Results**
- **35% latency improvement** in high-volume access control flows  
- **Permission centralization** eliminated duplication across services  
- **Static analysis via SonarQube** improved code maintainability  
- **Enhanced security posture** through encrypted secrets and auditability

