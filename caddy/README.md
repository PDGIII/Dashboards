# Caddy

Monitors a standalone Caddy reverse proxy using Caddy's built-in Prometheus metrics endpoint.

**Grafana.com:** [25216-caddy-standalone-reverse-proxy](https://grafana.com/grafana/dashboards/25216-caddy-standalone-reverse-proxy/)

## Screenshots

<!-- Add screenshots here -->

## Requirements

| Dependency | Version |
|------------|---------|
| Grafana    | 7.1+    |
| Prometheus | any     |
| Caddy      | 2.x     |

## Usage

Import `dashboard.json` via Grafana UI (**Dashboards → Import**) or place it in your
provisioning directory (`/etc/grafana/provisioning/dashboards/`).

Enable metrics in your Caddyfile:

```caddyfile
{
  metrics
}
```

Then configure Prometheus to scrape Caddy's admin API:

```yaml
- job_name: 'caddy'
  static_configs:
    - targets:
      - 'localhost:2019'
  metrics_path: /metrics
  scrape_interval: 30s
```
