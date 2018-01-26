# kubernetes-prometheus
Configuration files for setting up prometheus monitoring on Kubernetes cluster.

You can find the full tutorial from here https://devopscube.com/setup-prometheus-monitoring-on-kubernetes/

# Monitoring Pod

Example scrape config for pods

The relabeling allows the actual pod scrape endpoint to be configured via the following annotations:

* `prometheus.io/scrape`: Only scrape pods that have a value of `true`
* `prometheus.io/path`: If the metrics path is not `/metrics` override this.
* `prometheus.io/port`: Scrape the pod on the indicated port instead of the
 pod's declared ports (default is a port-free target if none are declared).


# Ref
1. [Detail configuration](https://github.com/prometheus/prometheus/blob/master/documentation/examples/prometheus-kubernetes.yml)