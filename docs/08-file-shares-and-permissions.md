# File Shares and Permissions

This section documents the creation of departmental network shares and the configuration of share and NTFS permissions to control access to organisational resources.

## Step 23 — Create Department File Shares

### Purpose

Create departmental folders and publish them as network shares.

### Procedure

1. Create `C:\Shares` on DC01.
2. Create the following departmental folders:
   - IT
   - HR
   - Finance
   - Executive
3. Configure each folder using Advanced Sharing.
4. Assign the appropriate share permissions.
5. Test authorised and unauthorised access from the domain client.
6. Verify that all departmental network shares are available.

### Verification

Departmental shares are accessible over the network according to their assigned permissions. Access testing confirms that authorised users can access their departmental resources while unauthorised access is denied.

### Evidence

![Department Shared Folders Created](../screenshots/46%20-%20Department%20Shared%20Folders%20Created.png)

![IT Folder Advanced Sharing](../screenshots/47%20-%20IT%20Folder%20Advanced%20Sharing.png)

![IT Share Permissions](../screenshots/48%20-%20IT%20Share%20Permissions.png)

![Unauthorized IT Share Access Denied](../screenshots/49%20-%20Unauthorized%20IT%20Share%20Access%20Denied.png)

![Authorized IT Share Access](../screenshots/50%20-%20Authorized%20IT%20Share%20Access.png)

![Department Network Shares Configured](../screenshots/51%20-%20Department%20Network%20Shares%20Configured.png)

---

## Step 24 — Configure NTFS Permissions

### Purpose

Secure departmental folders using NTFS permissions and security groups.

### Procedure

1. Open the Security settings for each departmental folder.
2. Disable inheritance and convert the inherited permissions.
3. Grant `Modify` permissions to the appropriate departmental security group.
4. Retain access for `SYSTEM` and `Administrators`.
5. Repeat the configuration for each department.
6. Test access using domain user accounts.

### Permission Model

| Department | Security Group | Access |
|---|---|---|
| IT | `IT_Users` | Modify |
| HR | `HR_Users` | Modify |
| Finance | `Finance_Users` | Modify |
| Executive | `Executive_Users` | Modify |

### Verification

Users can only access resources belonging to their department. Testing confirms that authorised users can write to their departmental folders while users without the required permissions are denied access.

### Evidence

![IT Folder Default NTFS Permissions](../screenshots/52%20-%20IT%20Folder%20Default%20NTFS%20Permissions.png)

![IT Group NTFS Permissions](../screenshots/53%20-%20IT%20Group%20NTFS%20Permissions.png)

![Department NTFS Permissions Configured](../screenshots/54%20-%20Department%20NTFS%20Permissions%20Configured.png)

![IT User NTFS Write Access Verified](../screenshots/55%20-%20IT%20User%20NTFS%20Write%20Access%20Verified.png)

![Unauthorized HR Folder Access Denied](../screenshots/56%20-%20Unauthorized%20HR%20Folder%20Access%20Denied.png)

---

[← Previous: Domain Client Deployment](07-domain-client-deployment.md) | [Next: Group Policy →](09-group-policy.md)
