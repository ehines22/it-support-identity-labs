# Windows 11 Domain Join & DNS Troubleshooting

## Project Overview
This home lab documents the process of joining a Windows 11 workstation to an Active Directory domain hosted on Windows Server 2025. During the domain-join attempt, Windows reported that the domain controller could not be contacted.

The project focuses on investigating domain connectivity, reviewing client DNS configuration, and verifying successful domain membership.

## Lab Environment
- Windows Server 2025 — Active Directory Domain Services and DNS
- Windows 11 — Domain-join client
- Oracle VirtualBox — Virtual lab environment
- Active Directory domain: `adlab.local`

## Problem
The Windows 11 client initially operated outside the domain. When attempting to join `adlab.local`, Windows displayed an error indicating that an Active Directory domain controller could not be contacted.

## Investigation and Verification
1. Reviewed the Windows 11 client's initial workgroup configuration.
2. Attempted to join the client to `adlab.local` and documented the domain controller connection error.
3. Inspected the client's network configuration using `ipconfig /all`, including its IP address, DNS server, and DNS suffix.
4. Continued the domain-join process and confirmed the client displayed membership in `adlab.local`.
5. Queried Active Directory DNS SRV records using `nslookup` to verify domain controller discovery information.
6. Checked the client's logon-server information using `echo %logonserver%`.
7. Inspected Active Directory Users and Computers to verify the workstation's computer object.

## Outcome
The workstation was successfully joined to the Active Directory domain. Follow-up checks showed domain membership, domain controller discovery information, and the computer object in Active Directory.

The screenshots document the initial error and the final working state. They do not establish every intermediate configuration change, so a single confirmed root cause is not claimed.

## Tools and Skills Demonstrated
- Windows 11 domain joining
- Active Directory Domain Services
- DNS configuration and SRV record lookup
- `ipconfig /all`
- `nslookup`
- `echo %logonserver%`
- Active Directory Users and Computers
- Windows troubleshooting and outcome verification

## Evidence

The following screenshots document the domain-join troubleshooting process and verification:

1. [Before Domain Join](screenshots/01-Before-Domain-Join.png)
2. [Domain Join Error](screenshots/02-Domain-Join-Error.png)
3. [Client IP and DNS Configuration](screenshots/03-Client-IP-DNS-Configuration.png)
4. [Successful Domain Membership](screenshots/04-Successful-Domain-Membership.png)
5. [Active Directory DNS SRV Verification](screenshots/05-AD-DNS-SRV-Verification.png)
6. [Domain Logon Server Verification](screenshots/06-Domain-Logon-Server-Verification.png)
7. [Computer Object in Active Directory](screenshots/07-Computer-Object-in-ADUC.png)

## Key Takeaways
- Active Directory domain discovery depends on functioning DNS.
- Network and DNS settings should be checked when a client cannot locate a domain controller.
- A troubleshooting task should conclude with multiple verification checks rather than assuming the issue is resolved.

---
**Environment:** Personal Windows Server and Windows 11 virtual lab. This project demonstrates simulated enterprise IT administration, not production support experience.
