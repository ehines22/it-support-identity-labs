# Microsoft Entra ID — User Provisioning & Onboarding

## Project Overview

This hands-on lab demonstrates the onboarding (joiner) stage of identity lifecycle management using Microsoft Entra ID.

I created a fictional employee account, configured employee attributes, created a security group, assigned group membership, and verified the results.

## Lab Environment

- Microsoft Entra ID Free
- Personal training tenant
- Northstar Technologies — fictional organization
- Employee: Jordan Williams
- Department: Finance
- Job title: Accountant
- Security group: `Finance-SG`

## Scenario

Northstar Technologies is onboarding Jordan Williams as a new Accountant in the Finance department.

The simulated request calls for an enabled organizational user account and membership in the Finance security group.

HR confirmation and manager approval were assumptions provided for the training scenario, not actual approvals.

## Steps Performed

1. Opened Microsoft Entra ID and selected **Users > New user > Create new user**.
2. Created an internal member account for Jordan Williams.
3. Configured employee properties, including department, job title, company, employee ID, and office location.
4. Verified the user account appeared in the directory.
5. Confirmed Jordan's account was enabled and his employee attributes were saved.
6. Created `Finance-SG` as a Security group with Assigned membership.
7. Added Jordan to `Finance-SG`.
8. Returned to Jordan's profile and verified the security group membership.

## Troubleshooting Observation

Immediately after creating Jordan's account, the Users page still displayed only the original user.

Instead of attempting to create another account, I refreshed the Users list.

The directory then displayed two users, including Jordan Williams.

This reinforced the importance of verifying administrative changes before repeating an operation.

## Verification Results

| Validation Check | Result |
|---|---|
| User account created | Verified |
| Account enabled | Verified |
| Employee attributes saved | Verified |
| Finance security group created | Verified |
| Jordan added to Finance-SG | Verified |
| Directory administrative roles | None shown during verification |
| Finance application access | Not configured or tested |
| User sign-in and MFA | Not tested |

## Tools and Skills Demonstrated

- Microsoft Entra ID
- Cloud user provisioning
- Identity attribute administration
- Security group creation
- Group membership management
- Joiner workflows
- Change verification
- IAM ticket documentation
- Least-privilege awareness

## Evidence

Five screenshots were captured during the lab:

1. Employee properties configuration
2. User creation confirmation
3. Employee properties verification
4. Finance security group configuration
5. Finance group membership verification

Clickable evidence links will be added after privacy review and screenshot upload.

## Key Takeaways

- User accounts should contain accurate employee attributes.
- Group-based access administration helps standardize identity management.
- Administrative changes must be verified rather than assumed successful.
- Security group membership alone does not prove access to an application.
- Onboarding should follow documented organizational approvals and procedures.

## Lab Scope

This project was completed in a personal Microsoft Entra ID Free tenant using a fictional organizational scenario.

The user account and security group membership were verified. No real Finance application was configured, no end-user sign-in was tested, and no production enterprise environment was involved.

---

**Related documentation:** IAM-001 simulated service ticket will be included in this project.
