# Home Lab Network Plan

## Purpose

This document defines the proposed network design for the enterprise systems-administration home lab. The design supports Windows domain services, Linux operations, monitoring, remote administration, and future security exercises.

**Environment:** Home Lab
**Status:** Proposed
**Implementation:** Not yet completed

## Design Principles

- Keep lab systems separate from normal household devices when possible.
- Use private addresses only.
- Provide controlled internet access for updates and installation.
- Allow communication between approved lab systems.
- Document all required ports and dependencies.
- Avoid exposing administrative services directly to the internet.
- Use Tailscale or another approved secure-access method for remote administration.
- Do not publish actual home-network or Tailscale addresses.

## Proposed Systems

| System | Proposed Hostname | Primary Function |
|---|---|---|
| Hyper-V Host | `LAB-HV01` | Virtualization host |
| Rocky Linux Server | `LAB-LNX01` | Containers, monitoring, and Linux administration |
| Domain Controller | `LAB-DC01` | Active Directory and DNS |
| Member Server | `LAB-SRV01` | File services, administration, and recovery exercises |
| Windows Client | `LAB-CL01` | Domain-client and troubleshooting exercises |

Hostnames may be adjusted during implementation. Final names must be recorded in the system inventory.

## Proposed Domain

The Windows lab will use a nonpublic internal domain name reserved for testing.

Example sanitized domain:

```text
ad.morilab.test