# Lab Sessional Cafe Management System - Microservices Setup

## Overview
This project contains multiple Node.js microservices for a Cafe Management System:
- API Gateway
- Customer Services
- Inventory Services
- Menu Services
- Order Services
- Payment Services

## Local Development Setup

### Install Dependencies
Navigate to each microservice directory and run:
```
npm install
```

### Run Microservices Locally
You can run each microservice independently using:
```
node index.js
```

### Docker Setup

#### Build Docker Images
Each microservice has a Dockerfile. To build all images locally, run:
```
docker-compose build
```

#### Run with Docker Compose
To start all services and network them together, run:
```
docker-compose up
```
This will expose the services on ports 3000-3005.

## CI/CD with GitHub Actions

A GitHub Actions workflow is configured to:
- Build Docker images for each microservice on push to `main` branch
- Push images to Docker Hub (requires setting secrets `DOCKER_USERNAME` and `DOCKER_PASSWORD`)

## Notes
- Ensure Docker Desktop or Docker Engine is installed and running.
- Update ports in Dockerfiles and docker-compose.yml if needed.
- API Gateway routes requests to other microservices.

## Repository
Make sure to push your code to your GitHub repository before enabling CI/CD.
