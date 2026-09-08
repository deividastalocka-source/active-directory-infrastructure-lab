# IT Support and Validation

This section demonstrates common IT support procedures within the Active Directory environment and performs a final validation of the deployed infrastructure.

## Step 26 — Perform Password Reset

### Purpose

Simulate a forgotten password support request and restore access to a domain user account.

### Procedure

1. Open Active Directory Users and Computers.
2. Locate the affected user account.
3. Reset the user's password.
4. Require the user to change their password at the next sign-in.
5. Sign in to PC01 using the new credentials.
6. Complete the password change when prompted.
7. Verify successful authentication.

### Verification

The user successfully authenticates to the domain after the password reset and password change process.

### Evidence

![Locating User Account for Password Reset](../screenshots/64%20-%20Locating%20User%20Account%20for%20Password%20Reset.png)

![Resetting Domain User Password](../screenshots/65%20-%20Resetting%20Domain%20User%20Password.png)

![User Required to Change Password](../screenshots/66%20-%20User%20Required%20to%20Change%20Password.png)

![Successful Login After Password Reset](../screenshots/67%20-%20Successful%20Login%20After%20Password%20Reset.png)

---

## Step 27 — Configure and Test Account Lockout

### Purpose

Configure an account lockout policy and demonstrate the process of recovering a locked domain user account.

### Procedure

1. Edit the Default Domain Policy.
2. Configure the account lockout settings.
3. Force a Group Policy update.
4. Attempt authentication using invalid passwords until the account is locked.
5. Verify that the user account is locked in Active Directory.
6. Unlock the account.
7. Sign in again using the correct credentials.

### Verification

The account lockout policy functions correctly. The account is locked after repeated invalid authentication attempts and access is successfully restored after the administrator unlocks the account.

### Evidence

![Account Lockout Policy Configured](../screenshots/68%20-%20Account%20Lockout%20Policy%20Configured.png)

![Active Directory Account Locked Out](../screenshots/69%20-%20Active%20Directory%20Account%20Locked%20Out.png)

![Unlocking Active Directory User Account](../screenshots/70%20-%20Unlocking%20Active%20Directory%20User%20Account.png)

![Successful Login After Account Unlock](../screenshots/71%20-%20Successful%20Login%20After%20Account%20Unlock.png)

---

## Step 28 — Validate the Environment

### Purpose

Perform a final review of the Active Directory environment to confirm that all deployed services and configurations are operating correctly.

### Procedure

1. Verify the Active Directory organisational structure.
2. Verify domain-joined computers.
3. Verify DNS configuration and records.
4. Verify departmental shared folders and permissions.
5. Verify Group Policy configuration.
6. Confirm successful domain authentication.

### Validation Summary

| Component | Validation |
|---|---|
| Active Directory | OUs, users and security groups configured |
| Domain Client | PC01 successfully joined to `home.lab` |
| DNS | Domain DNS configuration and records operational |
| File Services | Departmental shares and access controls operational |
| Group Policy | Centralised user restrictions successfully applied |
| Authentication | Domain users able to authenticate successfully |

### Verification

All infrastructure components are operating as expected.

### Evidence

![Active Directory Environment Validation](../screenshots/72%20-%20Active%20Directory%20Environment%20Validation.png)

![Domain Joined Computer Validation](../screenshots/73%20-%20Domain%20Joined%20Computer%20Validation.png)

![DNS Configuration Validation](../screenshots/74%20-%20DNS%20Configuration%20Validation.png)

![Department Shares Validation](../screenshots/75%20-%20Department%20Shares%20Validation.png)

![Group Policy Validation](../screenshots/76%20-%20Group%20Policy%20Validation.png)

---

[← Previous: Group Policy](09-group-policy.md) | [Next: Conclusion and Lessons Learned →](11-conclusion-and-lessons-learned.md)
