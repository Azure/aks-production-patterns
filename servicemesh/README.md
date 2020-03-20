# Service Mesh

This service mesh section is to help organizations determine if a service mesh is really needed within their organization.

## Exercise

You've been tasked with investigating wether or not your organization requires the additional complexity that comes with adding a Service Mesh. Maybe you do, but do you need it on Day 1? The ask from the CTO and Security Team is to help them understand where a Service Mesh provides value. Can Service Mesh technologies be addressed by existing Monitoring + Logging + Security solutions?

### Service Mesh #1

Your first challenge is to install Linkerd into your cluster and secure communication between two pods.

### Service Mesh #2

Your second challenge is to determine the success rate and requests per second (RPS) between your two pods. Use the RPS values to build a Horizontal Pod Autoscaler (HPA).

## Success Criteria

* Demonstrate Linkerd is installed and functioning correctly by showing that pod to pod communication is secure with mTLS (certificates).
* Demonstrate that your application workload automatically scales if the requests per second are exceeded.

## References

Linkerd

* [Linkerd](https://linkerd.io/2/tasks/install/)

Flagger

* [Flagger](https://docs.flagger.app/)

Prometheus Metrics Adapter

* [Prometheus Metrics Adapter](https://github.com/helm/charts/tree/master/stable/prometheus-adapter)

Azure

* [About Service Meshes](https://docs.microsoft.com/en-us/azure/aks/servicemesh-about)
