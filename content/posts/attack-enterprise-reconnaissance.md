+++
date = '2025-09-03T19:21:54+05:30'
draft = false
title = 'MITRE ATT&CK - Enterprise - Reconnaissance'
+++
- Actively or passively gather information of victim organization/ infrastructure/ staff etc.

## Active Scanning
- Probe victim infrastructure via network traffic
- Scanning IP blocks: public IPs
- Vulnerability Scanning: Configurations of target host/ applications, versions etc
- Wordlist Scanning: Bruteforcing, Crawling, to identify content and infrastructure (like if an SQLDB is MySQL, Oracle, Ppostgress etc).

## Gather Victim host information
- Administrative data, configs, etc
- Hardware: Types, versions, additional components etc
- Software: Types, versions, additional components, etc (AV, SIEM, etc)
- Firmware: Types, versions, configurtions, age, patch-level etc
- Client Configuration: Settings, OS, versions, architecture, language, virtualisation

## Gather victim identity information
- PII, credentials, MFA configurations etc
- Credentials: User tendency to use same passwords across accounts
- Emails: Organizations having public facing email infrastructure and addresses of employees
- Employee names: To derive emails, craft more believable lures

## Gather victim network information
- Administration data, topology, operations etc
- Domain: What domains, their owners, administrative data, nameservers etc
- DNS: Registered Nameservers, mailserver, DNS, MX, TXT, SPF records etc
- Network topology: Physical/ logical, gateways, routers etc
- IP addresses: To derive organization size, physical location, ISP etc
- Network trust dependencies: 3rd party organizations, ISP, contractors etc
- Network security applications: Firewalls, filters, proxies, NIDs etc

## Gather victim organization information
- Divisions, departments, business operations, roles, responsibility
- Gather physical locations: Key resources, Infrasrucure, authorities, victims etc
- Identify roles: PII, data resources
- Business relationships: 3rd party organizations, domains, contracts, network access
- Identify business tempo: Operational working hours, purchases, shipments etc

## Phishing for information
- Objective is to gather data from victim
- Spear phishing service: Social engineering, credentials, actionable information
- Spear phishing attachment/ link/ voice: Posing as a source with a reason to collect information like establish or compromise accounts, send urgent messages etc

## Search closed sources
- Available for purchase from private sources, databases, paid subscriptions, feeds of threat intel, dark web, cyber blackmarkets
- Threat intel vendors: Target industries, attribution claims, successful TTPs/ countermeasures etc from paid feeds/ portals from threat intel
- Purchase technical data: From private sources, databases, darkweb etc

## Search open technical databases
- Databases, repositories, domains, network, artifacts etc
- DNS/ passive DNS: Records like nameservers, subdomains, mailservers etc
- WHOIS: Assigned IP blocks, contact info, DNS nameservers
- Digital certificates: Contain information of company name, location
- CDN: Gain data about victim
- Scan DBs: Internet scans/ surveys, IPs, hostnames, ports, certificates, server banners

## Search open websites/ domains 
- From Social Media, news, hirings, contracts awarded etc
- Social media: Victim organization, business announcements, roles, locations, staff
- Search engines
- Code repositories: GitHub, GitLab, Sourceforge, BitBucket etc

## Search victim owned websites
- Departments/ divisions, locations, names, roles, contact info, business operations, relationships etc
