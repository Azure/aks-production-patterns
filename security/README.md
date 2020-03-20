# Security

This security section is all about how to implement security controls within Azure and AKS to meet an organizations security needs. The main focus areas are Kubernetes Policy, secrets management, and build and runtime container image management.

## Exercise

You've been tasked with improving the security of your existing AKS clusters. There are a number of security controls that the organization needs to implement and want to know how to do this in the Azure and Kubernetes ecosystems. There are clusters that are pulling images from non-sanctioned registries, secrets stored in base64 encoded Kuberentes secrets, and no container image scanning take place at all. The ask from the CTO and Security Team is to ensure that all clusters are leveraging Kubernetes Policy, all secrets are stored in Azure Key Vault, and build and runtime image scanning are put in place.

### Security #1

Your first challenge is to install OPA + Gatekeeper into your cluster and put a policy in place that does not allow pulling container images from Docker Hub.

### Security #2

Your second challenge is to setup AAD Pod Identity into your cluster and mount keys in Azure Key Vault to a running container.

### Security #3

Your third challenge is setting up Azure Security Center so it can highlight security recommendations and capture securty threats within the cluster.

## Success Criteria

* Creating a container from a container image in Docker Hub fails.
* Exec into a running container and show the Azure Key Vault keys have been successfully mounted.
* Show one Azure Security Center recommendation, and one Azure Security Center threat that pertains to your cluster.

## References

OPA + Gatekeeper

* [Gatekeeper](https://github.com/open-policy-agent/gatekeeper)

AAD Pod Identity

* [AAD Pod Identity](https://github.com/Azure/aad-pod-identity)

Azure

* [Container Image Management Security](https://docs.microsoft.com/en-us/azure/aks/operator-best-practices-container-image-management)
* [Pod Security](https://docs.microsoft.com/en-us/azure/aks/developer-best-practices-pod-security)
