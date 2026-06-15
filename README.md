# Platform Engineer Demo

👤 **Reginald Anderson**
📧 [rtanderson8@gmail.com](mailto:rtanderson8@gmail.com)
🔗 [LinkedIn](https://www.linkedin.com/in/reginald-anderson/)

A hands-on Platform Engineering project focused on building a complete Internal Developer Platform (IDP) using Infrastructure as Code, CI/CD, GitOps, Kubernetes, observability, and security automation.

This project demonstrates how a developer can commit code to GitHub and have it automatically built, scanned, stored, deployed, and monitored through a fully automated platform workflow.

---

## 🏗️ Architecture

[See this architecture diagram](./Architecture%20Diagram.pdf)

---

## 🛠️ Skills Demonstrated

| Area | Tools & Approach |
| :--- | :--- |
| **Infrastructure as Code (IaC)** | Terraform automation |
| **Configuration Management** | Ansible playbooks |
| **CI/CD Pipelines** | Jenkins automation and pipeline development |
| **Containerization** | Docker image builds, deployment, and GitHub Container Registry (GHCR) |
| **Kubernetes** | Kind-based clusters, kubectl, and Helm chart packaging |
| **GitOps Deployments** | ArgoCD synchronization and automated delivery |
| **Monitoring & Observability** | Prometheus metrics, Grafana dashboards, and alerting loops |
| **Security Automation** | SonarQube code analysis, Trivy scanning, and Kubernetes Network Policies |
| **Operations & DevEx** | Makefile automation, runbooks, and rollback procedures |
---

## 📖 Project Journey

### 🏗️ Phase 1 – Infrastructure as Code

* Provision Ubuntu platform server with Terraform
* Configure system resources and networking
* Establish repeatable infrastructure deployment

### ⚙️ Phase 2 – Configuration Management

* Configure the server using Ansible playbooks
* Automated installation of Docker, Jenkins, Kind, kubectl, and Helm

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
* Deploy ArgoCD to the cluster
* Connect Git repositories to track configuration states
* Automate application deployments using GitOps continuous delivery workflows
* Eliminate manual `kubectl apply` commands by synchronizing cluster state from Git

### 📊 Phase 6 – Observability
* Deploy Prometheus to collect cluster metrics and application performance data
* Deploy Grafana to build centralized monitoring dashboards
* Establish a complete operational feedback loop with customized metrics visualization

### 🔒 Phase 7 – Security Automation
* Integrate SonarQube into Jenkins pipelines for automated static code analysis
* Run Trivy container image scans to catch vulnerabilities before images hit the registry
* Enforce Kubernetes Network Policies to restrict pod-to-pod traffic and isolate workloads

### 🛠️ Phase 8 — Operations & Developer Experience
* Document deployment, rollback, and troubleshooting procedures in dedicated runbooks
* Implement a Makefile to provide single-command operations (`make deploy`, `make destroy`) to optimize platform management

---
