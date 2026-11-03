# Wi-Fi Connectivity Troubleshooting

## Project Overview

This home lab documents a Windows Wi-Fi connectivity troubleshooting scenario using network adapter information, command-line diagnostics, and browser testing.

The project follows a three-stage evidence approach: before, broken, and after.

## Lab Environment

- Windows 11 workstation
- Wireless network adapter
- Windows Network Connections
- Command Prompt
- Web browser

## Problem

During the troubleshooting exercise, the workstation experienced a network connectivity failure.

A ping test to 8.8.8.8 returned general failure messages with 100% packet loss, despite earlier evidence of working network connectivity.

## Investigation and Evidence

1. **Before — Initial Connection:** Inspected Windows Network Connections and captured the Wi-Fi adapter's connected status, alongside successful connectivity diagnostics.
2. **Broken — Connectivity Failure:** Used `ping 8.8.8.8` to test external IP connectivity. The command returned general failure messages and 100% packet loss.
3. **After — Website Access Restored:** Verified that a website could load successfully in a web browser.

## Findings

The screenshots show that the workstation experienced a connectivity failure and subsequently regained usable web access.

The evidence does not establish the exact configuration change that restored connectivity, so a specific root cause is not claimed.

## Tools and Skills Demonstrated

- Windows network adapter inspection
- `ping` connectivity testing
- `nslookup` DNS diagnostics
- Basic network troubleshooting
- Browser-based connectivity verification
- Before/broken/after documentation

## Evidence

Three original screenshots document the initial network state, connectivity failure, and restored website access. Clickable evidence links will be added after the screenshots are uploaded.

## Key Takeaways

- A connected Wi-Fi adapter does not always guarantee working internet access.
- Testing an external IP address can help distinguish connectivity problems from DNS-related problems.
- Network troubleshooting should include verification that the user can access the required service.
- Documenting before and after results helps demonstrate the impact of troubleshooting.

---

**Environment:** Personal Windows troubleshooting lab. This project demonstrates hands-on practice rather than production enterprise experience.
