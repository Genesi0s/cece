# Infrastructure — Monitoring

Stack de monitoring avec Prometheus et Grafana.

## Architecture

```
monitoring/
├── prometheus.yml    # Scrape config
├── grafana/
└── data/
```

## Lancer la stack

```bash
# Prometheus
prometheus --config.file=monitoring/prometheus.yml

# Grafana
grafana-server --homepath=/usr/share/grafana
```

## Prometheus — scrape config

```yaml
scrape_configs:
  - job_name: 'metrics'
    static_configs:
      - targets: ['localhost:8000']
```
