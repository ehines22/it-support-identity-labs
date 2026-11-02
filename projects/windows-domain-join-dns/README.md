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
Seven original lab screenshots document:
1. Workstation before domain join
2. Domain controller connection error
3. Client IP and DNS configuration
4. Successful domain membership
5. Active Directory DNS SRV lookup
6. Domain logon-server verification
7. Workstation computer object in Active Directory

Screenshots will be added after reviewing them for information appropriate for public sharing.

## Key Takeaways
- Active Directory domain discovery depends on functioning DNS.
- Network and DNS settings should be checked when a client cannot locate a domain controller.
- A troubleshooting task should conclude with multiple verification checks rather than assuming the issue is resolved.

---
**Environment:** Personal Windows Server and Windows 11 virtual lab. This project demonstrates simulated enterprise IT administration, not production support experience.
