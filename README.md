# azure-devops-aks-terraform-project

## Overview
End-to-end CI/CD pipeline deploying containerized app to AKS.

## Tech Stack
- Azure DevOps
- Docker
- AKS (Kubernetes)
- Terraform
- Azure Key Vault

## Architecture
[Developer]
     ↓
[Git Repo]
     ↓
┌────────────────────────────┐
│ Azure DevOps Pipeline      │
│  - Build                  │
│  - Docker                 │
│  - Key Vault (Secrets)    │
└────────────────────────────┘
     ↓
[ACR]
     ↓
┌────────────────────────────┐
│ AKS Cluster                │
│  Deployment (2 replicas)   │
│  Pods                     │
│  LoadBalancer Service     │
└────────────────────────────┘
     ↓
[End User]

## Features
- CI/CD automation
- Container deployment
- Infrastructure as Code
- Secure secret management

## How to Run
1. Terraform apply
2. Build pipeline
3. Deploy to AKS
