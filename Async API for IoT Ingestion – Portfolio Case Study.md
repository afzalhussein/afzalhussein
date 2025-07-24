## Async API for IoT Ingestion – Portfolio Case Study  
**Project Title:** *Scalable FastAPI Microservice for Vehicle Telemetry*  
**Company:** Toyota  
**Role:** Senior Software Engineer (2021–Present)

---

### Project Objective  
Toyota's connected systems generated massive volumes of real-time telemetry data from vehicles, devices, and edge sensors. I was responsible for building a high-throughput backend ingestion API that could reliably handle 1.2K+ requests/second while maintaining low latency and scalable processing.

---

### Technology Stack  
| Component            | Tools & Technologies         |
|----------------------|------------------------------|
| API Framework        | FastAPI (Python)             |
| Caching Layer        | Redis (92% hit rate)         |
| Database             | PostgreSQL                   |
| Containerization     | Docker                       |
| Deployment           | AWS ECS                      |
| Auth & Security      | JWT, RBAC                    |

---

### System Architecture Diagram

```
    ┌──────────────────────────┐
    │      IoT Devices         │
    │ (Vehicle Sensors, Edge) │
    └────────────┬─────────────┘
                 ▼
     ┌──────────────────────────┐
     │  FastAPI Async Endpoint  │
     │ ─ JSON Telemetry Parser │
     │ ─ JWT Auth Middleware    │
     └────────────┬────────────┘
                  ▼
         ┌────────────────────┐
         │    Redis Cache     │◄───┐
         │ (Hot Sensor Values)│    │
         └────────┬───────────┘    │
                  ▼                │
     ┌──────────────────────────┐  │
     │ PostgreSQL Time-Series DB│◄─┘
     └──────────────────────────┘
                  │
         Async Queues (Celery/Task Fanout)
                  ▼
     ┌──────────────────────────┐
     │ AWS ECS Docker Services │
     └──────────────────────────┘
```

---

### Key Features & Contributions
- **1,200+ requests/sec** throughput using FastAPI async endpoints.
- **Redis caching** enabled rapid lookups and reduced DB load (92% cache hit rate).
- **Time-series telemetry ingestion** via PostgreSQL and normalized schema design.
- **Dockerized microservice** deployed to AWS ECS with auto-scaling configuration.
- Secured endpoints via **JWT auth** and role-based access controls.

---

### Impact
- **Latency reduction** and stable ingest even during telemetry spikes.
- Enabled **real-time monitoring dashboards** for connected vehicle programs.
- Designed for **low-maintenance and high-reliability**, supporting fault-tolerant ingestion across distributed systems.
