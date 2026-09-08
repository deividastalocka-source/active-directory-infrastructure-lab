# Group Policy

This section documents the configuration and validation of Group Policy within the Active Directory environment. Group Policy is used to centrally manage and enforce workstation settings for domain users.

## Step 25 — Configure Group Policy

### Purpose

Create and link a Group Policy Object (GPO) to centrally manage user settings within the domain.

### Procedure

1. Open Group Policy Management on DC01.
2. Create a new GPO named `Corporate Desktop Policy`.
3. Link the GPO to the appropriate Users OU.
4. Configure the desktop wallpaper policy.
5. Configure a restriction preventing users from accessing Control Panel.
6. Configure a restriction preventing users from accessing the Run command.
7. Update Group Policy on PC01.
8. Sign in with a domain user account and verify that the restrictions are applied.

### Verification

The configured Group Policy settings are successfully applied to the domain client after the policy refresh. The user is prevented from accessing Control Panel and the Run command is removed.

### Evidence

![Group Policy Management Console](../screenshots/57%20-%20Group%20Policy%20Management%20Console.png)

![Corporate Desktop Policy Created](../screenshots/58%20-%20Corporate%20Desktop%20Policy%20Created.png)

![Configuring Desktop Wallpaper Policy](../screenshots/59%20-%20Configuring%20Desktop%20Wallpaper%20Policy.png)

![Control Panel Restriction Policy](../screenshots/60%20-%20Control%20Panel%20Restriction%20Policy.png)

![Run Command Restriction Policy](../screenshots/61%20-%20Run%20Command%20Restriction%20Policy.png)

![Control Panel Restricted](../screenshots/62%20-%20Control%20Panel%20Restricted.png)

![Run Command Removed](../screenshots/63%20-%20Run%20Command%20Removed.png)

---

[← Previous: File Shares and Permissions](08-file-shares-and-permissions.md) | [Next: IT Support and Validation →](10-it-support-and-validation.md)
