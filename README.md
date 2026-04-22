DevOps CI/CD Pipeline with Docker, Nginx, AWS

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
