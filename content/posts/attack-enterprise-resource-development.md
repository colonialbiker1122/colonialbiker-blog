+++
date = '2025-09-03T19:52:52+05:30'
draft = false
title = 'MITRE ATT&CK - Enterprise - Resource Development'
+++
- Adversaries creating, purchasing, compromising, stealing resources like infrastructure, accounts, capabilities etc

## Acquire Access
- Purchase/ acquire existing access to target system/ network via brokers who sell previously compromised systems

## Acquire Infrastructure
- Buy/ lease/ rent/ physical or cloud/ domains/ web services etc
  - Domains: Domain names
  - DNS server: For post-compromise activity, C&C etc
  - Virtual Private Server: To rapidly provision, modify, shutdown infra etc
  - Servers: To stage, launch, execute operations, water hole operations, C&C, phishing etc
  - Botnet: Subscription from botnet, booter/ stresser service
  - Web services: Abused for C&C, phishing, exfiltration over web etc
  - Serverless: Cloudflare workers, AWS lambda etc
  - Malvertising: Using ads to distribute malware to victims

## Compromise Accounts
- Rather than creating/ establishing accounts as utilising an existing persona has level of trust in potential victim
- Social media accounts: Compromise existing accounts
- Email accounts: To conduct phishing, spam email campaigns, acquire infrastructure
- Cloud accounts: Dropbox, S3, to upload tools, exfiltration to cloud storage

## Compromise infra
- Physical, cloud, domain, network, infrastructure, web, DNS etc
  - Domains: Domain registration hijacking, social engineering, A domain registration help desk, advantage of renewal process gaps etc
  - DNS server: Compromise 3rd party DNS, servers for C&C etc
  - Virtual Private Server
  - Server
  - Botnet
  - Web services
  - Serverless
  - Network devices: Small office/ home office routers etc

## Develop capabilities
- Malwares, exploits ,self-signed certificates etc
  - Malware: Payloads, droppers, post-compromise tools, backdoors etc
  - Code signing certificates: Create self-signed code signing certificates
  - Digital certificates: Adversaries create self-signed SSL/TLS certificates
  - Exploits: Through fuzzing, patch analysis etc

## Establish Accounts
- To create persona for public information, presence, history affiliations for social media, website, to scrutinize for legitimacy
- Social media accounts
- Email accounts: To conduct phishing, acquire infra, etc
- Cloud accounts

## Obtain Capabilities
- Purchase, freely download or steal
  - Malware: To support operations, maintain control, evade defences etc
  - Tool: Procure commercial software licenses (cobalt strike, PsExec etc)
  - Code signing certificates
  - Digital certificates
  - Exploits
  - Vulnerabilities: Gain information via open/ closed vulnerability databases
  - AI: To aid various techniques, to inform bolster, enable tasks, conduct recon, create scripts, create payloads, assist social engineering etc

## Stage capabilities 
- Upload, install, stage capabilities on infra
  - Upload Malware: To support operations, to enable ingress tool transfer
  - Upload tool: Making it available to victim network
  - Install digital certificate
  - Drive by target: Prepare operational environemnt to infect systems
  - Link target: Put in place resources which can be referenced by a link
  - SEO poisoning
