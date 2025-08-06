+++
date = '2025-08-06T19:52:28+05:30'
draft = false
title = 'Assessment Techniques and Patching in ICS'
+++
## Assessment techniques for ICS
- Asset discovery/ identification
- Asset Management
- Vulnerability Management
- Cadence : first time / one-time/ periodic/ ongoing
- Work with operational personnel to understand impact: system-level/ network-level/ device-level
- Physical walkthrough: Infrastructure, Protocols, Media, age of systems, etc
- Routine, scheduled scanning
- Common Techniques:
  - Authenticated/ credentialed scanning : Ports and services, software inventory, patch auditing (OS and app), light weight scanning
  - Configuration auditing : Identify known good state or optimal configuration and compare it against it
  - Native OS commands: Check network config, installed patches, ports nad services , user accounts, etc.
  - Native ICS protocols and tools

## Patching in ICS
- Cyber maintenance
- Create an intelligent process that fits the context of system
- Automate and leverage virtualisation where possible
- Remove unneeded ports and services
- Change default or easily-guessed credentials
- Opt for SSH over telnet for infrastructure devices
