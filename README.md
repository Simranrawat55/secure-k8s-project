# Security Hardened Kubernetes Platform

A secure containerized application deployed on Kubernetes with security hardening, network isolation, RBAC, secrets management, ingress, and automated CI/CD using Jenkins.

## Project Overview

This project demonstrates the deployment of a Flask-based application on a Kubernetes cluster with multiple security controls.

The platform is designed to provide:

- Containerized application deployment
- Kubernetes orchestration
- Role-Based Access Control (RBAC)
- Network isolation using NetworkPolicy
- Secure configuration using ConfigMap and Secret
- Dedicated ServiceAccount
- Pod security hardening
- Ingress-based application access
- Automated CI/CD using Jenkins
- Automated Docker image building
- Automated Kubernetes deployment and rollout verification

---

## Technologies Used

- Python
- Flask
- Docker
- Kubernetes
- Minikube
- Jenkins
- Git
- GitHub
- YAML
- Nginx Ingress

---

## Architecture

```text
                 GitHub
                    |
                    v
                 Jenkins
                    |
             Docker Build
                    |
                    v
            Docker Image
                    |
                    v
              Kubernetes
              (Minikube)
                    |
        +-----------+-----------+
        |                       |
   Deployment                Service
   2 Replicas                   |
        |                       v
        |                 Application
        |
   Security Controls
        |
   +----+----+---------+----------+
   |         |         |          |
 RBAC   NetworkPolicy  Secret  ServiceAccount
   |
 Pod Security Hardening
