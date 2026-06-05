# ACM Multicluster Observability

> **Disclaimer:** This repository is prepared for **demonstration and educational purposes only**. The configurations, thresholds, and examples used here are simplified to illustrate concepts and are not intended for production use. Always review and adapt the configurations to your environment's requirements, security policies, and best practices before applying them to production clusters. Additionally, some components used in these demos (e.g., MinIO) are **not supported or maintained by Red Hat** and are included solely for demonstration convenience.

This repository contains hands-on demos for ACM multicluster observability. It covers end-to-end setup of the observability stack, custom dashboarding with Grafana and Perses, custom alerting and recording rules with metrics forwarding from managed clusters, and user workload monitoring integration.

The demos use ACM 2.16 with MinIO as the object storage backend. Both the standard observability stack and the Multicluster Observability Add-on (MCOA) are covered.

> **Prerequisites:**
> - ACM installed on the hub cluster (2.15/2.16 recommended)
> - At least one managed cluster imported (`local-cluster` + `additional`)

---

## Topics

1. **[MCO Install & Configuration](docs/1.mco-install.md)** : MultiClusterObservability CR setup, MinIO object storage, SNO considerations. Includes both standard and MCOA metrics collection options.

2. **[Metrics UI & Dashboards](docs/2.metrics_ui_dashboard.md)** : Dashboarding and visualization options for ACM observability.

3. **[Spoke Clusters Metrics Collection](docs/3.metricscollection.md)** : Two mutually exclusive methods to collect metrics from managed clusters (standard metrics-collector vs MCOA).

4. **[User Workload Monitoring](docs/4.user_worload_monitoring.md)** : Forwarding user workload metrics and alerts from managed clusters to the hub, using either the standard or MCOA stack.
