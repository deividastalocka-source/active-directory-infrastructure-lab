# Lab Environment

The Active Directory lab was deployed in a virtualised environment using VMware Workstation Pro. The environment consists of a Windows Server 2025 domain controller and a Windows 11 Enterprise client workstation.

## Environment Configuration

| Component | Configuration |
|---|---|
| Host OS | Windows 11 |
| Hypervisor | VMware Workstation Pro |
| Server | DC01 - Windows Server 2025 |
| Client | PC01 - Windows 11 Enterprise |
| Domain | `home.lab` |
| Primary Service | Active Directory Domain Services |

## Core Technologies

- Windows Server 2025
- Windows 11 Enterprise
- VMware Workstation Pro
- Active Directory Domain Services (AD DS)
- DNS
- Group Policy
- NTFS Permissions

## Environment Roles

### DC01

DC01 serves as the central Windows Server 2025 domain controller for the environment. It provides:

- Active Directory Domain Services
- DNS
- Group Policy management
- User and group administration
- Departmental file shares

### PC01

PC01 is a Windows 11 Enterprise workstation used to represent an employee endpoint within the environment.

The workstation is joined to the `home.lab` domain and is used to validate:

- Domain authentication
- DNS resolution
- Group Policy application
- Network share access
- User account administration

---

[← Previous: Project Overview](01-project-overview.md) | [Next: Solution Architecture →](03-solution-architecture.md)
