+++
date = '2025-08-26T19:23:41+05:30'
draft = false
title = 'DDoS (Distributed Denial of Service)'
+++
## Introduction
- Overwhelm target (server/website etc) resources making it diffucult/ impossible for legitimate users to access the service.
- Impacts: Disrupt, cause downtime or degrade performance

## Common DDoS Attacks
- SYN flood
- HTTP flood
- UDP flood
- Ping of death: send IP packets greater than 65K bytes
- Smurf attack: Flood with ICMP packets
- Slowloris 
- DNS flood
- Teardrop attack: Send fragmented packets. Server can’t reassemble
- DNS amplification 
- SNMP amplification
- NTP amplification
- SNMP reflection
- SSDP 
- Fraggle attack: Similar to smurf. Use UDP instead of ICMP 

## Detailed List of DDoS Attacks
### 1. DDOS CLDAP Flood
- Servers running CLDAP (connectionless LDAP), UDP protocol.
- Amplification: Small requests but huge reply from server
- Exhaustion of target server’s resources

### 2. DDOS Discard Flood
- Server running discard protocol (port 9). TCP or UDP. RFC 863
- Discard services used for testing/ debugging/ maintenance etc.

### 3. DDOS DNS flood
- Servers running DNS query traffic
  - DNS Query Flood: Large number of queries (random/ specific)
  - DNS Reflection Attack
  - DNS Amplification Attack: Response size > Query size
- DNS rate limiting and traffic shaping
  - Traffic classification: A/ MX/ AAAA records, source IP etc.
  - Prioritization and bandwidth allocation
  - BIND, Unbound, Microsoft DNS
- Anycast routing
- Open resolver protection: Prevention agaisnt amplification attacks

### 4. DDOS DNS Reflect-attck
- Zombie machine sends DNS requests with source addresses spoofed to the target address to multiple open DNS resolvers. Resolvers then send reply to target machine.

### 5. DDoS DNS Fragmented Reflection Flood 
- Send large response from DNS server to client
- Response is large enough to create fragmented UDP packets.

### 6. DDoS DNS Fragmented Reflection Flood (DNSKEY)
- Large fragmented UDP datagram as response to small query
- Response would be DNS key records along with RRSIGs
- Fragmentation complicates detection and mitigation of attack
- Ensure DNSSEC
- Traffic analysis

### 7. DDoS DNS Fragmented Reflection Flood (TXT)
- Large fragmented UDP datagram, as response to small query
- Response will be TXT records

### 8. DDoS HTTP GET POST
- Excessive GETs and POSTs of files a DDoS attack [RFC 1945]
- Use WAF: Web pplication Firewall
- Use caching, load balancing, application hardening, IP whitelisting

### 9. DDoS HTTP MultiVERB
- Simulate multiple GETs within a single HTTP request. 
- Used to create DoS condition on web server
- Multiple HTTP methods (VERBs) like GET/ POST/ PUT etc to overwhelm
- Complex traffic pattern

### 10. DDoS HTTP Pipeline Flood
- Multiple requests within a single HTTP session
- HTTP Pipelining: Feature of HTTP/1.1
- Send multiple HTTP requests without waiting for response
- Connection handling, queueing and processing issues come up

### 11. DDoS HTTP RUDY
- Low and slow attack
- A RUDY tool crawls the victim’s app looking for a form field
- Creates HTTP post request. Header mentions length content
- Tool breaks down packets as small as 1 byte each
- Tool sends packets at 10 sec interval each

### 12. DDoS HTTP Slow Post
- Exploit web server’s support for users with slow or intermittent connections
- Content-length header contains a message body size will be fulfilled over several TCP packets

### 13. DDoS HTTP Slowloris
- Opening and maintaining many simultaneous HTTP connections
- Uses up server resources (threads)
- Attacker periodically sends partial request headers to target to keep request alive
- Increase server availability and rate limit incoming requests

### 14. DDoS HTTP TCP Receive Window Size 0
- Retrieves a large webpage then slowly lowers the TCP receive window size to 0 bytes
- Server’s TCP stack is forced to pause data transmission
- Causes resource exhaustion and connection flooding

### 15. DDoS ICMP Echo Reply Flood
- Echo request packet directed at a broadcast/ multicast address with source address assigned to victim IP address
- Emulate reflected traffic directed at the victim
- Flooding with echo replies

### 16. DDoS ICMP Fragment Flood
- Send large amount of random ICMP request data larger than standard MTU of 1500 bytes
- ICMP messages need to be fragmented, overwhelming the victim with computationally expensive task of reassembling frames
- Causes network congestion, is complex and stealthy

### 17. DDoS ICMP Ping Flood
- Send overwhelming amount of ICMP ping packets

### 18. DDoS LOIC HTTP
- Low Orbit Ion Cannon (LOIC): Tool developed by Praetox Technology
- Now open-sourced. JS LOIC and Low Orbit Web Cannon
- Flood target server with TCP, UDP, HTTP packets
- One attacker using LOIC is not serious impact
- In order to make co-ordinated attacks easier, users can use IRC chat channels to run a ‘Hivemind’ version of LOIC which lets one primary user several networked secondary computers, creating a voluntary botnet

