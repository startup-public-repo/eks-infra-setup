---
name: "Link ArgoCD to EKS"
about: "Request to configure ArgoCD to deploy to an EKS cluster"
title: "[Setup Request] Connect ArgoCD with EKS Cluster"
labels: ["eks", "argocd", "kubernetes", "gitops"]
assignees: ["manupanand"]
---

## ☸️ ArgoCD ↔️ EKS Cluster Integration  
Use this template to request ArgoCD access to a specific Amazon EKS cluster.

---

### Request Details  

#### EKS Cluster Information  
- **EKS Cluster Name**: _Specify the cluster name (e.g., `eks-prod-cluster`)_  
- **AWS Region**: _Specify the AWS region (e.g., `us-west-2`)_  
- **IAM Role for ArgoCD Access (if applicable)**: _Provide ARN for access (e.g., `arn:aws:iam::123456789012:role/argocd-access`)_  

#### ArgoCD Configuration  
- **ArgoCD Project Name**: _Specify the target ArgoCD project (e.g., `platform-team`)_  
- **Git Repository for App Configs**: _Provide the repo URL (e.g., `https://github.com/org/app-configs`)_  
- **Kubernetes Namespaces**:  
  - `default`  
  - `staging`  
  - `app-namespace`  

#### Additional Details  
- _Include any extra configuration details, security policies, or restrictions._  

---

### ✅ Checklist  
Before submitting this request, ensure:  
- [x] All required details are provided.  
- [x] IAM roles and permissions are validated.  
- [x] Repo access is confirmed for ArgoCD.  

