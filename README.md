## The CI/CD test
A test for CI/CD pipeline constain simple python with Flask, Docker, GitHub Actions, adn AWS EC2

## This pipeline does
Every time code is pushed to main or PR to main:
1. GitHub Actions runs automated tests
2. Builds a Docker Image
3. Pushes the image to Docker Hub
4. App is deployed on AWS EC2

## Stack

- **Python** / **Flask** - Simple Web app
- **Docker** - containization
- **GitHub Actions** - CI/CD pipeline
- **AWS EC2** - Cloud compute deployment
- **Docker Hub** - image registry
- **Kubernetes** - basic container orchestration (local)

## To run locally
Clone the repo:
```bash
git clone https://github.com/PaleCanary/Pipeline_test.git
cd Pipeline_test
```

## Run locally with Docker
```bash
docker pull palecanary/my-pipeline:latest
docker run -p 3000:3000 palecanary/my-pipeline:latest
```
## Run locally with kubernetes
```bash
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```
## Kubernetes setup
- 2 replicas running
- LoadBalancer is exposed on port 80 (HTTP)
- Auto Create new one if deleted
```bash
kubectl delete pod my-pipeline-###########
kubectl get pods
```

## Overview

push to GitHub main > test with Actions > docker build image > push to docker hub > SSH to EC2 > app live

Author: Arinchai + PaleCanary (Same Person)
