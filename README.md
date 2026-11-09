# Guitar Store E-Commerce

A full-stack e-commerce application for an online guitar store, built with Go, Angular, PostgreSQL, Docker, and Kubernetes.

## Overview

Guitar Store is a full-stack web application that provides an online shopping experience for musical instruments. It includes user authentication, product browsing, shopping cart functionality, order management, and administrative features.

The project is organized as a monorepo containing the backend, frontend, and Kubernetes Helm deployment configuration.

## Tech Stack

### Backend
- Go
- PostgreSQL
- REST API
- Docker

### Frontend
- Angular
- TypeScript
- HTML
- CSS

### DevOps & Deployment
- Docker
- Docker Compose
- Kubernetes
- Helm
- Persistent Volumes and Persistent Volume Claims
- Kubernetes ConfigMaps and Secrets
- Ingress

## Features

### Customer Features
- User registration and authentication
- Browse products and categories
- View product details
- Shopping cart management
- Place orders
- View order history
- Manage user profile

### Admin Features
- Product management
- Category management
- Order management

## Project Structure

```text
guitar-store-ecommerce/
│
├── capp/                     # Go backend
│   ├── cmd/
│   ├── internal/
│   │   ├── config/
│   │   ├── handlers/
│   │   ├── middleware/
│   │   ├── models/
│   │   └── repository/
│   ├── migrations/
│   ├── static/
│   ├── Dockerfile
│   └── go.mod
│
├── capp-frontend/             # Angular frontend
│   ├── src/
│   ├── public/
│   ├── Dockerfile
│   └── package.json
│
├── fullstack-chart/           # Kubernetes Helm chart
│   ├── templates/
│   ├── Chart.yaml
│   └── values.yaml
│
└── docker-compose.yaml
```

## Architecture

The application follows a separated frontend/backend architecture.

- **Angular** provides the user interface.
- **Go** handles API requests and application logic.
- **PostgreSQL** stores application data.
- **Docker** containerizes the application components.
- **Kubernetes** manages application deployment and resources.
- **Helm** organizes and manages Kubernetes manifests.

## Running the Project

### Using Docker Compose

Make sure Docker and Docker Compose are installed.

```bash
docker compose up --build
```

### Using Kubernetes and Helm

Make sure Kubernetes and Helm are installed and your Kubernetes cluster is running.

Install the application:

```bash
helm install guitar-store ./fullstack-chart
```

Check the deployed resources:

```bash
kubectl get pods
kubectl get services
kubectl get pvc
```

## Configuration & Security

Application configuration should be provided through environment variables and Kubernetes configuration resources.

**Important:** Do not commit `.env` files, database passwords, JWT secrets, or other sensitive credentials to version control.

## Repository

GitHub: https://github.com/prensmatt/guitar-store-ecommerce

---

*This project was developed as a full-stack and DevOps learning project, combining backend development, frontend development, containerization, and Kubernetes deployment.*
