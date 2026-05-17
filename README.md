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
- [Homelab Topology](screenshots/domain-topology.png)

---

## Scenario-Based Lab Structure
Each scenario represents a **real-world IT support ticket** and is documented independently.

| Scenario | Description | Status |
|--------|------------|--------|
| 01 | Windows Server Deployment and Active Directory OU Structure | Complete |
| 02 | Password Reset & Account Unlock | Complete |
| 03 | Password Policy via Group Policy | Planned |
| 04 | Network Drive Mapping via GPO | Planned |
| 05 | Account Disable / Enable | Planned |
| 06 | Domain Trust Repair | Planned |

---

## Implemented Scenarios

### Scenario 01 – Windows Server Deployment and Active Directory OU Structure
📄 Documentation: [User and OU Structure](documentation/AD-OU-structure.md) 

Status: Completed

--- 

### Scenario 02 – account lockout & password reset
📄 Documentation: [Account Lockout Scenario](documentation/Account-lockout-scenario.md)  

Status: Completed

---


### Scenario 03 – Password Policy via Group Policy
📄 Documentation: `[password policy via GPO](documentation/password-policy-via-GPO.md)

Status: Complete

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
