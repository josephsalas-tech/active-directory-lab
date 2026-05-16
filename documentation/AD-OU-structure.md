# Active Directory Organizational Structure

## Overview

This section documents the Organizational Unit (OU) structure used within the Active Directory lab environment. The structure was designed to simulate a small school district or educational IT environment with separated users, computers, and administrative groups.

The goal of this structure is to improve:
- User organization
- Group Policy management
- Administrative delegation
- Scalability
- Troubleshooting efficiency

---

# Domain Information

| Component | Value |
|----------|------|
| Domain Name | JS3homelab.local |
| Directory Service | Active Directory Domain Services |
| Environment Type | Educational / School District Simulation |

---

# Organizational Unit Structure

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

# OU Design Goals

## Faculty OU
Used to organize:
- Teacher accounts
- Administrative staff
- Faculty workstations

This allows policies and permissions to be applied separately from student systems.

---

## Students OU
Used for:
- Student user accounts
- Classroom or lab systems
- Restricted policy testing

This separation simulates common school district access control practices.

---

## Computers OU
Used to organize domain-joined systems by device type and role.

Examples:
- Administrative systems
- Student lab machines
- Shared workstations

---

## IT_Admins OU
Contains privileged administrative accounts used for:
- Domain management
- User administration
- Group Policy configuration
- Infrastructure maintenance

---

# Group Policy Integration

The OU structure was designed to support future:
- Password policies
- Login restrictions
- Drive mapping
- Software deployment
- Administrative controls

This structure simplifies targeted Group Policy application.

---

# Screenshots to Capture

## Active Directory Users and Computers (ADUC)
- Full OU structure
- Faculty OU expanded
- Students OU expanded
- Computer organization
- Security groups

---

# Skills Demonstrated

- Active Directory organization
- Organizational Unit planning
- Educational IT structure simulation
- User and computer management
- Group Policy planning
- Administrative structure design

---

# Why This Matters

Proper Active Directory organization is critical in enterprise and educational environments. A clean OU structure improves:
- Scalability
- Troubleshooting
- Policy management
- Administrative efficiency

This project demonstrates foundational identity and access management concepts commonly used in school district and enterprise IT environments.

---

# Resume / LinkedIn Summary

Designed and implemented a structured Active Directory Organizational Unit (OU) hierarchy to simulate user, computer, and administrative management practices used in educational and enterprise IT environments.
