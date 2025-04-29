---
name: "ArgoCD to EKS Cluster Integration Issue"
about: "Request assistance with linking ArgoCD to manage deployments on an EKS cluster."
title: "[ArgoCD ↔️ EKS] Connect ArgoCD to EKS Cluster"
labels: ["AWS", "EKS", "ArgoCD", "Kubernetes", "GitOps"]
assignees: [manupanand]
---

## Description

**As a** DevOps engineer  
**I want to** connect ArgoCD to an Amazon EKS cluster  
**So that I can** deploy and manage Kubernetes applications using GitOps workflows.

## Requirements

1. **EKS Cluster Information**:
   - **Cluster Name**: [e.g., eks-production-cluster]
   - **AWS Region**: [e.g., us-west-2]
   - **Kubernetes Version**: [e.g., v1.27]
   - **Cluster Access Method**:
     - Service account (IRSA)
     - IAM Role assumption
     - kubeconfig authentication

2. **ArgoCD Project/Application Details**:
   - **Project Name**: [e.g., platform-team-project]
   - **Application Repositories**:
     - GitOps Repo URL: [e.g.,https://github.com/startup-public-repo/ci-cd-jenkins-pipeline]
   - **Destination Cluster Settings**:
     - Cluster URL: [e.g., https://ABCDEF.gr7.us-west-2.eks.amazonaws.com]
     - Namespaces managed: [e.g., default, staging, production]

3. **Networking and Access**:
   - **ArgoCD Connectivity**: Direct (internal) / External via LoadBalancer / Private endpoint
   - **RBAC Policies**: Namespaces with limited permissions or full-cluster admin

4. **Expected Behavior**:
   - ArgoCD should be able to deploy, sync, and monitor Kubernetes applications on the EKS cluster.

5. **Optional Enhancements**:
   - Enable ApplicationSets for dynamic app generation.
   - Add health checks and auto-sync policies.

## Steps to Reproduce

1. Register EKS cluster in ArgoCD via UI or CLI (`argocd cluster add`).
2. Define Kubernetes apps in Git repository.
3. Sync apps using ArgoCD UI or automation tools.

## Expected Outcome

ArgoCD should successfully deploy and manage Kubernetes apps on the specified EKS cluster, with healthy sync and status reports.

## Actual Outcome

_Describe any issues, authentication errors, or connectivity problems._

## Additional Context

- Logs or errors (kubectl, ArgoCD controller logs, etc.):  
- IAM Role / Service Account details (if issues seem permissions-related):  
- Related GitHub repositories or manifests:  

## Checklist

Before submitting:
- [x] EKS cluster details are provided.
- [x] GitOps repo information is clear.
- [x] Authentication/access method is specified.

---

### Thank you for advancing GitOps practices in our infrastructure! ☸️🚀
