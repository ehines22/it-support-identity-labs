# Microsoft Entra ID — Employee Offboarding & Account Security

## Project Overview

This hands-on lab demonstrates the leaver (offboarding) stage of identity lifecycle management using Microsoft Entra ID.

The exercise focuses on disabling an employee account, revoking sign-in sessions, removing obsolete security group membership, and verifying the final account state.

## Lab Environment

- Microsoft Entra ID (personal test tenant)
- Microsoft Entra admin center
- Entra user and group administration
- Fictional organization: Northstar Technologies
- Security group: `HR-SG`

## Scenario

Jordan Williams, a fictional HR Coordinator, is leaving Northstar Technologies.

A simulated HR offboarding request directs IT to terminate organizational access while retaining the user account for possible future auditing and retention requirements.

The task is to perform the approved offboarding steps in the lab and document the outcome.

## Offboarding Procedure

1. Located Jordan Williams in Microsoft Entra ID.
2. Verified that the user account was enabled before making changes.
3. Captured the initial account status.
4. Disabled the user account to block new sign-ins.
5. Revoked the user's sign-in sessions.
6. Reviewed the user's remaining security group memberships.
7. Removed Jordan from `HR-SG` without deleting the group.
8. Verified that the account remained disabled and the obsolete group membership was removed.
9. Retained the user account rather than deleting it.

## Results

- **Account status:** Disabled
- **Session revocation:** Completed through Microsoft Entra ID
- **HR security group:** User membership removed
- **Finance security group:** Previously removed during the employee transfer lab
- **User account:** Retained in the directory
- **Business application access:** Not independently tested because no enterprise application assignments were configured in this lab

## Security Concepts

### Account Disabling

Disabling the account prevents new sign-ins while retaining the identity and its associated directory information.

### Session Revocation

Revoking sessions invalidates supported refresh tokens and sessions. It does not necessarily terminate every previously issued application access token immediately.

### Least Privilege and Access Cleanup

Removing obsolete group membership reduces unnecessary standing access and helps prevent old group-based permissions from being restored if an account is accidentally re-enabled.

### Retention and Auditability

Retaining a disabled account can support organizational retention and investigation requirements, depending on applicable policies.

## Tools and Skills Demonstrated

- Microsoft Entra ID
- User lifecycle administration
- Account disabling
- Sign-in session revocation
- Security group membership management
- Least privilege
- Offboarding verification
- Service ticket documentation

## Evidence

The following screenshots document the employee offboarding workflow:

1. [Account Status Before Offboarding](screenshots/01-Before-Offboarding-Account-Status.png)
2. [Session Revocation Confirmation Prompt](screenshots/02-Session-Revocation-Confirmation-Prompt.png)
3. [HR Group Membership Removed](screenshots/03-HR-Group-Membership-Removed.png)
4. [Final Disabled Account Status](screenshots/04-Final-Disabled-Account-Status.png)

**Note:** Screenshot #2 captures the session revocation confirmation prompt, not a success notification. Session revocation was completed during the lab but is not independently verified by that screenshot.

### Service Ticket

[View IAM-004 Employee Offboarding Service Ticket](IAM-004-Service-Ticket.md)
## Key Takeaways

- Disabling an account and revoking sessions are separate security actions.
- Removing unnecessary group memberships supports access governance.
- Offboarding should follow an authorized request and documented procedure.
- Final verification is necessary before closing an identity administration ticket.

---

**Environment:** Personal Microsoft Entra ID test tenant using a simulated HR offboarding request. This lab demonstrates hands-on administrative practice, not production enterprise experience.
