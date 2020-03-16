# Cluster Management

This clsuter management section is all about AKS Cluster Management. The main focus areas are managing multiple clusters with a GitOps approach, patching clusters, and how to manage upgrading.

## Challenge

You've been tasked with improving the managment of your existing AKS clusters. There are mutiple clusters and they are not all configured in the same way which means that not all clusters have everything the organization needs to operate them. The ask from the CTO and Security Team is to ensure that all clusters have the necessary software the organization needs, this includes run-time monitoring software and Namespace RBAC + Limits + Quotas.

### GitOps #1

Your first challenge is to install a Flux Operator into your cluster and point it to the **gitops-baseconfig** directory of the forked repo.

### GitOps #2

Your second challenge is to install a second Flux Operator into your cluster and point it to the **gitops-clsuterconfig** directory of the forked repo.

## Success Criteria

* **Falco** should be running in your cluster.
* There should be 7 namespaces created (dev, staging, production, falco, ingress, aadpodidentity, dummy-ns).
* There should be 2 Flux Operators running side by side.
* Delete the suumy-ns and within a couple of mins the namespace should come back.

## References

GitOps

* [Guide to GitOps](https://www.weave.works/technologies/gitops/)

Flux Operator

* [Flux Docs](https://fluxcd.io/)

Azure

* [Azure ARC for Kubernetes - Coming Soon]()
