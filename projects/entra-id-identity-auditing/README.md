# Microsoft Entra ID — Identity Auditing & Access Review

## Project Overview

This hands-on lab demonstrates how to investigate identity and security group changes using Microsoft Entra ID audit logs.

The investigation builds on a simulated employee transfer from Finance to Human Resources.

## Lab Environment

- Microsoft Entra ID (free test tenant)
- Microsoft Entra admin center
- Directory audit logs
- Security groups: `Finance-SG` and `HR-SG`
- Fictional organization: Northstar Technologies

## Scenario

Jordan Williams, a fictional employee, transferred from Finance to Human Resources.

The previous lab involved updating employee attributes, removing Finance group membership, and adding HR group membership.

The objective of this investigation was to review historical audit evidence without modifying the employee's permissions.

## Investigation Steps

1. Opened the Microsoft Entra admin center and navigated to directory audit logs.
2. Filtered audit activity for October 30, 2026.
3. Located successful group creation, member removal, and member addition events.
4. Opened the `Remove member from group` audit event.
5. Reviewed the Activity, Target(s), and Modified Properties tabs.
6. Verified that the event status was `Success` and the target user was Jordan Williams.
7. Identified `Finance-SG` in the old value of `Group.DisplayName`, supporting the Finance membership removal.
8. Located a successful `Add member to group` event and captured supporting evidence.
9. Reviewed how current group memberships and authorization records should be checked separately from historical activity.

## Investigation Findings

- **Finance membership removal:** Supported by the successful removal event and its modified properties.
- **Group addition:** A successful addition event was identified; its full target details were not independently documented in the investigation report.
- **Current membership:** A verification screenshot was captured, but its exact contents were not recorded in the original report.
- **Unauthorized activity:** None established. A possible later re-addition was discussed only as a hypothetical troubleshooting exercise.
- **Application access:** No actual business application permissions were configured or tested.

## Tools and Skills Demonstrated

- Microsoft Entra ID
- Identity audit log investigation
- Group membership auditing
- Activity and target analysis
- Modified property interpretation
- Access governance concepts
- Least privilege
- Technical documentation

## Evidence

The following screenshots document the Microsoft Entra ID audit investigation:

1. [Entra Audit Log Overview](screenshots/01-Entra-Audit-Log-Overview.png)
2. [Finance Group Removal Audit](screenshots/02-Finance-Group-Removal-Audit.png)
3. [HR Group Addition Audit](screenshots/03-HR-Group-Addition-Audit.png)
4. [Current HR Group Membership](screenshots/04-Current-HR-Group-Membership.png)

### Service Ticket

[View IAM-003 Identity Auditing Service Ticket](IAM-003-Service-Ticket.md)

## Key Takeaways

- A successful audit event confirms that an operation was recorded, not that the resulting access remains unchanged.
- Reviewing modified properties can identify details missing from the main audit record.
- Historical group changes should be compared with current membership and authorized requests.
- Audit evidence should be documented without assuming facts that were not verified.

---

**Environment:** Personal Microsoft Entra ID test tenant and fictional organizational scenario. This project demonstrates hands-on IAM investigation practice, not production enterprise experience.
