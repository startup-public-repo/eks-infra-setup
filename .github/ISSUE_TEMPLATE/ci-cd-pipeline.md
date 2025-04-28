---
name: "Jenkins CI/CD Pipeline Server Setup"
about: "Report or request the setup of a Jenkins CI/CD pipeline server."
title: "[Jenkins CI/CD] Basic Server Setup with Upgrade Requirements"
labels: ["Jenkins", "CI/CD", "Setup", "AWS", "EKS"]
assignees: [manupanand]
---

## Description

**As a** DevOps engineer

Set up a basic Jenkins CI/CD pipeline server to support continuous integration and delivery for projects. The server will initially meet basic requirements but should be upgradeable for future scalability and integration needs.

## Requirements

1. **Server Details**:
   - **Operating System**: RHEL (Red Hat Enterprise Linux) image on AWS.
   - **Hardware Requirements**: 
     - CPUs: 4
     - RAM: 8GB
     - Storage: 50GB

2. **Jenkins Setup**:
   - Jenkins Version: Latest LTS version.
   - Plugins Required: Git, Pipeline, Blue Ocean.

3. **Pipeline Details**:
   - Type of Pipeline: Declarative.
   - Initial Stages: Build, Test, Deploy.
   - Source Repository: GitHub.

4. **Future Integration Needs**:
   - Kubernetes Integration: Setup to integrate with Amazon Elastic Kubernetes Service (EKS).
   - Scaling: Ensure the server is capable of hardware upgrades to handle increased load.

## Steps to Reproduce

1. Deploy the RHEL image on AWS.
2. Install Jenkins and required plugins.
3. Configure pipeline stages.
4. Test the pipeline functionality.

## Expected Outcome

A fully operational Jenkins server set up on AWS, capable of handling CI/CD workflows. The server should be prepared for future upgrades and integration with Kubernetes on EKS.

## Actual Outcome

_Provide details if there are any issues or deviations after setup._

## Additional Context

- Known blockers: Potential limitations with AWS instance scaling or plugin compatibility.
- Dependencies: Ensure the RHEL image has required configurations for Jenkins installation.

## Checklist

Before submitting this issue, ensure the following:
- [x] All requirements are clearly listed.
- [x] Relevant logs or screenshots are included (if applicable).
- [x] The issue title is descriptive and concise.

---

### Thank you for your contribution!
