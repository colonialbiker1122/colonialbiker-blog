+++
date = '2025-08-31T11:39:35+05:30'
draft = true
title = 'ICS Asset Inventory'
+++
## Physical Inspection
- Physically walk through, document hardware seen in racks etc, inspect software and protocols etc.
- Time consuming, expensive, physical risks exists

## Configuration Analysis
- Access control systems and network devices
- Switch and firewall config can reveal IP and MAC address pairings through ARP tables to indicate devices allowed/denied in network
- Traffic and port information reveals general protocols in use.
- Configuartion settings from ICS, PLC, RTU, IED, etc

## Active Scanning
- Intrusive to ICS operations. Fast process.
- Unnatural representation of network communications

## Passive Network Traffic Analysis
- Accurate representation of natural network control system communication
- Beneficial to capture and analyse during various modes of operation (startup, normal operations, emergency modes)

## Miscellaneous
- SPAN/ hardware TAP/ mirrored port configuration of fully managed switch
- LLDP: Link Layer Discovery Protocol
- Secure, searchable and scalable ICS asset inventory
