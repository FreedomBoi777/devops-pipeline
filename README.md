DevOps CI/CD Pipeline with Docker, Nginx, AWS

This project demonstrates a production-style deployment of a containerized Node.js application using Docker, Nginx reverse proxy, and AWS EC2. It includes CI pipeline integration using GitHub Actions and basic monitoring via logs.

              ┌──────────────┐
              │   User       │
              │  (Browser)   │
              └──────┬───────┘
                     │ HTTP (80)
                     ↓
              ┌──────────────┐
              │    Nginx     │
              │ Reverse Proxy│
              └──────┬───────┘
                     │
                     ↓
          ┌────────────────────┐
          │  Docker Container  │
          │  Node.js App       │
          │  Port: 3000        │
          └────────┬───────────┘
                   ↓
          ┌────────────────────┐
          │   AWS EC2 Instance │
          │   Ubuntu Server    │
          └────────────────────┘
