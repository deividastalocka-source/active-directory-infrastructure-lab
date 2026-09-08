# Solution Architecture

## Network Topology

The Active Directory environment was designed as a small business network hosted within VMware Workstation Pro.

![Network Topology](../screenshots/Network%20Topology.png)

## Architecture Overview

The environment consists of two primary virtual machines connected through a VMware NAT network.

### DC01 — Domain Controller

DC01 is a Windows Server 2025 server that provides the central infrastructure services for the domain.

**Services:**

- Active Directory Domain Services (AD DS)
- DNS
- Group Policy
- Departmental file shares

**Network Configuration:**

- IPv4 Address: `192.168.79.10`
- Subnet Mask: `255.255.255.0`
- Default Gateway: `192.168.79.2`
- DNS Server: `192.168.79.10`

### PC01 — Domain Client

PC01 is a Windows 11 Enterprise workstation representing an employee endpoint connected to the Active Directory environment.

**Network Configuration:**

- IPv4 Address: `192.168.79.20`
- Subnet Mask: `255.255.255.0`
- Default Gateway: `192.168.79.2`
- DNS Server: `192.168.79.10`

## Domain Architecture

Both systems operate within the `home.lab` Active Directory domain.

DC01 provides centralised authentication, DNS resolution, Group Policy management and access to shared resources. PC01 communicates with DC01 to locate domain services, authenticate domain users and receive centrally managed policies.

The environment uses the VMware NAT network `192.168.79.0/24`, which provides connectivity between the virtual machines while allowing access outside the virtual environment.

---

[← Previous: Lab Environment](02-lab-environment.md) | [Next: Server Deployment →](04-server-deployment.md)
