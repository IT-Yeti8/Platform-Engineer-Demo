# Platform Engineer Demo

👤 **Reginald Anderson**
📧 [rtanderson8@gmail.com](mailto:rtanderson8@gmail.com)
🔗 [LinkedIn](https://www.linkedin.com/in/reginald-anderson/)

A hands-on Platform Engineering project focused on building a complete Internal Developer Platform (IDP) using Infrastructure as Code, CI/CD, GitOps, Kubernetes, observability, and security automation.

This project demonstrates how a developer can commit code to GitHub and have it automatically built, scanned, stored, deployed, and monitored through a fully automated platform workflow.

---

## 🏗️ Architecture

```text
Terraform
↓
Ubuntu VM

Ansible
↓
Docker
↓
Jenkins
↓
Kind Kubernetes Cluster

GitHub
↓
Jenkins
↓
GHCR
↓
Kind + Helm
↓
ArgoCD
↓
Deploy Voting App

Prometheus
↓
Grafana

SonarQube
↓
Trivy
```

---

## 🛠️ Skills Demonstrated

* **Infrastructure as Code (IaC)**: Terraform automation
* **Configuration Management**: Ansible playbooks
* **CI/CD Pipelines**: Jenkins automation
* **Containerization**: Docker image builds
* **Container Registry**: GitHub Container Registry (GHCR)
* **Kubernetes Administration**: Kind-based Kubernetes cluster
* **GitOps Deployments**: ArgoCD synchronization
* **Application Packaging**: Helm charts
* **Monitoring & Observability**: Prometheus and Grafana
* **Security Scanning**: SonarQube and Trivy
* **Linux Administration**: Ubuntu server management

---

## 🎯 Project Goals

This project is designed to simulate a real-world Platform Engineering environment.

Instead of focusing on application development, the objective is to create a reliable platform that enables developers to:

* Build applications automatically
* Scan code and container images
* Store container images in a registry
* Deploy applications through GitOps workflows
* Monitor workloads and cluster health
* Reduce manual operational tasks

---

## 📦 Demo Application

This project uses the Docker Voting App as a sample multi-service application.

The application itself is not the focus of the project.

The primary objective is to build and automate the platform responsible for deploying, managing, and monitoring the application.

---

## 📖 Project Journey

### 🏗️ Phase 1 – Infrastructure as Code

* Provision Ubuntu platform server with Terraform
* Configure system resources and networking
* Establish repeatable infrastructure deployment

### ⚙️ Phase 2 – Configuration Management

* Configure the server using Ansible
* Install Docker
* Install Jenkins
* Install Kind Kubernetes cluster
* Install kubectl and Helm

### 🚀 Phase 3 – CI/CD Automation

* Configure Jenkins pipelines
* Clone and build the Docker Voting App
* Build Docker images automatically
* Push container images to GitHub Container Registry (GHCR)

### ☸️ Phase 4 – Kubernetes Platform

* Deploy a Kind Kubernetes cluster
* Package applications using Helm charts
* Deploy workloads and services to Kubernetes
* Manage application lifecycle through Kubernetes

### 🔄 Phase 5 – GitOps Deployment

* Deploy ArgoCD
* Connect Git repositories to Kubernetes
* Automate deployments using GitOps workflows
* Synchronize cluster state from Git

### 📊 Phase 6 – Observability

* Deploy Prometheus
* Deploy Grafana
* Monitor cluster health and application performance
* Create dashboards for metrics and resource utilization

### 🔒 Phase 7 – Security Automation

* Integrate SonarQube into Jenkins pipelines
* Integrate Trivy container image scanning
* Automate code quality and vulnerability checks
* Enforce security validation before deployments

---

## 💡 Why This Project Matters

This project demonstrates the skills commonly required for modern Platform Engineer, DevOps Engineer, and Cloud Platform Engineer roles.

It showcases:

* Infrastructure automation
* Kubernetes administration
* GitOps workflows
* CI/CD automation
* Observability and monitoring
* Security integration
* Developer platform design

Rather than focusing on application development, this project focuses on building the platform that enables developers to deliver software efficiently and reliably.
