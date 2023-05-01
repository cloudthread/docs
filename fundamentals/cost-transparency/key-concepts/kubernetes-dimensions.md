# Kubernetes Dimensions

**Kubernetes Dimensions** is a feature allowing for [performing-k8s-cost-analysis.md](../../../guides/monitoring-cloud-costs/performing-k8s-cost-analysis.md "mention").

{% hint style="info" %}
**Cluster**, **Namespace**, **Pod**, **Label** are currently available as Kubernetes Dimensions in Filter Pane of [costs-overview.md](../costs-overview.md "mention") section.
{% endhint %}

Cloudthread is performing container cost allocation for Kubernetes by distributing EC2 instance costs billed by AWS to K8s containers based on [Prometheus](https://prometheus.io/) monitoring data. We use container **CPU**, **Memory** and **Network** consumption data metrics as the basis for cost allocation.
