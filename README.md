# Kubernetes Web Application Deployment

## Project Overview

This project demonstrates deployment of a Dockerized web application on DigitalOcean Kubernetes (DOKS).

Technologies Used:
- Docker
- Kubernetes
- DigitalOcean Kubernetes
- Docker Hub
- Nginx

---

## Project Structure

myproject/
├── index.html
├── Dockerfile
├── deployment.yaml
├── service.yaml

---

## Docker Build

docker build -t myproject .

---

## Run Locally

docker run -d -p 8080:80 myproject

---

## Push to Docker Hub

docker tag myproject archana2309/myproject:v1

docker push archana2309/myproject:v1

---

## Kubernetes Deployment

kubectl apply -f deployment.yaml

kubectl apply -f service.yaml

---

## Enable Autoscaling

kubectl autoscale deployment myproject-deployment --cpu-percent=50 --min=2 --max=5

---

## Verify Deployment

kubectl get pods

kubectl get svc

kubectl get hpa

---

## Features

- Containerized deployment
- Kubernetes orchestration
- Load balancing
- High availability
- Horizontal pod autoscaling
