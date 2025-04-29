name: Link ArgoCD to EKS
description: Request to configure ArgoCD to deploy to an EKS cluster
title: "[Setup Request] Connect ArgoCD with EKS Cluster"
labels: [eks, argocd, kubernetes, gitops]
assignees: []

body:
  - type: markdown
    attributes:
      value: |
        ## ☸️ ArgoCD ↔️ EKS Cluster Integration
        Use this template to request ArgoCD access to a specific Amazon EKS cluster.

  - type: input
    id: eks-cluster-name
    attributes:
      label: EKS Cluster Name
      description: Name of the EKS cluster to connect with ArgoCD
      placeholder: eks-prod-cluster
    validations:
      required: true

  - type: input
    id: region
    attributes:
      label: AWS Region
      description: Region where the EKS cluster is hosted
      placeholder: us-west-2
    validations:
      required: true

  - type: input
    id: iam-role
    attributes:
      label: IAM Role for ArgoCD Access (if applicable)
      description: IAM role ARN ArgoCD will assume to access the EKS cluster (via IRSA or kubeconfig)
      placeholder: arn:aws:iam::123456789012:role/argocd-access
    validations:
      required: false

  - type: input
    id: argocd-project
    attributes:
      label: ArgoCD Project Name
      description: Target ArgoCD project to assign the EKS app to
      placeholder: platform-team
    validations:
      required: false

  - type: textarea
    id: repo-url
    attributes:
      label: Git Repository for App Configs
      description: Link to the GitOps repo ArgoCD should use for deployment
      placeholder: https://github.com/org/app-configs
    validations:
      required: true

  - type: textarea
    id: namespaces
    attributes:
      label: Kubernetes Namespaces
      description: List of namespaces in the EKS cluster ArgoCD should manage
      placeholder: |
        - default
        - staging
        - app-namespace
    validations:
      required: true

  - type: textarea
    id: additional-details
    attributes:
      label: Additional Details
      description: Any extra configuration details, security policies, or restrictions
