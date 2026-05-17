# Scenario 03 – Group Policy Password Complexity Enforcement

## Scenario Overview

This scenario documents the implementation of domain-wide password security policies using Group Policy within the Active Directory lab environment. The objective was to enforce stronger authentication standards across all domain users by configuring password complexity requirements, minimum password length, and account lockout settings.

This scenario simulates real-world enterprise and school district security practices designed to reduce weak passwords and unauthorized access attempts.

---

# Administrative Request

> “The organization requires stronger password policies to improve account security and standardize authentication requirements across all domain users.”

---

# Environment

| System | Purpose |
|--------|---------|
| Windows Server | Domain Controller |
| Active Directory | Centralized authentication |
| Group Policy Management | Policy enforcement |
| Windows 10 Pro VM | Domain-joined client machine |
| Proxmox VE | Virtualization platform |

---

# Objective

The goals of this scenario were to:

- Enforce password complexity requirements
- Configure minimum password length
- Configure account lockout policies
- Apply policies domain-wide
- Validate policy enforcement on client systems

---

# Group Policy Path

```text
Computer Configuration
└── Policies
    └── Windows Settings
        └── Security Settings
            └── Account Policies
                ├── Password Policy
                └── Account Lockout Policy
```

---

# Policies Configured

| Policy | Configuration |
|--------|---------------|
| Enforce Password History | Configured |
| Maximum Password Age | Configured |
| Minimum Password Length | Configured |
| Password Complexity Requirements | Enabled |
| Account Lockout Threshold | Configured |
| Account Lockout Duration | Configured |

---

# Phase 1 – Opening Group Policy Management

## Steps Performed
1. Logged into the Domain Controller
2. Opened:
   - **Group Policy Management**
3. Navigated to:
   - Default Domain Policy

---

# Phase 2 – Configuring Password Policy

## Steps Performed
1. Edited the Default Domain Policy
2. Navigated to:
   - Password Policy
3. Configured:
   - Password complexity requirements
   - Minimum password length
   - Password history
   - Password expiration settings

---

## Expected Result
All domain users become subject to the configured password requirements.

---

## Screenshots to Capture
- [Password Policy settings/Complexity requirement enabled/Minimum password length configuration](screenshots/applying-gpo-password-policy.png)

---

# Phase 3 – Configuring Account Lockout Policy

## Steps Performed
1. Navigated to:
   - Account Lockout Policy
2. Configured:
   - Failed login threshold
   - Lockout duration
   - Reset lockout counter timing

---

## Expected Result
User accounts become temporarily locked after repeated failed login attempts.

---

## Screenshots to Capture
- Account Lockout Policy settings
- Lockout threshold configuration

---

# Phase 4 – Applying Group Policy Changes

## Steps Performed
1. Applied Group Policy changes
2. Opened Command Prompt on the client machine
3. Ran:

```powershell
gpupdate /force
```

4. Refreshed or restarted the client system

---

## Screenshots to Capture
- `gpupdate /force` command
- Successful Group Policy update confirmation

---

# Phase 5 – Validation Testing

## Tests Performed
- Attempted to create weak passwords
- Attempted repeated failed logins
- Verified account lockout behavior
- Verified password complexity enforcement

---

## Validation Results
- Weak passwords were rejected
- Password complexity rules applied successfully
- Repeated failed sign-ins triggered account lockout
- Policies applied across domain-connected systems

---

## Screenshots to Capture
- Weak password rejection message
- Failed login attempts
- Account lockout behavior
- Successful compliant password creation

---

# Skills Demonstrated

- Active Directory administration
- Group Policy configuration
- Password security management
- Account lockout configuration
- Enterprise authentication practices
- Client policy validation
- Centralized administrative control

---

# Troubleshooting Notes

## Key Observations
- Group Policy changes may require policy refresh or restart before applying
- DNS functionality is required for successful Group Policy processing
- Default Domain Policy impacts all domain users
- Incorrect policy settings can unintentionally prevent user access

---

# Lessons Learned

This scenario reinforced the importance of centralized authentication security within enterprise environments. Group Policy provides scalable administrative control for enforcing password standards and reducing unauthorized access risks across all domain-connected systems.

---

# Why This Scenario Matters

Password security policies are a foundational component of enterprise IT infrastructure. This scenario demonstrates practical experience with:
- Identity and access management
- Authentication security
- Domain-wide administrative policy enforcement
- Active Directory security practices

These skills are commonly required in:
- Help desk environments
- School district IT support
- Systems administration
- MSP-managed infrastructures

---

# Resume / LinkedIn Summary

Configured and validated domain-wide password complexity and account lockout policies using Group Policy within an Active Directory environment to enforce centralized authentication security standards across domain users.
