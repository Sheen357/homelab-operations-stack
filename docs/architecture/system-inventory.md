# System Inventory

## Inventory Rules

- This inventory contains sanitized home-lab information.
- Passwords, tokens, public IP addresses, private keys, and personal information are excluded.
- `Current` means the component has been deployed.
- `Planned` means the component has not yet been deployed or validated.

## Physical Systems

| System | Platform | Purpose | Status |
|---|---|---|---|
| Hyper-V Host | Windows 11 Pro | Hosts lab virtual machines and supports streaming activities | Current |
| Work Laptop | Windows | Provides remote administrative access through approved tools | Current |

## Virtual Machines

| System | Operating System | Purpose | Hypervisor | Status |
|---|---|---|---|---|
| Rocky Operations Server | Rocky Linux | Linux administration, containers, monitoring, and remote-access practice | Hyper-V | Current |
| Domain Controller | Windows Server | Active Directory, DNS, authentication, and Group Policy | Hyper-V | Planned |
| Member Server | Windows Server | File services, permissions, patching, PowerShell, and recovery testing | Hyper-V | Planned |
| Domain Client | Windows 11 | Domain login, Group Policy, software, and troubleshooting exercises | Hyper-V | Planned |

## Current Services

| Service | Location | Purpose | Status |
|---|---|---|---|
| Docker Engine | Rocky Operations Server | Runs containerized lab services | Current |
| Docker Compose | Rocky Operations Server | Defines and manages the monitoring stack | Current |
| Prometheus | Rocky Operations Server | Collects and stores infrastructure metrics | Current |
| Grafana | Rocky Operations Server | Displays dashboards and monitoring data | Current |
| Uptime Kuma | Rocky Operations Server | Performs service and availability checks | Current |
| cAdvisor | Rocky Operations Server | Collects container resource metrics | Current |
| Node Exporter | Rocky Operations Server | Exposes Linux host metrics to Prometheus | Current |
| SSH | Rocky Operations Server | Provides command-line administration | Current |
| Tailscale | Lab environment | Provides secured remote connectivity | Current |
| Git/GitHub | Lab environment | Stores version-controlled configurations and documentation | Current |

## Planned Windows Services

| Service | Planned Location | Purpose | Status |
|---|---|---|---|
| Active Directory Domain Services | Domain Controller | Centralized identity and authentication | Planned |
| DNS | Domain Controller | Internal hostname resolution | Planned |
| Group Policy | Domain Controller | Centralized Windows configuration and security policies | Planned |
| File Services | Member Server | Shared folders and NTFS permission exercises | Planned |
| Windows Monitoring Exporter | Windows servers and client | Provides Windows metrics to the monitoring stack | Planned |
| Backup Service | Separate storage target | Protects lab systems and supports restoration testing | Planned |

## Storage Plan

| Storage Use | Minimum Target | Status |
|---|---:|---|
| Active virtual machines | 500 GB SSD | Planned |
| Backup and recovery data | Separate physical drive | Planned |
| Installation media and temporary files | Secondary storage | Planned |

Hyper-V checkpoints will be used only for short-term testing and will not be treated as backups.

## Update Procedure

Update this inventory whenever a system or service is:

- Deployed
- Reconfigured
- Upgraded
- Migrated
- Decommissioned
- Restored from backup

A planned item must not be changed to current until its configuration and validation have been documented.