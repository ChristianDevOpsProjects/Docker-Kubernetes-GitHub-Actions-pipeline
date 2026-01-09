# CI/CD Kubernetes Demo 🚀

A showcase **CI/CD pipeline** demonstrating modern DevOps practices using **Docker, Kubernetes (Minikube), GitHub Actions**, and **GitHub Container Registry (GHCR)**.

---

## 🏗️ Architecture
GitHub Repo → GitHub Actions → GHCR → Kubernetes (Minikube)
- Code changes trigger **GitHub Actions**
- Docker image built & pushed to **GitHub Container Registry**
- Kubernetes Deployment automatically updates pods
- Service exposed via NodePort (Minikube)

---

## 💻 Features

- Dockerized FastAPI app
- Kubernetes Deployment + Service manifests
- GitHub Actions CI/CD pipeline
- Automated image build and deployment
- Secret management for GHCR access

---

## 🚀 How to Run Locally

1. Start Minikube:

```bash
minikube start

1. Build Docker image inside Minikube:
eval $(minikube -p minikube docker-env)
docker build -t cicd-demo:latest .

2. Apply Kubernetes manifests:
kubectl apply -f k8s/

Open service:
minikube service cicd-demo-service

📦 GitHub Actions Pipeline

The workflow:

Builds Docker image

Pushes to GHCR

Deploys to Kubernetes automatically
