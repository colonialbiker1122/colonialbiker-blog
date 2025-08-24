+++
date = '2025-07-20T23:56:44+05:30'
draft = false
title = 'Nmap Basics'
categories = ['Vulnerability Assessment']
+++
## 1. Network discovery
- Find out IP address ranges
- Determine estimated services offered by a host
- Figure out general network topology
- Check for Firewall filtering policies
- sL : List scan
- A : Advanced / Aggressive
- Finding an organization's IP address :
  - host -t ns target.com
  - host -t a target.com
  - host -t aaaa target.com
  - host -t mx target.com
  - host -t soa target.com
  - nmap -Pn -T4 –-traceroute target.com
  - whois <x.x.x.x>

## 2. Host discovery
- nmap -sL abc.com
- nmap -sn -t4 abc.com : Ping scan
- nmap -Pn -t4 abc.com : Disable Ping 
- nmap -sn -PS8O -v abc.com : TCP SYN Ping
- nmap -sn -PA8O -v abc.com: TCP ACK Ping
- nmap -sn -PU -v abc.com : UDP Ping
- nmap -sn -PE -v abc.com : ICMP Ping (8/echo)
- nmap -sn -PR -v abc.com : ARP Scan
- nmap -sn -PE -PS443 -PA80 -PP abc.com : Default

## 3. Port Scanning
- Open : accepting TCP connections
- Closed : Accessible but no application listening
- Filtered : Not able to determine if port is open ( Firewall )

