Monitors the GitHub Actions Runner Scale Set Controller (ARC) running on Kubernetes.

## Panels

- **Runner Pool** — registered, busy, idle, desired, min/max runners + autoscaler bounds over time
- **Job Throughput** — assigned/started/completed/running counts, job rate per minute, startup and execution duration (p50/p95)
- **Controller Health** — reconcile rate, errors, duration (p50/p95), active workers, work queue depth

## Requirements

- ARC installed in scale set mode (`helm install arc-controller`)
- Prometheus scraping ARC pods with `job` labels `arc-controller` and `arc-listeners`

## Template Variables

- `datasource` — select your Prometheus datasource

## Source

[PDGIII/Dashboards](https://github.com/PDGIII/Dashboards/tree/main/github-actions-arc-runner-scale-set)
