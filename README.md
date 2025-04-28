
---

# EKS Infrastructure Setup Using Terraform, Ansible, and Vault

## Overview

This repository provides an automated and secure method for deploying an Amazon Elastic Kubernetes Service (EKS) infrastructure. By leveraging **Terraform** for infrastructure provisioning, **Ansible** for configuration management, and **Vault** for secrets management, the project ensures scalability, security, and efficiency.

## Features

- **Infrastructure as Code (IaC)**: Utilize Terraform to define and provision EKS clusters and other AWS resources.
- **Configuration Management**: Use Ansible for configuring nodes, deploying dependencies, and setting up Kubernetes workloads.
- **Secure Secrets Management**: Leverage Vault to securely manage sensitive data such as credentials and secrets.
- **Modular Design**: Organize code into reusable modules for flexibility and clarity.

## Prerequisites

Before you begin, ensure you have the following installed:

- **Terraform** (>= 1.0.0)
- **Ansible** (>= 2.9)
- **HashiCorp Vault** (>= 1.8.0)
- **AWS CLI** (>= 2.0.0)
- An AWS account with proper IAM permissions
- A workstation with access to the internet and required tools

## Setup and Usage

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/eks-infra-setup.git
cd eks-infra-terraform-ansible-vault
```

### 2. Configure Terraform
1. Navigate to the Terraform directory:
   ```bash
   cd terraform
   ```
2. Update the `variables.tf` file with your AWS region, VPC details, and other parameters.
3. Initialize Terraform:
   ```bash
   terraform init
   ```
4. Apply the configuration:
   ```bash
   terraform apply
   ```
   This will provision the necessary infrastructure, including EKS clusters.

### 3. Configure Secrets with Vault
1. Start Vault and authenticate:
   ```bash
   vault login <your-auth-token>
   ```
2. Store sensitive information:
   ```bash
   vault kv put secret/eks-access kubeconfig=<your-kubeconfig> aws_key=<your-aws-key>
   ```

### 4. Use Ansible for Configuration
1. Navigate to the Ansible directory:
   ```bash
   cd ansible
   ```
2. Update the `inventory` and playbooks to match your environment.
3. Execute the playbook to configure the infrastructure:
   ```bash
   ansible-playbook main.yml
   ```

## Directory Structure

```
├── terraform/
│   ├── main.tf
│   ├── variables.tf
│   ├── outputs.tf
├── ansible/
│   ├── inventory
│   ├── roles/
│   ├── main.yml
├── vault/
│   ├── policies/
│   ├── secrets/
├── README.md
```

## Contributions

Contributions are welcome! Please fork the repository and create a pull request with detailed descriptions of your changes.

## License

This project is licensed under the [MIT License](LICENSE).

---

You can customize this README to include specific details about your setup or additional functionality. Let me know if you'd like any edits or enhancements!
