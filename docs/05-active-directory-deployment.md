# Active Directory Deployment

This section documents the installation of Active Directory Domain Services (AD DS), creation of the `home.lab` forest, promotion of DC01 to a Domain Controller and verification of the DNS infrastructure.

## Step 7 — Install Active Directory Domain Services

### Purpose

Launch the Add Roles and Features Wizard and begin installing AD DS.

### Procedure

1. Open Server Manager.
2. Select **Manage > Add Roles and Features**.
3. Choose Role-based installation.
4. Select Active Directory Domain Services.
5. Accept the required management tools and continue.

### Verification

AD DS installation completes successfully and the server is ready for promotion.

### Evidence

![Add Roles and Features Wizard](../screenshots/07%20-%20Add%20Roles%20and%20Features%20Wizard.png)

![Server Selection](../screenshots/08%20-%20Server%20Selection.png)

![Active Directory Installation Confirmation](../screenshots/09%20-%20Active%20Directory%20Installation%20Confirmation.png)

![Active Directory Installation in Progress](../screenshots/10%20-%20Active%20Directory%20Installation%20in%20Progress.png)

![Active Directory Installation Complete](../screenshots/11%20-%20Active%20Directory%20Installation%20Complete.png)

---

## Step 8 — Promote the Server to a Domain Controller

### Purpose

Begin the process of creating a new Active Directory forest and promoting DC01 to the first Domain Controller.

### Procedure

1. Select **Promote this server to a domain controller**.
2. Launch the AD DS Configuration Wizard.

### Evidence

![Promote Server to Domain Controller](../screenshots/12%20-%20Promote%20Server%20to%20Domain%20Controller.png)

---

## Step 9 — Verify AD DS Installation

### Purpose

Confirm that AD DS and the supporting management tools were installed successfully.

### Procedure

1. Review the installation status.
2. Confirm AD DS installation completed successfully.
3. Verify that the option to promote the server to a Domain Controller is available.

### Verification

The server is ready to be promoted to the first Domain Controller.

---

## Step 10 — Create the Active Directory Forest

### Purpose

Deploy a new Active Directory forest named `home.lab`.

### Procedure

1. Launch the AD DS Configuration Wizard.
2. Select **Add a new forest**.
3. Enter `home.lab` as the root domain name.
4. Review the deployment settings.

### Verification

The new Active Directory forest is configured and ready for deployment.

### Evidence

![Deployment Configuration](../screenshots/13%20-%20Deployment%20Configuration.png)

![Root Domain Name - home.lab](../screenshots/14%20-%20Root%20Domain%20Name%20-%20home.lab.png)

---

## Step 11 — Configure Domain Controller Options

### Purpose

Configure functional levels, DNS and recovery settings for the Domain Controller.

### Procedure

1. Select the Forest and Domain Functional Levels.
2. Enable the DNS Server role.
3. Configure the Directory Services Restore Mode (DSRM) password.
4. Review the additional Domain Controller settings.
5. Review the DNS delegation options.
6. Confirm the NetBIOS domain name.

### Verification

The Domain Controller configuration satisfies the deployment requirements.

### Evidence

![Domain Controller Options](../screenshots/15%20-%20Domain%20Controller%20Options.png)

![DNS Options](../screenshots/16%20-%20DNS%20Options.png)

![NetBIOS Domain Name](../screenshots/17%20-%20NetBIOS%20Domain%20Name.png)

---

## Step 12 — Review Database Paths

### Purpose

Review the storage locations for the Active Directory database, log files and SYSVOL.

### Procedure

1. Review the default NTDS database location.
2. Review the transaction log location.
3. Review the SYSVOL location.
4. Accept the default paths.

### Verification

The default storage locations are retained.

### Evidence

![Active Directory Database Paths](../screenshots/18%20-%20Active%20Directory%20Database%20Paths.png)

---

## Step 13 — Validate the Deployment

### Purpose

Review the deployment configuration and perform prerequisite checks before installing Active Directory.

### Procedure

1. Review the configuration summary.
2. Run prerequisite validation.
3. Resolve any reported issues.
4. Run the prerequisite check again.
5. Confirm the deployment is ready.

During validation, the prerequisite check initially failed because of the Administrator password configuration. The issue was corrected before the check was repeated successfully.

### Verification

All prerequisite checks pass successfully before installation.

### Evidence

![Review Active Directory Configuration](../screenshots/19%20-%20Review%20Active%20Directory%20Configuration.png)

![Prerequisites Check Failed - Administrator Password](../screenshots/20%20-%20Prerequisites%20Check%20Failed%20-%20Administrator%20Password.png)

![Active Directory Prerequisites Check Passed](../screenshots/21%20-%20Active%20Directory%20Prerequisites%20Check%20Passed.png)

---

## Step 14 — Complete Domain Controller Promotion

### Purpose

Install Active Directory and complete the promotion of DC01.

### Procedure

1. Start the installation.
2. Allow the server to restart automatically.
3. Sign in using the domain administrator account.
4. Open Server Manager and verify the domain.

### Verification

DC01 is successfully promoted as the first Domain Controller for the `home.lab` forest.

### Evidence

![Active Directory Installation Started](../screenshots/22%20-%20Active%20Directory%20Installation%20Started.png)

![DC01 Successfully Promoted to Domain Controller](../screenshots/23%20-%20DC01%20Successfully%20Promoted%20to%20Domain%20Controller.png)

---

## Step 15 — Verify DNS Configuration

### Purpose

Confirm that DNS is correctly configured and that the required Active Directory DNS zones and records were created.

### Procedure

1. Verify the IPv4 and DNS configuration on DC01.
2. Open DNS Manager.
3. Expand the `home.lab` Forward Lookup Zone.
4. Review the DNS host and SRV records.
5. Confirm Active Directory integration.

### Verification

DNS is operational and supports Active Directory name resolution.

### Evidence

![IPv4 and DNS Configuration](../screenshots/24%20-%20IPv4%20and%20DNS%20Configuration.png)

![Forward Lookup Zone - home.lab](../screenshots/25%20-%20Forward%20Lookup%20Zone%20-%20home.lab.png)

![DNS Records](../screenshots/26%20-%20DNS%20Records.png)

---

[← Previous: Server Deployment](04-server-deployment.md) | [Next: Organisational Structure →](06-organisational-structure.md)
