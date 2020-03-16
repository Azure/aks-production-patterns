# WORK IN PROGRESS

This repo is a **WORK IN PROGRESS**.

# AKS Production Patterns

<!-- 
Guidelines on README format: https://review.docs.microsoft.com/help/onboard/admin/samples/concepts/readme-template?branch=master

Guidance on onboarding samples to docs.microsoft.com/samples: https://review.docs.microsoft.com/help/onboard/admin/samples/process/onboarding?branch=master

Taxonomies for products and languages: https://review.docs.microsoft.com/new-hope/information-architecture/metadata/taxonomies?branch=master
-->

This repo was created to help organizations understand the patterns they will need to think about as they move AKS workloads into production.

## Sections

The repo has been broken into 4 distinct patterns that we are seeing as our more mature customers adopt AKS. The sections do not have to be done in order, they stand by themselves.

- [Cluster Management](cluster-management/README.md)
- [Observability](observability/README.md)
- [Security](security/README.md)
- [Service Mesh](servicemesh/README.md)

## Sample Agenda

The following is a sample agenda of what a 2-day engagement might look like.

### Day 1

- Review of base AKS platform capabilities and configuration (15 minutes)
- Production Ready AKS Architecture Overview & Networking Design (45 Mins)
- Cluster Management (~ 1/2 Day)
  - Namespaces, RBAC, Limits, Quotas
  - GitOps and Multicluster Management
  - Cluster and Nodepool Upgrades / Patching
  - Cost Management
  - Cluster Management Hands-on Challenge
  - Future – Azure Arc for Kubernetes
- Observability (~ 1/2 Day)
  - Logging & Monitoring Tooling at Cluster/Node/Pod Levels
  - Alerting (Logs, Metrics, Policy)
  - Threat detection
  - App Telemetry
  - Observability Hands-on Challenge
  - Future – Azure Security Center Integration

### Day 2

- Security (~ 1/2 Day)
  - Secrets Management – AAD Pod Identity + Key Vault
  - Image Management – Build-time & Run-time Scanning
  - Azure Policy with OPA / Gatekeeper
  - Security Hands-on Challenge
  - Future – AKS + Azure Policy + Azure Container Registry
- Service Mesh (~ 1/2 Day)
  - Capabilities
  - Planning for Service Mesh
  - Service Mesh Interface (SMI)
  - Service Mesh Hands-on Challenge
- Patterns to Consider (1 Hour)
  - CI/CD (Blue/Green, Canary, etc.)
  - Serverless, KEDA
  - Cloud Native ML / MLOps on Kubernetes
- Wrap-up (30 mins)
  - Share Lessons Learned

## Prerequisites

The following are the requirements to **start**.

- Azure Account [Azure Portal](https://portal.azure.com)

  - Ability to create AKS Clusters
  - Ability to create Azure Service Principals or access to one that can create AKS Clusters

- Azure CLI [Install CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest)

  - Minimum Version: 2.1.0
  - AKS Preview Extension: 0.4.30
  - Firewall Extension Version: 0.3.0

- Kubectl CLI [Install kubectl with Azure CLI](https://docs.microsoft.com/en-us/azure/aks/kubernetes-walkthrough#connect-to-the-cluster)

  - Minimum Version: 1.15.0

- Git [Git SCM](https://git-scm.com/downloads)

  - Minimum Version: 2.22

- GitHub Account [GitHub Account](https://help.github.com/en/github/getting-started-with-github/signing-up-for-a-new-github-account)

  - Required for GitOps Approach to Multi-Cluster Management

- Terraform [Terraform Download](https://www.terraform.io/downloads.html)

  - Minimum Version: v0.12.21

- Docker Community Edition (CE)[Install CE](https://docs.docker.com/v17.09/engine/installation/)

  - [Install Docker for Mac](https://docs.docker.com/v17.09/docker-for-mac/install/)
  - [Install Docker for Windows](https://docs.docker.com/v17.09/docker-for-windows/install/)

- Code Editor [Install VS Code](https://code.visualstudio.com/download)

## Fork the Repo

**It is important to Fork this repo, not just clone it. You will be creating Personal Access Tokens, which in turn will be creating SSH keys, and they will be used to make changes to a GitHub repo.**

[Forking a Repository](https://help.github.com/en/github/getting-started-with-github/fork-a-repo)

## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit [Microsoft Open Source](https://cla.opensource.microsoft.com).

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
