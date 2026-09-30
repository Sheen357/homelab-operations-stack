# Home Lab Overview

## Purpose

This repository documents a personal enterprise systems-administration home lab used for hands-on training, troubleshooting practice, automation, and interview preparation.

The environment is designed to demonstrate practical experience with Linux administration, containers, infrastructure monitoring, remote access, Windows Server, identity services, networking, backup and recovery, and technical documentation.

All work described in this repository is home-lab experience and does not represent a production customer or employer environment.

## Physical Environment

The lab runs on a Windows 11 Pro computer that serves two purposes:

- Hyper-V virtualization host
- Dedicated streaming computer

The computer is not used for gaming. Lab virtual machines will be shut down before streaming when additional system resources are required.

Confirmed host resources:

- Windows 11 Pro
- Hyper-V
- 32 GB RAM
- Multiple storage devices available or planned for active virtual machines and backups

## Current Environment

### Rocky Linux Virtual Machine

The existing Rocky Linux virtual machine provides Linux administration practice and hosts containerized monitoring services.

Confirmed technologies include:

- Rocky Linux
- Hyper-V
- Docker
- Docker Compose
- SSH
- Tailscale remote-access connectivity
- Git and GitHub

### Monitoring Stack

The current Docker Compose monitoring stack contains:

- Prometheus
- Grafana
- Uptime Kuma
- cAdvisor
- Node Exporter

These services provide experience with availability monitoring, system metrics, container metrics, dashboards, service validation, configuration management, and troubleshooting.

## Planned Windows Environment

The following systems are planned but are not yet deployed:

- Windows Server domain controller
- Active Directory Domain Services
- DNS
- Organizational units, users, groups, and Group Policy
- Windows Server member server
- Windows 11 domain client
- Windows monitoring integration
- Backup and restoration testing
- Network segmentation and security exercises

Planned components will not be listed as completed experience until they are deployed and validated.

## Operating Model

The lab will use a phased implementation approach:

1. Document and validate the existing Rocky Linux and monitoring environment.
2. Prepare dedicated Hyper-V storage and networking.
3. Deploy and validate Windows domain services.
4. Add a Windows client and member server.
5. Integrate Windows monitoring and alerting.
6. Configure and test backup and recovery.
7. Perform documented troubleshooting and security exercises.

Each phase will be completed and validated before the next phase begins.

## Evidence and Documentation

Major activities will include:

- Build documentation
- Validation commands and results
- Troubleshooting records
- Root-cause analysis
- Incident reports
- PowerShell or Linux scripts
- Recovery results
- Interview explanations
- Sanitized screenshots when appropriate

Passwords, tokens, private keys, certificates, personal information, public IP addresses, and employer information will not be stored in this repository.