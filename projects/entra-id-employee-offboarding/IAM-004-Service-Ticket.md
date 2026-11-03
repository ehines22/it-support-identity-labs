# IAM-004 — Employee Offboarding & Account Security

**Ticket type:** Identity access management / employee offboarding  
**Organization:** Northstar Technologies — fictional training scenario  
**Environment:** Personal Microsoft Entra ID training tenant  
**Affected user:** Jordan Williams  
**Department:** Human Resources  
**Role:** HR Coordinator  
**Request origin:** Simulated HR instruction (not a real approval)  
**Status:** Completed in guided lab, per operator's final verification

## Request

Offboard fictional departing employee Jordan Williams. Prevent new organizational sign-ins, revoke sign-in sessions, remove obsolete HR security group membership, and retain the account instead of deleting it pending a hypothetical retention procedure.

## Verification before changes

- Located the user under **Entra ID → Users → All users**.
- Checked existing account status and recorded starting-state evidence.
- Prior labs had transferred the fictional identity from Finance to Human Resources.

## Actions performed

1. Set **Account enabled = No** to block new sign-ins.
2. Selected **Revoke sessions** for the user.
3. Removed Jordan's membership from **HR-SG** without deleting the security group.
4. Checked that **Finance-SG** did not appear in the final group membership list.
5. Verified Jordan's account remained present and disabled.

## Reported results

| Check | Result |
|---|---|
| User account | Disabled |
| Revocation action | Reported completed in Entra portal; screenshot records confirmation prompt only |
| `HR-SG` membership | Removed |
| `Finance-SG` membership | Absent |
| Account retained | Yes |

## Evidence references

- `01-Before-Offboarding-Account-Status.png`
- `02-Session-Revocation-Confirmation-Prompt.png` — confirms the revocation prompt was displayed, not that a successful completion notification was captured
- `03-HR-Group-Membership-Removed.png`
- `04-Final-Disabled-Account-Status.png`

## Analyst notes / security rationale

- Disabling the identity helps prevent new sign-ins while preserving the account for possible retention and audit needs.
- Session revocation is a separate action: some preexisting application sessions or access tokens may remain usable until they expire or the service enforces revocation.
- Removing an obsolete security group membership reduces stale entitlements and the chance of regranting group-based permissions if an account is later re-enabled.
- No enterprise application assignment, production access test, or verified HR application deprovisioning occurred in this lab.

## Resolution

The simulated Entra offboarding tasks were reported completed and the account was retained in a disabled state. No production systems or actual employee accounts were affected.

**Closeout:** Guided IAM-004 training exercise completed.
