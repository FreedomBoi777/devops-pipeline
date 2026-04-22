DevOps CI/CD Pipeline with Docker, Nginx, AWS.

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
Tech Stack:
- AWS EC2
- Docker
- Nginx
- Node.js
- GitHub Actions
- Linux (Ubuntu)

Setup Instructions:
1. Clone repository
2. Build Docker image:
   docker build -t devops-app .
3. Run container:
   docker run -d -p 3000:3000 --restart unless-stopped devops-app
4. Install and configure Nginx
