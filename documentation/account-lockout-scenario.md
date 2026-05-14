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
- Failed login attempts on Windows client
- Account lockout message at login screen
- Expected event viewer ID for lockout 
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
