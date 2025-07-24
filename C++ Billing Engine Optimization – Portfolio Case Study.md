## C++ Billing Engine Optimization – Portfolio Case Study  
**Project Title:** *High-Throughput Billing Engine Optimization for Telecom Infrastructure*

---

### Context & Objective  
During my role as **Senior Frontend Developer at Rogers/Fido (2016–2018)**, I contributed to backend enhancements on the **telecom billing infrastructure**, specifically a legacy **C++ billing engine** that processed **500K+ daily transactions**. My goal was to boost reliability, performance, and operational uptime without disrupting live billing operations.

---

### Technology Stack
| Component              | Technology Used        |
|------------------------|------------------------|
| Billing Engine         | C++                    |
| Middleware Layer       | C#                     |
| Legacy Integration     | VB6, Oracle DB         |
| Performance Tools      | Valgrind, GFlags       |
| Metrics                | System Uptime, Memory Footprint |

---

### Architecture Flow Diagram

```
                  ┌──────────────────────────┐
                  │  Legacy Billing Workflow │
                  │    (500K+ TX/day)        │
                  └─────────┬────────────────┘
                            │
               ┌────────────▼────────────┐
               │  Core Billing Engine    │
               │     (C++ App)           │
               └─────────┬───────────────┘
                         │
              Memory Optimizations & Leak Detection
                         ▼
           ┌───────────────────────────────────┐
           │ C# Middleware for Data Bridging   │
           │ ─ Handles VB6 ↔ Angular Migration │
           └─────────────┬─────────────────────┘
                         │
              ┌──────────▼─────────┐
              │ Oracle Billing DB  │
              └────────────────────┘
```

---

### Results & Impact
- **Optimized memory handling** in C++ reduced allocation overhead and fixed leaks.
- **Achieved 30% improvement in system uptime**, minimizing downtime from memory-related failures.
- Integrated **C# middleware bridge** to support legacy VB6 and new Angular applications.
- Performed **load testing** and leak detection using Valgrind and internal profiling tools.
- Supported **smooth migration to modern interfaces** without disrupting billing flows.