### 19. DDoS LOIC TCP 8080
- Simulate LOIC TCP DDoS traffic targeting port 8080

### 20. DDoS LOIC UDP Port 53
- Simulate LOIC UDP DDoS traffic targeting port53

### 21. DDoS mDNS Response Flood
- Attacker redirects flood of mDNS reponses to victim
- mDNS
  - Primarily within LAN
  - Serverless. Multicast approach
  - Broadcast query ad response to all devices
- Used in 0 config networking scenarios where devices can automatically discover each other and their services

### 22. DDoS NTPv2 Moonlist Flood
- Attacker sends spoofed source moonlist request to NTP server
- Response of 44 KB to victim. Amplification factor : 233X
- NTP: Network Time Protocol. Synchronise clocks of devices
- Monlist: Returns list of last 600 IPs which queried NTP server

### 23. DDoS QoTD Reflection Flood
- Quote of the day protocol. UDP port 17

### 24. DDoS Radius Flood 
- RADIUS : Remote Authentication Dial-in User Service
- Used for Authentication, Authorisation, Accounting in network service
- UDP port 1812 (AA) and 1813 (Accounting)
- Client sends RADIUS requests to the server

### 25. DDoS Recursive GET
- GET requests are used to traverse through different pages or images collected by attacker
- Cause server to generate excessive load
- May also recursively trigger other GET requests

### 26. DDoS RCP/ Portmapper Reflection Flood
- Victim receives portmapper dump call responses
- RCP (Remote Procedure Call): Request service from another computer in the network. Executes remote procedures
- Portmapper (rpcbind): Used in Unix-like systems to map RPC program numbers to network port numbers

### 27. DDoS RTP Flood
- Backscatter traffic from a call center that has been flooded with spoofed SIP INVITE messages
- RTP: Real-Time Transport Protocol: Deliver audio/video over IP. VoIP calls, video conferencing, streaming media.

### 28. DDoS SIP Invite Flood
- Generate SIP invite messages with spoofed via and from header
- SIP: Session Initiation Protocol. Call setup, modification, teardown, etc. and management of multimedia communication sessions over IP networks
- SIP INVITE: Initiate new session or call

### 29. DDoS SNMPv2 Bulk Response Flood
- Flood UDP datagrams at target server
- Reflection attack caused by forged bulk Get requests requesting common OIDs repeatedly
- Simple Network Management Protocol
- GETBULK: Retrieve large info from network device

### 30. DDoS SSDP Flood
- Victim receives flood of SSDP M-search responses directed to its IP from reflectors
- Simple Service Discovery Protocol: Discover services over LAN part of UPnP (Universal plug n play), UDP port 1900

### 31. DDoS SSL HTTP POST Flood
- Sends large amount of data via HTTP POST method over SSL
- Consumes CPU and memory as it decrypts the contents

### 32. DDoS SSL Key Exchange Flood
- Flood of SSL initial key exchange messages
- CPU use is exhausted

### 33. DDoS TCP RST Flood
- Reflection attack that hides the source of the attack
- RST packets are sent in response to a TCP packet that is received out of a session in state
- Disrupt active connection. Can interrupt ongoing session, web transactions, file transfers, etc.

### 34. DDoS TCP SYN Flood
- Uncomplicated version of SYN flood attack

### 35. DDoS TDL4 HTTP Flood
- TDL4 DDoS initiated by instruction from a C&C server to an infected bot
- TDL4 (Top Layer DDoS): Specific type of DDoS attack tool or vector that primarily targets layer 7 of OSI. Known for its ability to conduct sophisticated and high volume attacks
- TDL4 was most active and resilient botnets in 2011.

### 36. DDoS UDP Application Flood
- Flood of UDP transport application traffic at a target service

### 37. DDoS UDP Chargen Reply Flood (Client simulator):
- Chargen service: Simply sends out a string of characters for purpose of basic troubleshooting

### 38. DDoS UDP Flood

### 39. DDoS UDP fragmentation
- Overwhelming the reassembly process

### 40. High Orbit Ion Cannon
- Successor of LOIC. Open source
- Works via application layer. HTTP flood DDoS attack
- Can target 256 sites simultaneously
- Use Swedish proxies to obfuscate their location
- IP reputation filtering

### 41.Mirai Botnet
- Mirai malware affects smart devices running on APC processor turning them into network of remotely controlled bots
- If default username and password are not changed of IoT services, it can be infected with Mirai botnet
- Mirai is mutating. Has given both to Okiru, Satori, Masuta, Pure Masuta, OMG strain, IOTrooper, reaper

### 42. QUIC Flood DDoS
- QUIC Protocol: Transport layer protocol theoretically replacing TCP and TLS. HTTP v3 runs on QUIC
- Flood QUIC traffic to overwhelm the server
