# Active Directory Lab – Scenario-Based IT Support Practice

## Overview
This repository documents a hands-on **Active Directory lab** built to simulate common **help desk and school IT support scenarios**. The focus of this lab is practical, ticket-driven workflows rather than basic installation alone.

The lab environment uses a Windows Server domain controller and domain-joined Windows client to practice real-world administrative and troubleshooting tasks.

---

## Lab Environment
- **Domain Controller:** Windows Server
- **Client OS:** Windows 10 Pro (domain-joined)
- **Directory Services:** Active Directory, DNS
- **Virtualization Platform:** Proxmox VE
- **Network Design:** VLAN-segmented homelab environment

---

## Domain Architecture
The lab follows a simple but scalable domain design.

**Planned Components:**
- Organizational Units (OUs) for users and computers
- Security groups for role-based access
- Group Policy Objects (GPOs) scoped to OUs
- Centralized authentication and DNS

📌 Diagram:
- `diagrams/domain-topology.png`

---

## Scenario-Based Lab Structure
Each scenario represents a **real-world IT support ticket** and is documented independently.

| Scenario | Description | Status |
|--------|------------|--------|
| 01 | User and OU Structure | In Progress |
| 02 | Password Reset & Account Unlock | Planned |
| 03 | Password Policy via Group Policy | Planned |
| 04 | Network Drive Mapping via GPO | Planned |
| 05 | Account Disable / Enable | Planned |
| 06 | Domain Trust Repair | Planned |

---

## Implemented Scenarios

### Scenario 01 – User and OU Structure
📄 Documentation: `scenarios/01-user-and-ou-structure.md`  
📸 Screenshots: `screenshots/aduc/`

Status: In Progress

---
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
```text
I am unable to sign into my domain account after entering the wrong password multiple times. Please assist with unlocking my account and resetting my password if necessary.



### Scenario 03 – Password Policy via Group Policy
📄 Documentation: `scenarios/03-password-policy-gpo.md`  
📸 Screenshots: `screenshots/gpo/`

Status: Planned

---

### Scenario 04 – Network Drive Mapping via GPO
📄 Documentation: `scenarios/04-drive-mapping-gpo.md`  
📸 Screenshots: `screenshots/shares/`

Status: Planned

---

### Scenario 05 – Account Disable / Enable
📄 Documentation: `scenarios/05-account-disable-enable.md`  
📸 Screenshots: `screenshots/aduc/`

Status: Planned

---

### Scenario 06 – Domain Trust Repair
📄 Documentation: `scenarios/06-domain-trust-repair.md`  
📸 Screenshots: `screenshots/client/`

Status: Planned

---

## Troubleshooting & Lessons Learned
Ongoing notes and observations are captured here:

📄 `notes/lessons-learned.md`

Topics include:
- DNS dependencies in Active Directory
- GPO refresh behavior
- OU design considerations
- Common authentication failures

---

## Why This Lab Matters
Active Directory remains a foundational technology in enterprise and educational IT environments. This lab demonstrates **practical experience** with real support scenarios such as password resets, policy enforcement, access control, and domain recovery.

---

## Resume / LinkedIn Summary
Built and documented a scenario-driven Active Directory lab using Windows Server and domain-joined Windows clients to practice real-world IT support workflows including password resets, Group Policy enforcement, and domain troubleshooting.
