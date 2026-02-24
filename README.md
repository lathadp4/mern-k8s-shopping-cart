# mern-k8s-shopping-cart
🛒 Shopping Cart – MERN Stack with Docker, Kubernetes & CI/CD
A production-style MERN application deployed using Docker and Kubernetes with proper service communication, environment management, and CI/CD integration.
____________________________________________________
🚀 Project Overview
This project demonstrates:
Full-stack MERN architecture
Dockerized frontend and backend
MySQL deployed inside Kubernetes
Internal service-to-service communication
NodePort-based external exposure
CI/CD using GitHub Actions
Production-level Kubernetes concepts
_______________________________________________________
🏗 Architecture

Browser
   ↓
Frontend Service (NodePort)
   ↓
Frontend Pod (React + Nginx)
   ↓
Backend Service (NodePort / ClusterIP)
   ↓
Backend Pod (Node.js + Express + Sequelize)
   ↓
MySQL Service (ClusterIP)
   ↓
MySQL Pod
___________________________________________________
🧰 Tech Stack
Frontend: React.js
Backend: Node.js + Express
ORM: Sequelize
Database: MySQL
Containerization: Docker
Orchestration: Kubernetes (Minikube)
CI/CD: GitHub Actions
__________________________________________________
🐳 Docker Setup
Backend
Node.js Alpine image
Production dependencies only
Exposes port 3400

Frontend
Multi-stage Docker build
React build → Nginx serve
Build-time environment variable injection
__________________________________________________
☸ Kubernetes Configuration
Namespaces
shopping-cart
Services
frontend-service → NodePort
backend-service → ClusterIP / NodePort
mysql-service → ClusterIP
Key Kubernetes Concepts Used
Service discovery via DNS
Secrets for DB connection
Deployment & ReplicaSets
Rolling updates
Port forwarding
NodePort exposure

