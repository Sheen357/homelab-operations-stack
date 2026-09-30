# Enterprise Systems Administration Home Lab Design

## Purpose

Expand the existing `homelab-operations-stack` into a small enterprise-style environment for hands-on systems administration practice, technical documentation, and interview preparation.

All résumé and interview references will identify this work as home-lab experience rather than production experience.

## Success Criteria

Phase 1 is complete when:

- Rocky Linux continues operating as the monitoring and operations server.
- A Windows Server domain controller provides Active Directory and DNS.
- A Windows member server joins the domain.
- A Windows 11 client joins the domain.
- Users, groups, organizational units, and Group Policies are configured.
- Windows and Linux systems are monitored through the existing monitoring stack.
- Backups are stored separately from active virtual machines.
- At least one server or file restoration is successfully tested.
- Build records, troubleshooting reports, and interview explanations are documented in GitHub.

## Physical Host

- Windows 11 Pro streaming computer
- Hyper-V virtualization
- 32 GB RAM
- Dual-purpose streaming and lab system
- Lab virtual machines will be shut down before streaming
- Minimum recommended dedicated VM storage: 500 GB SSD
- Backups should reside on a separate physical drive

## Initial Virtual Machines

### Rocky Linux Operations Server

Existing virtual machine responsible for:

- Docker and Docker Compose
- Prometheus
- Grafana
- Uptime Kuma
- cAdvisor
- Node Exporter
- Tailscale remote administration

### Windows Domain Controller

Responsibilities:

- Active Directory Domain Services
- DNS
- User and computer authentication
- Organizational units
- Security groups
- Group Policy

Recommended resources:

- Two virtual processors
- 4 GB dynamic memory
- 80 GB dynamically expanding VHDX

### Windows Member Server

Responsibilities:

- Domain membership
- File services and NTFS permissions
- PowerShell administration
- Patching and configuration exercises
- Backup and recovery exercises

Recommended resources:

- Two virtual processors
- 4–6 GB dynamic memory
- 100 GB dynamically expanding VHDX

### Windows 11 Client

Responsibilities:

- Domain-joined workstation
- User login and authentication testing
- Group Policy validation
- Application and permission testing
- Desktop and network troubleshooting scenarios

Recommended resources:

- Two virtual processors
- 4 GB dynamic memory
- 100 GB dynamically expanding VHDX

## Implementation Phases

1. Document and validate the existing Rocky Linux monitoring environment.
2. Prepare Hyper-V storage and virtual networking.
3. Deploy the Windows domain controller.
4. Configure Active Directory, DNS, OUs, users, groups, and Group Policy.
5. Deploy and join the Windows 11 client.
6. Deploy and join the Windows member server.
7. Integrate Windows monitoring with the Rocky Linux monitoring stack.
8. Configure backups and perform restoration testing.
9. Create security, networking, and incident-response exercises.
10. Convert completed work into résumé entries and STAR interview stories.

## Documentation Structure

- `docs/architecture` — diagrams, network plan, and system inventory
- `docs/build-guides` — installation and configuration records
- `docs/operations` — monitoring, patching, backup, and recovery procedures
- `docs/incidents` — troubleshooting and root-cause reports
- `docs/interview` — experience log and STAR stories
- `powershell` — Windows administration and automation scripts
- `linux-scripts` — Linux administration and automation scripts

## Evidence Requirements

Each major lab activity must record:

- Objective
- Environment and tools used
- Configuration performed
- Validation method
- Problem encountered
- Troubleshooting steps
- Root cause
- Resolution
- Security or operational consideration
- Interview explanation
- Potential production differences

## Security Rules

The public repository must not contain:

- Passwords or authentication tokens
- Real public IP addresses
- Tailscale device information
- Private certificates or keys
- Personal user information
- Employer or customer information
- Screenshots containing sensitive data

Fictional accounts and sanitized example addresses will be used in documentation.

## Operational Constraints

- Lab virtual machines will be shut down before streaming.
- Virtual disks will use dynamically expanding VHDX files.
- Hyper-V checkpoints will be temporary and will not be treated as backups.
- Backups will be placed on a different physical disk when available.
- New systems will be introduced one at a time and validated before continuing.
- Changes will be documented and committed to GitHub by milestone.

## Phase 1 Deliverable

A documented Windows domain containing one domain controller, one member server, and one Windows client, supported by the existing Rocky Linux monitoring environment and a tested recovery process.