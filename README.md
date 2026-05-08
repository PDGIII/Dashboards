# Homelab Dashboards

Grafana dashboards for homelab monitoring.

## Dashboards

| Dashboard                                                                     | Description                                                      | Grafana.com                                                                                          |
|-------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [GitHub Actions ARC - Runner Scale Set](github-actions-arc-runner-scale-set/) | Monitors ARC runner scale sets on Kubernetes                     | [#25015](https://grafana.com/grafana/dashboards/25015-github-actions-arc-runner-scale-set/)          |
| [Caddy - Standalone Reverse Proxy](caddy/)                                    | Monitors a standalone Caddy reverse proxy via Prometheus metrics | [#25216](https://grafana.com/grafana/dashboards/25216-caddy/)                                        |

## Import

Each folder contains a `dashboard.json` that can be imported via **Dashboards → Import** in Grafana,
or provisioned automatically by placing it in `/etc/grafana/provisioning/dashboards/`.
