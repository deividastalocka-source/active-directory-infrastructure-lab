# Organisational Structure

This section documents the creation of the Active Directory organisational structure, including Organisational Units (OUs), departmental security groups and domain user accounts.

## Step 16 — Create the Organisational Unit Structure

### Purpose

Create a logical Active Directory hierarchy to organise users, computers, groups and servers.

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
5. Verify the completed organisational structure.

### Verification

The OU structure provides a logical and scalable foundation for managing users, computers, groups and departmental resources.

### Evidence

![Open Active Directory Users and Computers](../screenshots/27%20-%20Open%20Active%20Directory%20Users%20and%20Computers.png)

![Creating Company Organisational Units](../screenshots/28%20-%20Creating%20Company%20Organisational%20Units.png)

![Completed Organisational Unit Structure](../screenshots/29%20-%20Completed%20Organisational%20Unit%20Structure.png)

---

## Step 17 — Create Security Groups

### Purpose

Create departmental security groups to simplify permission management and access control.

### Procedure

1. Open the appropriate location in Active Directory Users and Computers.
2. Create the following Global Security Groups:
   - `IT_Users`
   - `HR_Users`
   - `Finance_Users`
   - `Executive_Users`
3. Configure each group as a Global Security Group.
4. Verify that all departmental groups were created successfully.

### Verification

The departmental security groups are available for assigning permissions and controlling access to resources.

### Evidence

![Creating Active Directory Security Group](../screenshots/30%20-%20Creating%20Active%20Directory%20Security%20Group.png)

![Completed Security Groups](../screenshots/31%20-%20Completed%20Security%20Groups.png)

---

## Step 18 — Create User Accounts and Assign Group Membership

### Purpose

Create domain user accounts and assign each user to the appropriate departmental security group.

### Procedure

1. Create user accounts within the appropriate departmental OUs.
2. Configure usernames and initial passwords.
3. Add each user to the appropriate departmental security group.
4. Verify the completed user accounts.
5. Confirm group membership for each user.

### User Structure

| User | Department | Security Group |
|---|---|---|
| David Talocka | IT | `IT_Users` |
| Sarah Jones | HR | `HR_Users` |
| Michael Brown | Finance | `Finance_Users` |
| Emma Wilson | Executive | `Executive_Users` |

### Verification

The domain user accounts are organised within their respective departments and assigned to the appropriate security groups for role-based access control.

### Evidence

![Creating Active Directory User Account](../screenshots/32%20-%20Creating%20Active%20Directory%20User%20Account.png)

![Completed Active Directory User Accounts](../screenshots/33%20-%20Completed%20Active%20Directory%20User%20Accounts.png)

![User Group Membership](../screenshots/34%20-%20User%20Group%20Membership.png)

---

[← Previous: Active Directory Deployment](05-active-directory-deployment.md) | [Next: Domain Client Deployment →](07-domain-client-deployment.md)
