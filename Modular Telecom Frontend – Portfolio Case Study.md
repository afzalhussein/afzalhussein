## Modular Telecom Frontend – Portfolio Case Study  
**Project Title:** *Scalable Angular Applications for Telecom Services*

---

### Context & Objective  
At **Rogers/Fido (2016–2018)**, you led the development of modular frontend applications that powered customer portals for telecom services. These portals handled workflows for billing, account management, plan customization, and profile updates.

Your mission: deliver performant, maintainable interfaces using Angular, while collaborating closely with backend teams to ensure consistent API-driven experiences.

---

### Tech Stack
| Layer             | Technology Used     |
|-------------------|---------------------|
| Frontend Framework| Angular, Redux      |
| Backend APIs      | Node.js             |
| State Management  | Redux               |
| Performance Tools | Chrome DevTools, Lighthouse |
| Optimization      | Lazy Loading, Tree Shaking |
| Collaboration     | REST API Integration |

---

### Telecom Portal Architecture Diagram

```
                 ┌────────────────────────────┐
                 │ Customer Portal Frontend   │
                 │   (Angular + Redux)        │
                 └─────────────┬──────────────┘
                               │
              ┌───────────────▼───────────────┐
              │ Modular App Components        │
              │ ─ Billing                     │
              │ ─ Account/Profile Management  │
              │ ─ Plan Selection & Upgrades   │
              └───────────────┬───────────────┘
                               │
                    Lazy Loaded Modules (per route)
                               │
              ┌───────────────▼───────────────┐
              │ Redux Store + State Handlers │
              └───────────────┬───────────────┘
                               ▼
                 ┌─────────────────────────┐
                 │ Node.js REST API Layer  │
                 │  (User Profile Backend) │
                 └─────────────────────────┘
```

---

### Results & Impact
- **Modular Component Design** enabled independent development and faster feature releases.
- **Performance Boosts** using lazy loading and state management best practices.
- **Reduced DOM re-render overhead**, improving time-to-interaction on customer workflows.
- **Tight backend integration** ensured fast, reliable data flows for account management.
- **Scalable Architecture** allowed future reuse across other Rogers services.
