# Scenario 01 – Windows Server Deployment & Active Directory OU Structure

## Scenario Overview

This scenario documents the initial deployment and configuration of a Windows Server virtual machine used as the Domain Controller for the Active Directory lab environment. The project includes the installation of Active Directory Domain Services (AD DS), promotion of the server to a Domain Controller, and the creation of an Organizational Unit (OU) structure designed to simulate a school district or enterprise environment.

This scenario serves as the foundation for all future Active Directory, Group Policy, and help desk ticket simulations within the homelab.

---

# Project Objectives

The goals of this scenario were to:

- Deploy a Windows Server virtual machine within Proxmox
- Install and configure Active Directory Domain Services
- Promote the server to a Domain Controller
- Create a functional Active Directory domain
- Design a structured OU hierarchy
- Prepare the environment for future Group Policy and user management scenarios

---

# Environment

| System | Purpose |
|--------|---------|
| Proxmox VE | Virtualization platform |
| Windows Server VM | Domain Controller |
| Active Directory Domain Services | Centralized identity management |
| Windows 10 Pro VM | Domain-joined client machine |

---

# Infrastructure Overview

## Virtualization Platform
The Windows Server environment was deployed as a virtual machine hosted within the Proxmox homelab infrastructure.

---

## Domain Information

| Component | Value |
|----------|------|
| Domain Name | JS3homelab.local |
| Server Role | Domain Controller |
| Directory Service | Active Directory Domain Services |

---

# Phase 1 – Windows Server VM Deployment

## Steps Performed
1. Created a new Windows Server virtual machine within Proxmox
2. Allocated virtual hardware resources:
   - CPU
   - Memory
   - Storage
   - Network adapter
3. Mounted Windows Server installation media
4. Installed Windows Server operating system
5. Configured initial administrative settings

---

## Screenshots to Capture

### Proxmox
- [Windows Server VM overview](screenshots/windows-server-install-complete.png)

---

### Windows Server
- [Windows Server installation](screenshots/windows-server-static-ip.png)
- Initial desktop setup
- [Server Manager dashboard](screenshots/windows-server-DC-DNS-and-LDAP-ready.png)

---

# Phase 2 – Active Directory Domain Services Installation

## Steps Performed
1. Opened **Server Manager**
2. Added the following role:
   - Active Directory Domain Services (AD DS)
3. Installed required dependencies
4. Verified successful role installation

---

## Expected Result
The server becomes ready for Domain Controller promotion.

---

## Screenshots to Capture
- Server Manager
- Add Roles and Features Wizard
- AD DS installation confirmation

---

# Phase 3 – Domain Controller Promotion

## Steps Performed
1. Promoted the server to a Domain Controller
2. Created a new forest:
   - `JS3homelab.local`
3. Configured:
   - DNS services
   - Directory Services Restore Mode (DSRM)
4. Completed Domain Controller setup
5. Restarted the server

---

## Validation Performed
- Verified successful domain creation
- Confirmed DNS functionality
- Verified Active Directory administrative tools installed successfully

---

## Screenshots to Capture
- Domain Controller promotion wizard
- Domain configuration page
- Successful promotion confirmation
- Post-restart login screen

---

# Phase 4 – Organizational Unit (OU) Structure Creation

## OU Design Goals

The OU structure was designed to simulate:
- Educational IT environments
- Administrative separation
- Scalable Group Policy management
- User and computer organization

---

## Organizational Unit Structure

```text
JS3homelab.local
│
├── Faculty
│   ├── Teachers
│   ├── Staff
│   └── Administrators
│
├── Students
│   ├── Student Users
│   └── Student Groups
│
├── IT_Admins
│
├── Computers
│   ├── Faculty PCs
│   ├── Student PCs
│   └── Lab Systems
│
└── Security Groups
```

---

# Phase 5 – User and Group Preparation

## Administrative Tasks Performed
- Created test user accounts
- Created security groups
- Organized users into appropriate OUs
- Prepared structure for future Group Policy scenarios

---

## Screenshots to Capture

### Active Directory Users and Computers (ADUC)
- Full OU structure
- Faculty OU expanded
- Students OU expanded
- Security groups
- Test users

---

# Validation & Testing

## Validation Performed
- Confirmed Active Directory functionality
- Verified OU creation
- Verified administrative tools operation
- Confirmed domain accessibility
- Confirmed readiness for client domain join

---

# Skills Demonstrated

- Windows Server deployment
- Proxmox virtualization
- Active Directory Domain Services installation
- Domain Controller promotion
- DNS configuration
- Organizational Unit design
- User and group management
- Enterprise identity infrastructure planning

---

# Troubleshooting Notes

## Key Observations
- DNS configuration is critical for Active Directory functionality
- Proper OU organization simplifies future Group Policy management
- Virtualization allows safe testing and rollback during deployment
- Initial server planning significantly improves scalability

---

# Lessons Learned

This scenario reinforced the importance of proper infrastructure planning before implementing identity management and Group Policy systems. Creating a clean OU hierarchy early simplifies administration, troubleshooting, and future policy deployment.

---

# Why This Scenario Matters

Active Directory remains a foundational technology in enterprise and educational IT environments. This project demonstrates practical experience with:
- Identity infrastructure deployment
- Windows Server administration
- Centralized authentication systems
- Organizational planning
- Enterprise directory services

These concepts are directly relevant to:
- Help desk technician roles
- School district IT support
- Systems administration
- MSP environments

---

# Resume / LinkedIn Summary

Deployed and configured a Windows Server virtual machine within Proxmox, installed Active Directory Domain Services, promoted the system to a Domain Controller, and designed a structured Organizational Unit hierarchy to simulate enterprise and educational IT environments.
