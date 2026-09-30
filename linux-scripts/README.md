# Linux Administration Scripts

This directory contains sanitized Linux and Bash scripts created for the enterprise systems-administration home lab.

## Script Requirements

Each script must document:

- Purpose
- Home-lab environment
- Prerequisites
- Required permissions
- Arguments or environment variables
- Usage example
- Expected output
- Validation method
- Error behavior
- Rollback or recovery steps
- Production-environment considerations

## Security Rules

Scripts must not contain:

- Passwords
- Tokens
- Private keys
- Personal information
- Employer information
- Real public IP addresses
- Unprotected credentials

Use protected environment variables, configuration files excluded by `.gitignore`, or approved secret-management methods when authentication information is required.

## Planned Script Topics

- System-health reporting
- Disk-capacity checks
- Service-status checks
- Log collection
- Package-update checks
- Docker container validation
- Monitoring-target validation
- Backup verification
- Network-connectivity checks

Scripts will not be listed as completed experience until they have been tested and their results documented.