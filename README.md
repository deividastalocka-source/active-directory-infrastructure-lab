# Active Directory Infrastructure Lab

A Windows Server 2025 Active Directory lab designed to simulate a small business IT environment with centralised identity management, Group Policy, DNS, secure file sharing and Windows 11 domain administration.

The project demonstrates practical experience with technologies and support tasks commonly encountered in IT Support and Systems Administration roles.

## Architecture

![Network Topology](screenshots/Network%20Topology.png)

The environment was deployed in VMware Workstation Pro using a Windows Server 2025 Domain Controller and a Windows 11 Enterprise client.

| System | Role |
|---|---|
| DC01 | Windows Server 2025 Domain Controller |
| PC01 | Windows 11 Enterprise domain client |
| Domain | `home.lab` |
| Network | VMware NAT `192.168.79.0/24` |
| DC01 IP | `192.168.79.10` |

## Technologies

- Windows Server 2025
- Windows 11 Enterprise
- Active Directory Domain Services (AD DS)
- DNS
- Group Policy
- NTFS Permissions
- VMware Workstation Pro

## What I Built

### Active Directory

Deployed a Windows Server 2025 Domain Controller and created the `home.lab` Active Directory forest.

Configured:

- Organisational Units (OUs)
- Domain user accounts
- Departmental security groups
- Computer accounts
- DNS integration

### Windows 11 Domain Client

Deployed a Windows 11 Enterprise workstation and joined it to the `home.lab` domain.

Validated domain authentication, DNS resolution and Active Directory communication from the client.

### Group Policy

Created and applied a `Corporate Desktop Policy` to centrally manage domain users.

Configured policies including:

- Desktop wallpaper
- Control Panel restriction
- Run command restriction

### File Shares and Permissions

Created departmental network shares for:

- IT
- HR
- Finance
- Executive

Configured share and NTFS permissions using departmental security groups and tested both authorised and unauthorised access.

### IT Support Scenarios

Performed common Active Directory support tasks including:

- User account administration
- Password resets
- Account lockout recovery
- Group membership management
- File access troubleshooting
- Group Policy troubleshooting
- Domain connectivity and DNS troubleshooting

## Key Results

The completed environment successfully demonstrated:

- Centralised domain authentication
- Active Directory user and computer management
- DNS-based domain service discovery
- Group Policy enforcement
- Role-based access to departmental resources
- Windows 11 domain integration
- Password reset and account recovery procedures
- Infrastructure troubleshooting and validation

## Documentation

Detailed implementation documentation is available in the [`docs`](docs/) directory.

| Section | Documentation |
|---|---|
| 01 | [Project Overview](docs/01-project-overview.md) |
| 02 | [Lab Environment](docs/02-lab-environment.md) |
| 03 | [Solution Architecture](docs/03-solution-architecture.md) |
| 04 | [Server Deployment](docs/04-server-deployment.md) |
| 05 | [Active Directory Deployment](docs/05-active-directory-deployment.md) |
| 06 | [Organisational Structure](docs/06-organisational-structure.md) |
| 07 | [Domain Client Deployment](docs/07-domain-client-deployment.md) |
| 08 | [File Shares and Permissions](docs/08-file-shares-and-permissions.md) |
| 09 | [Group Policy](docs/09-group-policy.md) |
| 10 | [IT Support and Validation](docs/10-it-support-and-validation.md) |
| 11 | [Conclusion and Lessons Learned](docs/11-conclusion-and-lessons-learned.md) |

## Troubleshooting

Several issues were encountered and resolved during the project:

| Issue | Resolution |
|---|---|
| Domain join failed | Verified PC01 DNS configuration and connectivity to DC01 |
| Share access denied | Reviewed security group membership and NTFS permissions |
| Group Policy not applying | Used `gpupdate /force` and verified OU placement |
| User account locked | Unlocked the account through Active Directory Users and Computers |
| AD DS prerequisite check failed | Corrected the Administrator password configuration and repeated validation |

## Skills Demonstrated

- Windows Server Administration
- Active Directory Domain Services
- User and Group Administration
- Identity and Access Management
- DNS Administration
- Group Policy Management
- NTFS and Share Permissions
- Windows 11 Administration
- IT Support Troubleshooting
- Virtualisation
- Technical Documentation

## Future Improvements

Potential future extensions include:

- Secondary Domain Controller
- DHCP
- Windows Server Update Services (WSUS)
- PowerShell user provisioning
- Microsoft Entra ID integration
- Microsoft 365 administration

## Repository Structure

```text
active-directory-infrastructure-lab/
├── docs/
│   ├── 01-project-overview.md
│   ├── 02-lab-environment.md
│   ├── 03-solution-architecture.md
│   ├── 04-server-deployment.md
│   ├── 05-active-directory-deployment.md
│   ├── 06-organisational-structure.md
│   ├── 07-domain-client-deployment.md
│   ├── 08-file-shares-and-permissions.md
│   ├── 09-group-policy.md
│   ├── 10-it-support-and-validation.md
│   └── 11-conclusion-and-lessons-learned.md
├── screenshots/
│   ├── 01 - Virtual Machine Created.png
│   ├── ...
│   ├── 76 - Group Policy Validation.png
│   └── Network Topology.png
├── LICENSE
└── README.md
