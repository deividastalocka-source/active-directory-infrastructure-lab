# Conclusion and Lessons Learned

## Skills Demonstrated

This project provided practical experience across Windows Server administration, Active Directory and common IT support operations.

Key skills demonstrated include:

- Windows Server 2025 Administration
- Active Directory Domain Services (AD DS)
- DNS Administration
- Group Policy Management
- VMware Workstation Pro
- Windows 11 Enterprise Administration
- NTFS Permissions
- Network Shares
- Identity and Access Management
- IT Support Troubleshooting
- Technical Documentation

## Lessons Learned

This project strengthened practical knowledge of enterprise Windows administration by combining infrastructure deployment with real-world IT support scenarios.

It highlighted the importance of planning, validation, documentation and troubleshooting throughout an infrastructure deployment.

The project also demonstrated how Active Directory components work together. DNS enables domain clients to locate Active Directory services, security groups simplify access management, Group Policy provides centralised configuration and NTFS permissions control access to organisational resources.

## Troubleshooting Summary

Several issues were encountered and resolved during the deployment.

| Issue | Resolution | Outcome |
|---|---|---|
| Domain join failed | Verified DNS pointed to DC01 and confirmed connectivity | PC01 joined the domain successfully |
| Share access denied | Reviewed security group membership and NTFS permissions | Authorised users received correct access |
| GPO not applying | Forced `gpupdate /force` and verified OU placement | Policies applied successfully |
| Account locked | Unlocked the account in Active Directory Users and Computers | User authenticated successfully |

These scenarios demonstrated a structured troubleshooting process involving identifying the affected service, reviewing the configuration, applying a corrective action and validating the result.

## Operational Best Practices

The following practices were followed throughout the deployment to improve stability, maintainability and recoverability:

- Assign a static IP address before promoting a Domain Controller.
- Use the Domain Controller as the preferred DNS server for domain members.
- Create VMware snapshots before major configuration changes.
- Manage permissions through security groups instead of individual user accounts.
- Apply the principle of least privilege when configuring share and NTFS permissions.
- Validate each configuration change before progressing to the next deployment stage.
- Document significant configuration steps with supporting evidence.

## Future Improvements

The environment could be expanded further by:

- Deploying a secondary Domain Controller.
- Implementing DHCP and WSUS.
- Automating user provisioning with PowerShell.
- Integrating Microsoft Entra ID and Microsoft 365.
- Deploying a dedicated help desk platform for additional support simulations.

## Technologies Used

| Technology | Purpose |
|---|---|
| Windows Server 2025 Standard | Domain Controller and server infrastructure |
| Windows 11 Enterprise | Domain-joined client workstation |
| VMware Workstation Pro | Virtualisation platform |
| Active Directory Domain Services | Centralised identity and domain management |
| DNS | Domain name resolution and Active Directory service discovery |
| Group Policy | Centralised user and workstation configuration |
| NTFS | File system permissions and access control |

## Acronyms

| Acronym | Meaning |
|---|---|
| AD DS | Active Directory Domain Services |
| DNS | Domain Name System |
| GPO | Group Policy Object |
| OU | Organisational Unit |
| NTFS | New Technology File System |
| VM | Virtual Machine |

## Conclusion

The project successfully delivered a functional Windows Server 2025 Active Directory environment capable of supporting centralised authentication, policy management and secure resource access.

The completed lab demonstrates practical experience with technologies commonly encountered in entry-level IT Support and Systems Administration roles. It also provides a reusable environment that can be expanded with additional Windows Server, automation and cloud administration technologies.

---

[← Previous: IT Support and Validation](10-it-support-and-validation.md) | [Back to Project Overview](01-project-overview.md)
