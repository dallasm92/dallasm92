# STAR Interview Cheat Sheet (IT Support)

Use this page to answer behavioral and troubleshooting interview questions with concise, evidence-backed stories.

## 1) DNS Outage / Intermittent Website Failure

- Situation: Coursera and YouTube intermittently failed to load after deploying Pi-hole in a home lab.
- Task: Restore reliable access and identify the true root cause.
- Action: Checked Pi-hole logs, validated client DNS resolver with `nslookup`, identified IPv6 DNS bypass and Firefox DoH interference, corrected client DNS path, and disabled browser DoH for system DNS usage.
- Result: Client traffic returned to Pi-hole, sites loaded consistently, and troubleshooting process was documented for repeat use.
- Evidence: https://github.com/dallasm92/it-support-labs/blob/main/labs/networking/2026-01-06-firefox-doh-pihole-dns-bypass.md

## 2) Network Printer Offline Incident

- Situation: User could not print after router reboot; printer showed Offline.
- Task: Restore printing quickly with minimal user disruption.
- Action: Verified connectivity, confirmed printer DHCP IP changed, corrected Windows TCP/IP printer port, cleared queue, and restarted print spooler.
- Result: Printing restored, test page passed, and recurrence risk reduced with DHCP reservation recommendation.
- Evidence: https://github.com/dallasm92/it-support-labs/blob/main/labs/windows/2026-02-13-network-printer-offline-tcp-ip-port.md

## 3) Windows File Access / Shared Drive Enablement

- Situation: Needed centralized shared storage for domain users in Windows Server lab.
- Task: Deploy reliable SMB share and mapped drive workflow with tested permissions.
- Action: Created user/account context in AD, provisioned share and NTFS permissions, mapped drive on Windows 11 client, and validated access path and user context.
- Result: Reliable user access to shared data and clearer support baseline for file access incidents.
- Evidence: https://github.com/dallasm92/it-support-labs/blob/main/labs/windows/2026-01-06-windows-server-file-share-map-drive.md

## 4) Device Refresh and Data Migration

- Situation: Legacy Windows 10 system had severe performance issues and needed replacement.
- Task: Migrate to Windows 11 with data safety and minimal downtime.
- Action: Performed backup-first migration with external SSD, validated copied data, completed new device provisioning, restored files, and tested printer/dual monitor setup.
- Result: User moved to a stable system with preserved data and validated peripherals.
- Evidence: https://github.com/dallasm92/it-support-labs/blob/main/labs/windows/2025-06-01-home-pc-refresh-data-migration.md

## 5) Linux Workstation Git/SSH Access Enablement

- Situation: Linux workstation could not authenticate to GitHub over SSH.
- Task: Enable secure, repeatable SSH-based Git operations.
- Action: Generated keypair, configured ssh-agent, corrected key location/naming, added public key to GitHub, and validated auth.
- Result: Reliable push/pull workflow restored and onboarding steps documented.
- Evidence: https://github.com/dallasm92/it-support-labs/blob/main/labs/linux/2026-01-01-github-ssh-setup.md

## Quick Practice Prompts

- Tell me about a time you solved an issue that looked like one thing but had a different root cause.
- Tell me about a time you restored a user’s workflow quickly.
- Tell me about a time you prevented a repeat incident after fixing the immediate issue.
