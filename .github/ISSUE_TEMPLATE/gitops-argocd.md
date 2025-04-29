name: Link Jenkins to ArgoCD
description: Request to integrate Jenkins pipeline with ArgoCD GitOps deployment
title: "[Integration Request] Link Jenkins Pipeline with ArgoCD"
labels: [jenkins, argocd, gitops, ci-cd]
assignees: [manupanand]

body:
  - type: markdown
    attributes:
      value: |
        ## 🧩 Jenkins ↔️ ArgoCD GitOps Integration
        Use this template to request the linkage of a Jenkins pipeline to trigger or interact with ArgoCD GitOps deployments.

  - type: input
    id: jenkins-job-name
    attributes:
      label: Jenkins Job Name
      description: Provide the full name of the Jenkins job or pipeline
      placeholder: e.g., ci-pipeline-service-a
    validations:
      required: true

  - type: input
    id: git-repo
    attributes:
      label: Git Repository (ArgoCD App Source)
      description: Provide the Git repository URL linked to ArgoCD
      placeholder: e.g., https://github.com/org/service-a-gitops
    validations:
      required: true

  - type: input
    id: branch
    attributes:
      label: Git Branch
      description: Branch in the repo to monitor or update (typically `main` or `dev`)
      placeholder: main
    validations:
      required: true

  - type: textarea
    id: pipeline-action
    attributes:
      label: What should the Jenkins job do?
      description: Should Jenkins update values.yaml? Create a Git commit? Just notify ArgoCD?
      placeholder: |
        Example:
        - Commit updated Docker image tags to GitOps repo
        - Trigger ArgoCD sync via webhook
    validations:
      required: true

  - type: input
    id: argocd-app-name
    attributes:
      label: ArgoCD Application Name (if known)
      description: Optional – Name of the ArgoCD application for targeting sync
      placeholder: service-a
    validations:
      required: false

  - type: textarea
    id: additional-info
    attributes:
      label: Additional Information
      description: Any environment, security, or RBAC considerations
