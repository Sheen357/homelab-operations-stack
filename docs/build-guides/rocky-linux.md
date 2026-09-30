# Rocky Linux Operations Server

## Purpose

The Rocky Linux virtual machine provides hands-on Linux systems-administration practice and hosts the lab’s containerized monitoring services.

**Environment:** Home Lab  
**Virtualization platform:** Microsoft Hyper-V  
**Operational status:** Current

## Current Capabilities

- Rocky Linux administration
- SSH remote administration
- Tailscale remote connectivity
- Docker container management
- Docker Compose service orchestration
- Prometheus metrics collection
- Grafana dashboards
- Uptime Kuma availability monitoring
- cAdvisor container monitoring
- Node Exporter host monitoring
- Git and GitHub version control

## Administrative Tasks Practiced

- Navigating the Linux filesystem
- Managing files, directories, ownership, and permissions
- Checking system and service status
- Reviewing logs
- Installing updates and packages
- Managing Docker containers
- Validating Docker Compose configurations
- Troubleshooting network ports and service connectivity
- Using Git to track configuration and documentation changes

## Safe Validation Commands

### Operating System

```bash
cat /etc/os-release
uname -r
hostnamectl