# Organisational Structure

This section documents the Active Directory organisational structure, including Organisational Units (OUs), departmental security groups and domain user accounts.

## Step 16 — Create the Organisational Unit Structure

### Purpose

Create a logical Active Directory hierarchy to organise users, computers, servers and groups.

### Procedure

1. Open Active Directory Users and Computers.
2. Create a top-level OU named `Company`.
3. Create the following OUs:
   - Users
   - Computers
   - Groups
   - Servers
4. Create departmental OUs:
   - IT
   - HR
   - Finance
   - Executive
5. Verify the completed hierarchy.

### Verification

The OU structure provides a scalable foundation for administration and Group Policy.

### Evidence

![Company OU Created](../screenshots/27%20-%20Company%20OU%20Created.png)

![Organisational Unit Structure](../screenshots/28%20-%20Organisational%20Unit%20Structure.png)

---

## Step 17 — Create Security Groups

### Purpose

Create departmental Global Security Groups to simplify permission management and access control.

### Procedure

1. Open the `Groups` OU.
2. Create the following Global Security Groups:
   - `IT_Users`
   - `HR_Users`
   - `Finance_Users`
   - `Executive_Users`
3. Verify the group scope and type are configured correctly.

### Verification

Departmental security groups are available for permissions and access control.

### Evidence

![Security Group Created](../screenshots/29%20-%20Security%20Group%20Created.png)

![Security Groups](../screenshots/30%20-%20Security%20Groups.png)

---

## Step 18 — Create User Accounts

### Purpose

Create domain user accounts and assign them to the appropriate departmental security groups.

### Procedure

1. Create user accounts within each departmental OU.
2. Configure usernames and passwords.
3. Add each user to the appropriate departmental security group.
4. Verify group membership.

### User Structure

| User | Department | Security Group |
|---|---|---|
| David Talocka | IT | `IT_Users` |
| Sarah Jones | HR | `HR_Users` |
| Michael Brown | Finance | `Finance_Users` |
| Emma Wilson | Executive | `Executive_Users` |

### Verification

Users are organised within their respective departmental OUs and inherit permissions through security group membership.

### Evidence

![User Accounts Created](../screenshots/31%20-%20User%20Accounts%20Created.png)

![User Account Properties](../screenshots/32%20-%20User%20Account%20Properties.png)

![User Group Membership](../screenshots/33%20-%20User%20Group%20Membership.png)

![Active Directory Users and Groups](../screenshots/34%20-%20Active%20Directory%20Users%20and%20Groups.png)

---

[← Previous: Active Directory Deployment](05-active-directory-deployment.md) | [Next: Domain Client Deployment →](07-domain-client-deployment.md)
