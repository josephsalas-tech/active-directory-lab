# Scenario 02 – Account Lockout and Password Reset

## Scenario Overview
This scenario simulates a common help desk support ticket in which a domain user becomes locked out of their Active Directory account after multiple failed login attempts. The issue is investigated and resolved through Active Directory Users and Computers (ADUC), then documented and closed within osTicket.

This workflow demonstrates a realistic IT support process involving:
- User authentication troubleshooting
- Active Directory account management
- Password reset procedures
- Ticket lifecycle documentation
- Client-side validation
---
## Ticket Summary

**Ticket Type:** Account Access  
**Priority:** Normal  
**Issue Reported:**  
> “I am unable to log into my computer after entering the wrong password multiple times.”
---
## Environment

| System | Purpose |
|--------|---------|
| Windows Server | Active Directory Domain Controller |
| Windows 10 Pro VM | Domain-joined client machine |
| osTicket | Help desk ticketing system |
| LDAP Integration | Domain authentication integration |
| Proxmox VE | Virtualization platform |

### Domain Information
- **Domain Name:** JS3homelab.local
- **Test User:** testuserlockout
---
## Objective
The objective of this scenario is to simulate a real-world account lockout event and resolve it through Active Directory administrative tools while documenting the process through a help desk ticket workflow.
---
# Phase 1 – Triggering the Account Lockout

## Steps Performed
1. Logged into the Windows 10 domain-joined client VM
2. Entered the incorrect password repeatedly at the login screen
3. Continued failed sign-in attempts until the account lockout threshold was reached
4. Confirmed the user account was no longer able to authenticate

## Expected Result
The user account becomes locked due to the configured domain account lockout policy.
---
## Screenshots to Capture
- [Account lockout message at login screen](screenshots/acct-lockout-windows.png)
- [Expected event viewer ID for lockout](screenshots/acct-lockout-ID.png)
---

# Phase 2 – Ticket Creation in osTicket

## Ticket Submission
A help desk ticket was created to simulate the user requesting assistance after the account lockout occurred.

### Ticket Information
- **Category:** Account Access
- **Status:** Open
- **Assigned Department:** IT Support

### Example Ticket Description
> “I am unable to log into my computer after entering the wrong password multiple times.”
---

## Screenshots to Capture
- [Ticket submission page](screenshots/ticket-creation.png)
- Open ticket in osTicket dashboard
- Ticket details page

---

# Phase 3 – Active Directory Investigation

## Steps Performed
1. Logged into the Domain Controller
2. Opened **Active Directory Users and Computers (ADUC)**
3. Located the user account: `testuser1`
4. Opened account properties
5. Confirmed the account was locked out

---

## Administrative Actions Taken
- Unlocked the user account
- Reset the user password
- Enabled:
  - **User must change password at next logon**

---

## Expected Result
The account becomes unlocked and the user is able to authenticate again using the temporary password.

---

## Screenshots to Capture
- [User properties window](screenshots/testuserlockout-prop.png)
- [Account unlock & pass reset](screenshots/acct-pass-reset.jpg)

---

# Phase 4 – Client Validation

## Steps Performed
1. Returned to the Windows 10 client VM
2. Signed in using the temporary password
3. Changed the password when prompted
4. Verified successful domain login

---

## Validation Performed
- User successfully authenticated against the domain
- Password change requirement functioned correctly
- Desktop loaded normally after login

---

## Screenshots to Capture
- [Password change prompt](screenshots/password-change.png)
- [Successful login to desktop](screenshots/testuserlockout-log-back-in.png)

---

# Phase 5 – Ticket Resolution Documentation

## Resolution Notes Added to osTicket

### Internal Technician Note

> "Verified the user account was locked in Active Directory following repeated failed sign-in attempts. Unlocked the account and reset the password. Configured the account to require a password change at next login."

### User Resolution Response

> "Your account has been unlocked and your password was reset successfully. Please log in using the temporary password provided and create a new password when prompted."


### Final Ticket Status
- Resolved
- Closed

---

## Screenshots to Capture
- Internal technician note
- Ticket response message
- Closed ticket confirmation

---

# Troubleshooting Notes

## Key Observations
- Active Directory account lockout behavior is controlled through Group Policy
- DNS functionality is critical for successful domain authentication
- Proper ticket documentation improves accountability and repeatability
- Validation on the client machine is necessary before closing tickets

---

# Skills Demonstrated

- Active Directory account management
- Password reset procedures
- Account lockout troubleshooting
- Help desk workflow documentation
- osTicket administration
- Client authentication validation
- Cross-system troubleshooting

---

# Lessons Learned

This scenario reinforced the importance of understanding how authentication, account policies, and ticketing workflows interact within an enterprise IT environment. It also demonstrated the value of validating resolutions directly on the affected client system before closing support tickets.

---

# Resume / LinkedIn Summary

Simulated and documented a real-world Active Directory account lockout scenario integrated with an osTicket help desk workflow, including ticket intake, account unlock, password reset, and client-side authentication validation.

