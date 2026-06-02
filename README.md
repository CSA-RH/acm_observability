# ACM Multicluster Observability

> **Disclaimer:** This repository is prepared for **demonstration and educational purposes only**. The configurations, thresholds, and examples used here are simplified to illustrate concepts and are not intended for production use. Always review and adapt the configurations to your environment's requirements, security policies, and best practices before applying them to production clusters. Additionally, some components used in these demos (e.g., MinIO) are **not supported or maintained by Red Hat** and are included solely for demonstration convenience.

This repository contains hands-on demos for ACM multicluster observability. It covers end-to-end setup of the observability stack, custom dashboarding with Grafana and Perses, custom alerting and recording rules with metrics forwarding from managed clusters, and user workload monitoring integration.

The demos use ACM 2.16 with MinIO as the object storage backend. Both the standard observability stack and the Multicluster Observability Add-on (MCOA) are covered.

> **Prerequisites:**
> - ACM installed on the hub cluster (2.15/2.16 recommended)
> - At least one managed cluster imported (or `local-cluster` self-managed)

---

## Topics

1. **[MCO Install & Configuration](docs/1.mco-install.md)** : MultiClusterObservability CR setup, MinIO object storage, SNO considerations.

2. **[Grafana Developer Instance](docs/2.grafana-dev-configuration_and_demo.md)** : Deploy the `grafana-dev` auxiliary instance for visual dashboard design, create custom dashboards as ConfigMaps.

3. **[Custom Alerts, Recording Rules, and Metrics](docs/3.metrics_alerts-recordrules.md)** : Two mutually exclusive methods to collect metrics from managed clusters.

4. **[Grafana Operator (Community)](docs/4.grafana-operator-configuration.md)** : Integration of the community Grafana Operator with the ACM observability stack (Thanos/Observatorium). Not officially supported by Red Hat.

5. **[User Workload Monitoring](docs/5.uwm-configuration_and_demo.md)** : Forwarding user workload metrics and alerts from managed clusters to the hub.

6. **[Perses Dashboards](docs/6.perses-configuration_and_demo.md)** : Install the Cluster Observability Operator (COO), enable Perses via UIPlugin, create Perses dashboards with multicluster metrics from ACM's Thanos.
