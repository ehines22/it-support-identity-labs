# Active Directory Group Policy Configuration & Verification

## Project Overview
This home lab explores creating and linking a Group Policy Object (GPO) in an Active Directory domain, refreshing policy on a Windows client, and investigating policy application with command-line tools.

## Lab Environment
- Windows Server with Active Directory Domain Services
- Group Policy Management Console (GPMC)
- Windows 11 virtual machine
- Oracle VirtualBox
- Marketing organizational unit (OU)

## Lab Scenario
The objective was to practice Group Policy administration for a department-specific OU and learn how to verify whether policies are being processed by a Windows client.

## Procedure and Evidence
1. Opened Group Policy Management and examined the Marketing OU.
2. Created and linked a Marketing-related GPO to the OU.
3. Ran `gpupdate` on a Windows client.
4. Confirmed that computer and user policy updates completed successfully.
5. Used `gpresult` to inspect the resulting Group Policy information.
6. Reviewed output showing a policy filtered with the status `Not Applied (Empty)`.

## Findings
The screenshots confirm that the GPO was linked to the Marketing OU and that the client completed a Group Policy refresh.

However, successful execution of `gpupdate` does not, by itself, prove that a particular GPO applied.

The captured `gpresult` output includes a filtered policy marked `Not Applied (Empty)`. The evidence does not establish that the intended Marketing policy settings successfully took effect on the client.

## Troubleshooting Considerations
If a linked GPO is not applying as expected, relevant checks include:
- Confirming that the target user or computer belongs to the correct OU
- Checking whether the GPO contains applicable and enabled settings
- Reviewing GPO link status, inheritance, and security filtering
- Running `gpresult /r` or generating a detailed policy report
- Verifying that the intended settings actually take effect

These checks are recommended follow-up investigation steps, not additional actions claimed to have been completed in this lab.

## Tools and Skills Demonstrated
- Group Policy Management Console
- Active Directory organizational units
- GPO linking and administration
- `gpupdate`
- `gpresult`
- Windows policy troubleshooting

## Evidence

The following screenshots document Group Policy configuration, refresh, and troubleshooting:

1. [GPO Linked to Marketing OU](screenshots/01-GPO-Linked-Marketing-OU.png)
2. [Successful Group Policy Refresh](screenshots/02-GPUpdate-Success.png)
3. [Group Policy Result Verification](screenshots/03-GPResult-Verification.png)

## Key Takeaways
- Linking a GPO does not guarantee it applies to a particular user or computer.
- A successful policy refresh is different from verifying an individual GPO's settings.
- `gpresult` helps administrators investigate applied and filtered policies.

---
**Environment:** Personal Active Directory home lab. This project documents hands-on practice rather than production enterprise experience.
