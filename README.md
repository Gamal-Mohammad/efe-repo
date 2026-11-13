# Noon Clone – Docker & Kubernetes (EFE)

![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white) ![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?logo=kubernetes&logoColor=white) ![Apache](https://img.shields.io/badge/Apache_httpd-D22128?logo=apache&logoColor=white) ![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)

> A Noon-style e-commerce page, containerised and deployable to Kubernetes.

## Overview

Static web page containerised with **Apache httpd**. The repository is used in the DevOps training track to practise Git, building Docker images and running them as containers. Kubernetes manifests (`deployment.yml`, `svc.yml`) run it with 5 replicas behind a Service.

## Tech Stack

- **Docker**
- **Kubernetes**
- **Apache httpd**
- **HTML/CSS**

## Repository Structure

```text
deployment.yml
Dockerfile
file.txt
index.html
README.md
svc.yml
```

## Getting Started

### Run with Docker

```bash
git clone https://github.com/Gamal-Mohammad/efe-repo.git
cd efe-repo
docker build -t efe-repo .
docker run -d --name efe-repo -p 8080:80 efe-repo
```

Then open http://localhost:8080.

### Deploy to Kubernetes

| File | Kind | Name |
|---|---|---|
| `deployment.yml` | Deployment | `nginx-deployment` |
| `svc.yml` | Service | `nginx-service` |

```bash
kubectl apply -f deployment.yml
kubectl apply -f svc.yml
kubectl get pods,svc
```

## Author

**Gamal Mohammad**

[![GitHub](https://img.shields.io/badge/GitHub-Gamal--Mohammad-181717?logo=github)](https://github.com/Gamal-Mohammad)
