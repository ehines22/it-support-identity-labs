# Microsoft Entra ID — Employee Transfer & Access Changes

## Project Overview

This hands-on lab demonstrates the mover stage of identity lifecycle management using Microsoft Entra ID.

The exercise involved transferring a fictional employee from Finance to Human Resources, updating employee attributes, and adjusting security group memberships to reflect the new role.

## Lab Environment

- Microsoft Entra admin center
- Microsoft Entra ID test tenant
- Fictional organization: Northstar Technologies
- Employee: Jordan Williams
- Security groups: `Finance-SG` and `HR-SG`

## Simulated Service Request

Jordan Williams is transferring from the Finance department to Human Resources.

**Previous role:**
- Department: Finance
- Security group: `Finance-SG`

**New role:**
- Department: Human Resources
- Job title: HR Coordinator
- Security group: `HR-SG`

The objective was to update Jordan's identity information and remove group membership no longer appropriate for the new position.

## Actions Performed

1. Reviewed Jordan's existing employee properties and Finance group membership.
2. Updated the employee's department to Human Resources and job title to HR Coordinator.
3. Created the `HR-SG` security group.
4. Removed Jordan from `Finance-SG`.
5. Added Jordan to `HR-SG`.
6. Verified the updated employee information and HR group membership.

## Results

The simulated employee transfer was completed in Microsoft Entra ID.

Jordan's identity was updated to reflect the Human Resources role, and security group membership was adjusted.

The account remained enabled throughout the transfer.

## Security Concepts

- **Least privilege:** Remove access that is no longer appropriate for an employee's responsibilities.
- **Joiner-Mover-Leaver lifecycle:** Update identity attributes and access when employees change roles.
- **Group-based access management:** Security groups can be used to organize authorization assignments.
- **Verification:** Confirm access changes rather than assuming they were applied correctly.

## Important Scope Limitation

This lab demonstrates security group administration. It does not demonstrate an actual Finance or HR enterprise application assignment, so application-level access was not tested.

The approval request was fictional and used for training purposes.

## Tools and Skills Demonstrated

- Microsoft Entra ID
- Employee attribute administration
- Security group creation
- Group membership changes
- Identity lifecycle management
- Least-privilege concepts
- Access change verification
- Service ticket documentation

## Evidence

The following screenshots document Jordan's simulated transfer from Finance to Human Resources:

1. [Employee Properties Before Transfer](screenshots/01-Before-Employee-Properties.png)
2. [Finance Group Membership Before Transfer](screenshots/02-Before-Finance-Group-Membership.png)
3. [Employee Properties After Transfer](screenshots/03-After-Employee-Properties.png)
4. [HR Security Group Created](screenshots/04-HR-Security-Group-Created.png)
5. [HR Group Membership Verified](screenshots/05-After-HR-Group-Membership-Verified.png)

### Service Ticket

[View IAM-002 Employee Transfer Service Ticket](IAM-002-Service-Ticket.md)

## Service Ticket

A simulated IAM-002 service ticket documents the access change request, actions performed, and verification. The ticket will be linked after upload.

## Key Takeaways

Employee transfers require more than updating a job title. Identity administrators must also review and adjust existing access to align with the employee's new responsibilities.

---
**Environment:** Personal Microsoft Entra ID lab using a fictional organizational scenario. This project does not represent production enterprise administration.
