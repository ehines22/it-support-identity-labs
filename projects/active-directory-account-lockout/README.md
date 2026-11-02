# Active Directory Account Lockout & Password Policy

## Project Overview
This home lab demonstrates user account lockout administration and domain password security policy configuration in an on-premises Active Directory environment.

The exercise uses a simulated help desk request involving an employee named Sarah whose account was locked.

## Lab Environment
- Windows Server and Active Directory Domain Services
- Active Directory Users and Computers (ADUC)
- Group Policy Management Console (GPMC)
- Personal virtual lab environment

## Scenario
A fictional employee, Sarah, is unable to access her account because it is locked. The help desk must verify the user's identity and account status before performing an authorized unlock.

The lab also includes configuring a domain account lockout threshold of five failed sign-in attempts.

## Actions Practiced
1. Located the affected user account in Active Directory Users and Computers.
2. Reviewed the account's lockout status.
3. Practiced an authorized account unlock workflow after simulated identity verification.
4. Opened Group Policy Management to review domain account lockout settings.
5. Configured the account lockout threshold to five invalid sign-in attempts.
6. Documented the account administration and password policy workflow.

## Security Concepts
- Account lockouts help limit repeated password-guessing attempts.
- Identity verification should occur before unlocking an account.
- Domain lockout policy should follow organizational security requirements.
- Support actions should be verified and documented.
- Account lockouts may have causes that require further investigation, such as outdated saved credentials.

## Tools and Skills
- Active Directory Users and Computers
- Group Policy Management
- User account administration
- Account lockout troubleshooting
- Password security policy configuration
- Help desk ticket documentation

## Evidence
Original lab screenshots document the account management and Group Policy workflow. Screenshots will be added after a privacy review.

## Key Takeaways
This lab reinforced the importance of verifying identity, understanding domain security policies, and documenting account recovery actions.

---
**Environment:** Personal Active Directory home lab using a fictional support scenario. This project is not production enterprise experience.
