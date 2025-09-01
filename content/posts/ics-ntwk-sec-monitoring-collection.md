+++
date = '2025-09-01T22:42:25+05:30'
draft = false
title = 'ICS Network Security Monitoring Collection'
+++
- Comms network collection points: edge of internal zone industrial firewalls or on core control network switches
- For SPAN config: Fully managed network switches
- For TAP config: Dedicated hardware TAP device
- 5-tuple capture
  - Source IP
  - Destination IP
  - Source Port
  - Destination Port
  - Protocol
- Full-packet capture
  - Full packet payload  + 5-tuple capture
- Collect 5-tuple data at minimum at firewalls at perimeters to identify malicious remote connections, network pivoting from IT to ICS through trusted connections, adversary C2 connection etc.
- Collect full packet captures inside control network from ICS DMZ down to level 1/0 to ensure Industrial protocol commands and data streams are captured for analysis/ baselining etc
