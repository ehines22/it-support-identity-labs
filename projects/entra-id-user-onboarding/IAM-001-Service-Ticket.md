# IAM-001 — New Employee Onboarding

**Organization:** Northstar Technologies (fictional)  
**Request type:** Identity provisioning / new hire  
**Lab date:** October 29, 2026  
**Requester:** Finance manager (simulated)  
**Employee:** Jordan Williams (fictional)  
**Platform:** Microsoft Entra ID Free  
**Ticket status:** **Identity and group provisioning verified; application access not tested**

## Request

Create an internal identity for incoming Finance employee Jordan Williams (Accountant) and assign membership in `Finance-SG`.

**Scenario prerequisites:** HR verification and Finance-manager approval were provided as training assumptions; they were not real approvals.

## Work performed

1. Created an enabled internal Entra user with display name Jordan Williams and username `jordan.williams` under the tenant's default `onmicrosoft.com` domain.
2. Configured department **Finance**, title **Accountant**, company **Northstar Technologies**, employee ID **NS-1001**, employee type **Employee**, and office location **Hattiesburg**.
3. Verified the user appears in the directory after refreshing the Users list.
4. Opened the user record and checked account status and employee attributes.
5. Created security group `Finance-SG` with Assigned membership.
6. Added Jordan to `Finance-SG` from Jordan's **Groups > Add memberships** view.
7. Verified that `Finance-SG` appears in Jordan's group memberships.

## Troubleshooting note

**Issue:** User list initially still showed one user after account creation.  
**Check:** Refreshed the Entra Users list rather than creating a second account.  
**Outcome:** List updated to two users, including Jordan.

## Validation

- **Passed:** User object visible; account enabled; employee properties correct; membership in `Finance-SG` confirmed.
- **Not tested:** Jordan's actual sign-in, MFA registration, Microsoft 365 licensing, and access to a Finance application.
- **Administrative access:** No Entra directory role assignments shown for Jordan during the user overview check.

## Resolution / handoff

**Provisioning steps for the training exercise are complete and verified.** Application access validation is out of scope because no Finance application was connected to the group. Do not represent this as full application onboarding or a production ticket closure.

**Evidence:** See the `screenshots/` directory and this project's `README.md`.
