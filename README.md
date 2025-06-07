# MyApp Kubernetes Deployment with Helm

This repository contains a Helm chart and Kubernetes manifests for deploying **MyApp** using Minikube and Docker driver on Windows.

---

## Prerequisites

- [Minikube](https://minikube.sigs.k8s.io/docs/start/) installed and running (using Docker driver on Windows)
- [kubectl](https://kubernetes.io/docs/tasks/tools/) CLI installed
- [Helm](https://helm.sh/docs/intro/install/) installed
- Docker installed and running

---

## Project Structure
K8s-Canary-Deployment/
├── app/ # Application source code and Dockerfiles
├── docs/ # Documentation and notes
├── helm-chart/ # Helm chart for deploying the app
├── istio/ # Istio configuration files for service mesh and routing
├── k8s/ # Kubernetes manifests (Deployments, Services, etc.)
└── logs/ # Logs and output files

---

## Prerequisites

- Kubernetes cluster (e.g., Minikube)
- kubectl CLI
- Helm CLI
- Docker installed and running
- Istio installed in your cluster (if using Istio config)

---

## Setup and Deployment

### 1. Start Minikube

```bash
minikube start --driver=docker

2. Build Docker images (if required)
Go to the app/ directory and build your app image:

cd app
docker build -t myapp:v1 .
docker build -t myapp:v2 .
Push it to your Docker registry if needed.

3. Deploy using Helm
Go to the helm-chart directory and install or upgrade the release:

cd helm-chart
helm upgrade --install myapp-release . -f values.yaml

4. Verify deployment

kubectl get pods
kubectl get svc

5. Access the app
Use Minikube to access the service:

```bash
minikube service myapp-myapp-release --url

Keep the terminal open to keep the tunnel active. Open the printed URL in your browser.

---

License
MIT License Koppala Ajith Kumar Reddy






