# IAM-002 — Employee Department Transfer

**Record type:** Simulated IAM service ticket / hands-on training  
**Ticket ID:** IAM-002  
**Date:** October 30, 2026  
**Organization:** Northstar Technologies *(fictional)*  
**System:** Microsoft Entra ID Free  
**Request category:** Identity lifecycle / Mover / Group membership change  
**Status:** Resolved — lab configuration verified

## Request summary

Jordan Williams transferred from Finance to Human Resources. Update the existing Entra ID account and replace the Finance security-group membership with the approved HR security-group membership.

### Employee details

| Field | Original | Requested |
| --- | --- | --- |
| Employee | Jordan Williams | Same existing identity |
| Employee ID | NS-1001 | Unchanged |
| Department | Finance | Human Resources |
| Job title | Accountant | HR Coordinator |
| Security group | `Finance-SG` | `HR-SG` |
| Account enabled | Yes | Remain enabled |

**Authorization:** Manager and HR approval are simulated as part of the lab scenario; this is not a real service request.

## Initial assessment

- Located Jordan's existing Microsoft Entra ID cloud user.
- Verified the Finance department and Accountant title.
- Confirmed `Finance-SG` membership before changes.
- Captured baseline screenshots: `01-Before-Employee-Properties.png` and `02-Before-Finance-Group-Membership.png`.

## Actions taken

1. Edited Jordan's **Department** to `Human Resources` and **Job title** to `HR Coordinator` on the same account.
2. Saved the change, refreshed the profile, and verified both updated values.
3. Created the `HR-SG` security group with **Assigned** membership and an HR-employee description.
4. Removed Jordan's membership in `Finance-SG`; did not delete the group.
5. Added Jordan to `HR-SG`.
6. Refreshed the Groups view and confirmed the final membership state.
7. Verified the account remained enabled.

## Validation

| Check | Outcome |
| --- | --- |
| Same user identity retained | Pass |
| Account enabled | Pass |
| Department set to Human Resources | Pass |
| Job title set to HR Coordinator | Pass |
| `Finance-SG` no longer assigned to Jordan | Pass |
| `HR-SG` assigned to Jordan | Pass |
| HR application access | **Not tested — no application configured** |

## Evidence attached

- `01-Before-Employee-Properties.png`
- `02-Before-Finance-Group-Membership.png`
- `03-After-Employee-Properties.png`
- `04-HR-Security-Group-Created.png`
- `05-After-HR-Group-Membership-Verified.png`

## Training-only follow-up: HR application access issue

**Hypothetical report:** Jordan can sign in, but cannot open an HR application.

**Triage approach:** Ask for the exact error; confirm user status and correct group membership; check whether the enterprise application requires user assignment and whether access is granted directly or through `HR-SG`; assess other relevant restrictions; obtain authorization before changing assignments; retest and document.

**Resolution:** Not performed. This was a discussion exercise, not an actual incident or application fix.

## Resolution notes

The simulated transfer was completed and verified within **Microsoft Entra ID user attributes and assigned security-group memberships**. Obsolete Finance group membership was removed, and HR group membership was added. Downstream application access, provisioning, and sign-in behavior were outside the lab scope.

**Ticket closure:** Resolved for the requested lab configuration changes only.

---

*Personal portfolio exercise. All company, employee, and approval details are fictional. No production systems were administered.*
