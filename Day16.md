# DevOps, Containers, and Docker

## 📖 Overview

This repository provides an introduction to **DevOps**, **Containers**, and **Docker**. It covers the basic concepts, architecture, advantages, and commonly used Docker commands for beginners.

---

# 📌 Table of Contents

- What is DevOps?
- What is a Container?
- What is Docker?
- Docker Architecture
- Docker Components
- Docker Image vs Container
- Common Docker Commands
- Docker vs Virtual Machine
- Advantages
- Conclusion

---

# 🚀 What is DevOps?

**DevOps** is a combination of **Development (Dev)** and **Operations (Ops)**.

It is a culture and set of practices that improves collaboration between software developers and IT operations teams. DevOps focuses on automating software development, testing, deployment, and monitoring.

## DevOps Lifecycle

```
Plan
  ↓
Develop
  ↓
Build
  ↓
Test
  ↓
Release
  ↓
Deploy
  ↓
Operate
  ↓
Monitor
```

## Benefits of DevOps

- Faster software delivery
- Better collaboration
- Continuous Integration (CI)
- Continuous Deployment (CD)
- Automation
- Improved software quality
- Faster bug fixes

---

# 📦 What is a Container?

A **container** is a lightweight package that includes:

- Application code
- Runtime
- Libraries
- Dependencies
- Configuration files

Containers ensure applications run consistently across different environments.

### Advantages

- Lightweight
- Portable
- Fast startup
- Secure isolation
- Easy scalability

---

# 🐳 What is Docker?

Docker is an open-source platform used to create, deploy, and run applications inside containers.

Docker packages applications along with all their dependencies, making them portable and easy to deploy.

---

# 🏗 Docker Architecture

```
+----------------------+
|    Docker Client     |
+----------+-----------+
           |
           ▼
+----------------------+
|    Docker Daemon     |
+----------+-----------+
           |
     +-----+------+
     |            |
     ▼            ▼
 Docker Images  Containers
           |
           ▼
      Docker Hub
```

---

# ⚙ Docker Components

## Docker Engine

Runs and manages Docker containers.

## Docker Image

A read-only template used to create containers.

Example:

```bash
docker pull ubuntu
```

## Docker Container

A running instance of a Docker image.

Example:

```bash
docker run ubuntu
```

## Dockerfile

A text file containing instructions to build a Docker image.

Example:

```dockerfile
FROM python:3.12

WORKDIR /app

COPY . .

RUN pip install -r requirements.txt

CMD ["python", "app.py"]
```

## Docker Hub

An online repository for sharing Docker images.

---

# 🖼 Docker Image vs Container

| Docker Image | Docker Container |
|--------------|------------------|
| Blueprint | Running instance |
| Read-only | Read & Write |
| Creates containers | Executes application |

---

# 🔄 Docker Workflow

```
Application
     │
     ▼
Dockerfile
     │
docker build
     │
     ▼
Docker Image
     │
docker run
     │
     ▼
Docker Container
```

---

# 💻 Common Docker Commands

### Check Docker Version

```bash
docker --version
```

### List Images

```bash
docker images
```

### List Running Containers

```bash
docker ps
```

### List All Containers

```bash
docker ps -a
```

### Download an Image

```bash
docker pull nginx
```

### Run a Container

```bash
docker run nginx
```

### Run in Background

```bash
docker run -d nginx
```

### Stop a Container

```bash
docker stop <container_id>
```

### Start a Container

```bash
docker start <container_id>
```

### Restart a Container

```bash
docker restart <container_id>
```

### Remove a Container

```bash
docker rm <container_id>
```

### Remove an Image

```bash
docker rmi <image_name>
```

### Build an Image

```bash
docker build -t myapp .
```

### Open Terminal Inside Container

```bash
docker exec -it <container_id> bash
```

---

# ⚖ Docker vs Virtual Machine

| Docker | Virtual Machine |
|--------|-----------------|
| Lightweight | Heavy |
| Shares Host OS | Separate OS |
| Fast Startup | Slow Startup |
| Low Memory Usage | High Memory Usage |
| High Performance | More Overhead |

---

# ⭐ Advantages of Docker

- Easy deployment
- Portable applications
- Faster startup
- Resource efficient
- Version control for applications
- Supports CI/CD
- Ideal for microservices

---

# 📚 Conclusion

DevOps, Containers, and Docker are essential technologies in modern software development. DevOps improves collaboration and automation, Containers provide isolated execution environments, and Docker simplifies container creation and deployment. Together they enable faster, more reliable, and scalable application delivery.

---
