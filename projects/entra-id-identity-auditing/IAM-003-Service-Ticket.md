# IAM-003 — Identity Audit Investigation

**Ticket type:** Identity audit / access review (simulated)  
**Organization:** Northstar Technologies *(fictional)*  
**Requested by:** Identity Operations training scenario  
**Subject:** Jordan Williams (fictional test user)  
**System:** Microsoft Entra ID Free  
**Investigation date:** November 1, 2026  
**Historical change date:** October 30, 2026  
**Status:** Investigation completed for the verified removal event; other checks documented with limitations

## Request description

Review audit evidence from a previously completed employee department transfer (Finance → Human Resources) and determine whether the recorded group-management activity supports the expected access changes.

**Expected configuration from IAM-002:**

- Department: Human Resources
- Job title: HR Coordinator
- `Finance-SG` membership removed
- `HR-SG` membership assigned
- Employee account remains enabled

These are the **expected** transfer results, not automatic findings of the new audit.

## Actions taken

1. Opened the Microsoft Entra directory audit log and filtered for October 30, 2026.
2. Located **Remove member from group** and **Add member to group** entries in the `GroupManagement` category.
3. Inspected the remove-member record at approximately 1:45 PM:
   - Activity type: `Remove member from group`
   - Status: `Success`
   - Target user: Jordan Williams (test account)
   - Target(s): group object ID shown, but no group display name in that tab
   - Modified Properties: `Group.DisplayName` old value `Finance-SG`
4. Cross-referenced the activity type, status, target user, and old group value to identify the successful removal of Jordan's Finance-SG membership.
5. Identified an add-member event at approximately 1:45 PM and saved an audit screenshot; the full detail fields were not independently recorded in the session narrative.
6. Reviewed how to investigate any mismatch between an approved access request, historical audit events, and current group memberships.

## Findings

**Confirmed from reviewed event:** The audit record indicates that Jordan Williams was successfully removed from `Finance-SG` on October 30, 2026.

**Additional audit event observed:** An `Add member to group` event was shown as successful in the audit list. The captured Modified Properties screenshot shows `HR-SG` as the added group. The success status is visible in the corresponding audit event list.

**Current access:** The training procedure called for checking Jordan's current membership and employee properties. The saved current-membership screenshot shows `HR-SG` listed for Jordan and does not show `Finance-SG` in the displayed membership list. This is a point-in-time verification; historical Success events alone do not establish current access.

**No evidence of unauthorized changes:** A Sunday re-addition to Finance-SG was discussed as a hypothetical case only. It was not observed in the lab.

## Validation and next follow-up

The captured group-membership page shows `HR-SG` present and `Finance-SG` absent from the displayed list. Recheck department, title, and account enabled state if completing a formal access-review closure; these fields were not independently reconfirmed in this investigation.

## Resolution / disposition

**Audit analysis documented:** Finance-SG removal supported by a successful recorded event and its modified properties. The report accurately distinguishes verified historical evidence from as-yet-undocumented current access validation. No permissions were changed during this investigation.

## Supporting evidence

- `01-Entra-Audit-Log-Overview.png`
- `02-Finance-Group-Removal-Audit.png`
- `03-HR-Group-Addition-Audit.png`
- `04-Current-HR-Group-Membership.png`
- `README.md`

**Security and privacy:** Redact personal emails, tenant identifiers, object IDs, and other identifying details before publishing portfolio screenshots.
