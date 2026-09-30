# Homelab Operations Stack

A personal enterprise systems-administration home lab for hands-on infrastructure practice, troubleshooting, automation, monitoring, recovery testing, and interview preparation.

This repository documents home-lab experience. It does not represent a production customer or employer environment.

## Current Environment

The current lab includes:

- Windows 11 Pro Hyper-V host
- Rocky Linux virtual machine
- Docker and Docker Compose
- Prometheus
- Grafana
- Uptime Kuma
- cAdvisor
- Node Exporter
- SSH
- Tailscale remote-access connectivity
- Git and GitHub configuration management

## Planned Expansion

The next phase will add:

- Windows Server domain controller
- Active Directory Domain Services
- DNS
- Organizational units, users, groups, and Group Policy
- Windows Server member server
- Windows 11 domain client
- Windows monitoring integration
- Backup and restoration testing
- Network and security troubleshooting scenarios
- PowerShell administration and automation

Planned systems will not be described as completed experience until they have been deployed and validated.

## Monitoring Services

The Docker Compose monitoring stack contains:

| Service | Purpose |
|---|---|
| Prometheus | Collects and stores infrastructure metrics |
| Grafana | Displays dashboards and monitoring data |
| Uptime Kuma | Performs service and availability checks |
| cAdvisor | Collects container resource metrics |
| Node Exporter | Exposes Linux host metrics |

List the configured services:

```bash
docker compose config --services