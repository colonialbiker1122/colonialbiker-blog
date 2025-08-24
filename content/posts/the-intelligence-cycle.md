+++
date = '2025-08-03T21:51:09+05:30'
draft = false
title = 'The Intelligence Cycle'
categories = ['Cyber Threat Intel']
+++
## Stages
1. Planning and targeting
  - Identify intelligence requirements
  - Identify key assets, security concerns, etc
  - Identify potential threats and corresponding mitigations
2. Preparation and Collection
  - Defining and developing collection methods to obtain information regarding requirements
3. Processing and Exploitation
4. Analysis and Production
5. Dissemination and integration
  - What are the most pressing issues?
  - How urgent is the intel? How much detail recipient needs?
6. Evaluation and Feedback

## Defining Intelligence Requirements (IR)
- IR is any subject, general or specific, upon which there is a need for collection of information
- IR is a requirement for intelligence to fill a gap in the command’s knowledge or understanding of the battlespace or threat forces
- What’s the mission of my organisation?
- What threat actors are interested in my industry?
- What threat actors are known for targeting my area of operation?
- What asset does my organisation protect?
- What threat actors could target my organization in order to reach another company I supply for?
- Had my organisation been targeted previously?
- To validate the priority for any IR,
  - Specificity of question
  - Necessity of question
  - Feasibility of collection
  - Timelines of intelligence
## Collection process
- Internal: networks, endpoints etc
- External : Blogs, public DB, forums, Threat Intel feeds
- Collection Management Framework (CMF)
- IoC: Indicator of compromise: hashes, URLs, domains, IPs, paths, filenames, registry keys, malware files
  - Quality over quantity of IoC becomes crucial
- Dropper : installs malware
- C2: attacker controlled computer server
  - For C2 communications, threat actors use cloud-based services, emails, blogs, comments, github repos, DNS queries etc.
- Honeypots: Decoy which imitates possible target of attacks
  - Low interaction: transport layer, limited access to OS
  - Medium interaction: Application layer
  - High interaction: Involve real OS and apps to imitate

## Processing and exploitation
3 commonly used frameworks are as follows:
- The Cyber Kill Chain (Lockheed Martin)
  - Reconaissance: Non invasive techniques to know victim
  - Weaponisation: Generating malicious payloads
  - Delivery: Deliver the weaponised artifact
  - Exploitation : Achieving code execution on victim’s system by exploiting the vulnerability
  - Installation: Installing final malware piece
  - C2: Establishing channel to communicate with the malware on victim’s system
  - Actions on objective: Attacker achieves the goal
- Diamond model: Adversary, Infrastructure, Capability, Victim
- MITRE ATT&CK framework: Enterprise, cloud, smartphones, ICS

## Bias and analysis
- Critical thinking for strategic intel (Pherson and Person, 2016)
- Psychology of intelligence analysis
- Structured analytical techniques for Intelligence analysis
