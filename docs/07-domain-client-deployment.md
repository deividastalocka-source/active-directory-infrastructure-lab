# Domain Client Deployment

This section documents the deployment of a Windows 11 Enterprise client workstation, its network and DNS configuration, and its integration with the `home.lab` Active Directory domain.

## Step 19 — Create the Windows 11 Enterprise Client

### Purpose

Deploy a Windows 11 Enterprise virtual machine to represent an employee workstation within the domain environment.

### Procedure

1. Create a new Windows 11 virtual machine in VMware Workstation Pro.
2. Install Windows 11 Enterprise.
3. Complete the initial operating system configuration.
4. Rename the workstation to `PC01`.
5. Restart the workstation to apply the new hostname.

### Verification

Windows 11 Enterprise is installed successfully and the workstation is identified as `PC01`.

### Evidence

![Creating Windows 11 Virtual Machine](../screenshots/35%20-%20Creating%20Windows%2011%20Virtual%20Machine.png)

![Windows 11 Installation Complete](../screenshots/36%20-%20Windows%2011%20Installation%20Complete.png)

![Rename Windows 11 Client to PC01](../screenshots/37%20-%20Rename%20Windows%2011%20Client%20to%20PC01.png)

---

## Step 20 — Configure PC01 Networking and DNS

### Purpose

Configure PC01 to communicate with the Domain Controller and use DC01 for DNS resolution.

### Procedure

1. Open the network adapter configuration on PC01.
2. Configure the workstation's network settings.
3. Set the Preferred DNS Server to `192.168.79.10`.
4. Verify connectivity with DC01.
5. Test DNS resolution for the `home.lab` domain.
6. Verify that Active Directory LDAP SRV records can be resolved.

### Verification

PC01 can communicate with DC01 and successfully resolve the `home.lab` domain through the Domain Controller's DNS service.

### Evidence

![PC01 Network Configuration](../screenshots/38%20-%20PC01%20Network%20Configuration.png)

![PC01 DNS Configuration](../screenshots/39%20-%20PC01%20DNS%20Configuration.png)

![PC01 Domain DNS Verification](../screenshots/40%20-%20PC01%20Domain%20DNS%20Verification.png)

---

## Step 21 — Join PC01 to the Domain

### Purpose

Join the Windows 11 Enterprise workstation to the `home.lab` Active Directory domain.

### Procedure

1. Open the system properties on PC01.
2. Select the option to join a domain.
3. Enter `home.lab` as the domain name.
4. Provide authorised domain credentials when prompted.
5. Confirm that PC01 successfully joins the domain.
6. Restart the workstation.

### Verification

PC01 successfully joins the `home.lab` domain and is recognised as a domain-joined workstation.

### Evidence

![Joining PC01 to home.lab Domain](../screenshots/41%20-%20Joining%20PC01%20to%20home.lab%20Domain.png)

![PC01 Successfully Joined Domain](../screenshots/42%20-%20PC01%20Successfully%20Joined%20Domain.png)

---

## Step 22 — Validate Domain Authentication

### Purpose

Confirm that domain users can authenticate successfully on the newly joined workstation.

### Procedure

1. Sign in to PC01 using a domain user account.
2. Authenticate using the `HOME` domain.
3. Run `whoami` to verify the authenticated domain user.
4. Run `hostname` to verify that the session is running on PC01.
5. Verify that the PC01 computer account appears in Active Directory.
6. Move PC01 into the appropriate `Computers` OU.

### Verification

Domain authentication succeeds and PC01 is correctly registered and organised within Active Directory.

### Evidence

![Domain User Login Verification](../screenshots/43%20-%20Domain%20User%20Login%20Verification.png)

![PC01 Computer Account in Active Directory](../screenshots/44%20-%20PC01%20Computer%20Account%20in%20Active%20Directory.png)

![PC01 Moved to Computers OU](../screenshots/45%20-%20PC01%20Moved%20to%20Computers%20OU.png)

---

[← Previous: Organisational Structure](06-organisational-structure.md) | [Next: File Shares and Permissions →](08-file-shares-and-permissions.md)
