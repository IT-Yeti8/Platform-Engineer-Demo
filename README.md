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

## 🏗️ Architecture

```mermaid
graph TD
    %% Styling
    classDef infra fill:#2b2d42,stroke:#8d99ae,stroke-width:2px,color:#fff;
    classDef cicd fill:#3a86ff,stroke:#00b4d8,stroke-width:2px,color:#fff;
    classDef gitops fill:#ff006e,stroke:#ffb703,stroke-width:2px,color:#fff;
    classDef sec fill:#fb5607,stroke:#ff006e,stroke-width:2px,color:#fff;
    classDef obs fill:#8338ec,stroke:#3a86ff,stroke-width:2px,color:#fff;

    %% Infrastructure & Config
    subgraph Provisioning & Configuration
        TF[Terraform] -->|Provisions| VM[Ubuntu VM]
        AN[Ansible] -->|Configures| VM
        VM -->|Hosts| DK[Docker]
        DK -->|Runs| KJ[Jenkins & Kind K8s]
    end
    class TF,VM,AN,DK,KJ infra;

    %% CI/CD Workflow
    subgraph Pipeline & GitOps
        GH[GitHub Commit] -->|Triggers| JK[Jenkins Pipeline]
        JK -->|Pushes Image| CR[GitHub Container Registry]
        CR -->|Pulled by| HM[Kind + Helm]
        HM -->|Managed by| AR[ArgoCD]
        AR -->|Deploys| AP[Docker Voting App]
    end
    class GH,JK,CR,HM,AR,AP cicd;

    %% Security
    subgraph Security Gate
        SQ[SonarQube Code Scan] --> JK
        TV[Trivy Container Scan] --> CR
    end
    class SQ,TV sec;

    %% Observability
    subgraph Metrics & Monitoring
        PR[Prometheus] -->|Scrapes Metrics| AP
        GR[Grafana] -->|Visualizes| PR
    end
    class PR,GR obs;
