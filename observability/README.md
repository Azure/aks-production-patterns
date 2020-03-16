# Observability

The observability section is all about what things to log and monitor as part of operating an AKS cluster day to day.

## Challenge

You've been tasked with improving the observability of your existing AKS clusters. There are mutiple clusters and the organization does not have a great line of sight into what is working, and what is not working correctly within the cluster. The ask from the CTO is to create a dashboard that provides the necessary visibility into the AKS clusters so that proactive vs reactive operations can take place.

### Infrastructure Monitoring #1

Your first challenge is to create a dashboard that provides visibility into the underlying VMs that AKS is using. Monitoring CPU and Memory is important as these are the core resources that applications use and if these resources are not availablt then workloads will not be able to be deployed. Storage is important because if new container images are not able to be pulled down to a Node then workloads cannot be deployed, or application logs will not be able to be captured which will make troubleshooting tough. Networking is important as this is a distributed system and distributed systems can be overly chatted if not architected correctly.

### Infrastructure Monitoring #2

Your second challenge is to detect when **Nodes Not Ready**. This indicates that a Node is not operating correctly which means workloads might not be able to be scheduled, or maybe not even running. The typical issue this is mitigating against is misconfigured network communication, usually firewall, between the worker nodes and AKS control plane.

### Infrastructure Monitoring #3

Your third challenge is to detect when **Pods Restart**. Similar to Nodes Not Ready, this indicates a problem at the application level versus the Infrastructure level. Pods could be restarting due to the container not starting up properly , or Out of Memory (OOM).

### Infrastructure Monitoring #4

Your fourth challenge is to detect when **Deployments are Not Ready**. This is simlar to Pods restarting, but how do you detect a workload deployment problem if the Pod does not even startup? Typical problems in this area are Pods not able to be scheduled due to Cluster resource capacity or a desired Node not found.

## Success Criteria

* Show cluster CPU, Memory, Disk Storage and Network and metrics queries.
* Show which Pods in the cluster are restarting and supporting queries.
* Show which deployments are not starting up correctly and supporting queries.
* Wrap all of the above in a single dashboard or set of dashboards to provide single pane of glass visibility.

## References

Prometheus & Grafana (Metrics)

* [Prometheus Operator](https://github.com/coreos/prometheus-operator)

Azure Monitor for Containers (Logging)

* [Azure Monitor for Containers](https://docs.microsoft.com/en-us/azure/azure-monitor/insights/container-insights-analyze)
* [Querying Logs](https://docs.microsoft.com/en-us/azure/azure-monitor/insights/container-insights-log-search)

Azure

* [Performance Alerts with Azure Monitor for Containers](https://docs.microsoft.com/bs-latn-ba/azure/azure-monitor/insights/container-insights-alerts)
