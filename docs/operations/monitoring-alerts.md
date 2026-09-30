# Monitoring and Alerting

## Purpose

The monitoring stack provides visibility into Linux host health, container performance, service availability, and operational issues within the home lab.

**Environment:** Home Lab  
**Status:** Current foundation with additional alerting planned

## Monitoring Components

### Prometheus

Prometheus collects and stores time-series metrics from configured targets.

Current uses:

- Collect Linux host metrics from Node Exporter
- Collect container metrics from cAdvisor
- Provide data for Grafana dashboards
- Validate whether configured monitoring targets are reachable

Safe validation:

```bash
docker compose config --services
docker ps
curl -fsS http://localhost:9090/-/healthy