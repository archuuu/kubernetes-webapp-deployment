# Kubernetes Web Application Deployment

## Project Overview

This project demonstrates deployment of a Dockerized web application on DigitalOcean Kubernetes (DOKS) using Kubernetes orchestration, load balancing, and horizontal pod autoscaling.

The solution showcases cloud-native deployment concepts including:

* Docker containerization
* Kubernetes deployments
* Load balancing
* Autoscaling
* High availability
* Public cloud hosting

---

# Technologies Used

* Docker
* Kubernetes
* DigitalOcean Kubernetes (DOKS)
* Docker Hub
* Nginx

---

# Project Structure

```text
myproject/
├── index.html
├── Dockerfile
├── deployment.yaml
├── service.yaml
├── css/
├── images/
└── fonts/
```

---

# Docker Build

Build Docker image:

```bash
docker build -t myproject .
```

---

# Run Application Locally

Run Docker container locally:

```bash
docker run -d -p 8080:80 myproject
```

Open browser:

```text
http://localhost:8080
```

---

# Push Image to Docker Hub

Tag Docker image:

```bash
docker tag myproject archana2309/myproject:v1
```

Push image:

```bash
docker push archana2309/myproject:v1
```

---

# Kubernetes Deployment

Deploy application:

```bash
kubectl apply -f deployment.yaml
```

Deploy service:

```bash
kubectl apply -f service.yaml
```

---

# Enable Horizontal Pod Autoscaling

```bash
kubectl autoscale deployment myproject-deployment --cpu-percent=50 --min=2 --max=5
```

---

# Verify Deployment

Check pods:

```bash
kubectl get pods
```

Check services:

```bash
kubectl get svc
```

Check autoscaler:

```bash
kubectl get hpa
```

---

# Features

* Dockerized web application
* Kubernetes orchestration
* Load balancing
* High availability
* Horizontal pod autoscaling
* Cloud-native deployment
* Public cloud hosting

---

# Infrastructure Highlights

* Managed Kubernetes cluster on DigitalOcean
* Public LoadBalancer service
* Multiple pod replicas
* Autoscaling based on CPU utilization
* Containerized deployment using Docker

---

# Future Improvements

* HTTPS & SSL configuration
* CI/CD pipeline automation
* Monitoring & logging
* Custom domain integration
* Kubernetes ingress controller

---

# Author

Archana Iyer
