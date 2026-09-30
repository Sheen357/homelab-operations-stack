# PowerShell Scripts

This directory contains sanitized PowerShell scripts created for the enterprise systems-administration home lab.

## Script Requirements

Each script must document:

- Purpose
- Home-lab environment
- Prerequisites
- Required permissions
- Parameters
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

Use parameters, environment variables, or approved secret-management methods when authentication information is required.

## Planned Script Topics

- System inventory
- Computer and user lookup
- Active Directory reporting
- Group membership reporting
- Service-health checks
- Storage-capacity checks
- Patch-status reporting
- Event-log collection
- Backup validation
- Monitoring validation

Scripts will not be listed as completed experience until they have been tested and their results documented.