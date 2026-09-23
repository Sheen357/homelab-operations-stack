# Homelab Operations Stack Architecture

## Purpose

This project provides monitoring and service-availability visibility for a Rocky Linux homelab server and its Docker containers.

## Platform

- Windows 11 Pro host
- Hyper-V
- Rocky Linux virtual machine
- Docker Engine with Docker Compose
- Tailscale for secure remote access
- GitHub for version control and documentation

## Monitoring Services

| Service | Purpose | Port |
|---|---|---:|
| Grafana | Dashboards and visualization | 3000 |
| Prometheus | Metrics collection and storage | 9090 |
| Node Exporter | Rocky Linux host metrics | 9100 |
| cAdvisor | Docker container metrics | 8080 |
| Uptime Kuma | Service availability monitoring | 3001 |

## Data Flow

1. Node Exporter collects Linux CPU, memory, disk, filesystem, and network metrics.
2. cAdvisor collects Docker container resource metrics.
3. Prometheus retrieves metrics from Node Exporter and cAdvisor.
4. Grafana queries Prometheus and displays dashboards.
5. Uptime Kuma checks whether selected services are reachable.
6. Tailscale provides remote access without public router port-forwarding.

## Security Boundaries

- No passwords, tokens, private IP addresses, or Tailscale keys are stored in GitHub.
- Configuration examples use environment variables or placeholder values.
- Monitoring services are not intentionally exposed to the public internet.
- Administrative dashboards are accessed through the home network or Tailscale.
- Persistent monitoring data is stored in Docker volumes on the Rocky Linux VM.

## Version 1 Scope

Version 1 monitors only the Rocky Linux VM and containers running on that VM. Windows monitoring, centralized logging, network-device monitoring, and automated alert delivery are future enhancements.