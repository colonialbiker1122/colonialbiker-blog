+++
date = '2025-08-04T20:54:31+05:30'
draft = false
title = 'Threat Hunting'
categories = ['Cyber Threat Intel']
+++
## Introduction
- Human driven activity of proactively and iteratively searching through the organisation’s environment (network, endpoints, apps etc) for signs of compromise in order to shorten the dwell-time and minimise the breach impact for the on.
- Types
  - Data-driven
  - Intel-driven
  - Entity-driven
  - TTP-driven
- Pyramid of pain: How much pain will be caused to adversaries to change their ways once you have identified their IoCs, network infra, etc.
  - TTP -> Tools -> Network/Host Artifact -> Domain names -> IP Addresses -> Hash Values

## Threat Hunting Maturity Model
- Used to classify the team’s detection capability.
  1. Initial: Automated alerting. Little or no routine data collection
  2. Minimal: Use CTI indicators. Moderate/ high routine data collection
  3. Procedural: Use data analysis procedures created by others
  4. Innovative: Create new data analysis procedures
  5. Leading: Automate majority of successful dat analysis procedure
- Threat hunting loop:
  - Build Hypothesis —> Start Investigation —> Uncover Anomalies/ Patterns -> Prove/ Disprove Hypothesis -> Automate Result —> Inform and enrich Analytics

## SANS Threat Hunting Model (Dan Gunther)
1. Purpose: State purpose of hunt, data, desired outcome.
2. Scope: Define hypothesis, identify network etc to get data
3. Equip: How to collect data, collect enough data, how to analyze, how to avoid bias, implement CMF (Collection Management Framework)
4. Plan review
5. Execute
6. Feedback: Improve previous stages

## Data Driven Methodology (Rodriguez brothers) InsomniHack
### 1. Define research goal: Understand and map data to adversary
  - What is it that we are going to hunt?
  - Do I understand my data? Do I have data wiki?
  - Do I have data stored somewhere in my environment?
  - Have we mapped logs to adversary action?
  - How specific do I have to be?
  - How many techniques can I cover per hypothesis?
  - Focus on technique enabler or main behaviour?
### 2. Modelling the data
  - Understanding where data comes from
  - Send logs to data lake to consult it
  - Structure data by creating data dictionaries
  - Try mapping each data source to an event
  - OSSEM: Open Source Security Events Metadata
### 3. Emulating the adversary:
  - Way for red teamers to replicate adversary behaviours in organisation environment
### 4. Defining detection model:
  - Way to carry out the hunt
### 5. Validating detection model:
- Try detection in production
- Zero results: Adversary behaviour not present
- Atleast one result: Look closer at results to confirm breach
- High volume of result: adjust process and try again
### 6. Documentation:

*Check project Helk and Project Mordor and Threat Hunter Playbook*

## TaHiTI: Targeted Hunting Integrating Threat Intelligence
### Phase 1: Initiate
- Trigger hunt
- Create Abstract: Rough description of hypotheses
- Store in backlog
- 5 major trigger categories:
  1. Threat intelligence
  2. Other hunting investigations
  3. Security monitoring
  4. Security Incident Response: Historical incident / RT exercise
  5. Others
### Phase 2: Hunt
- Define / refine:
  1. Enrich investigation abstract
  2. Determine hypothesis
  3. Determine data sources
  4. Determine analysis techniques
- Execute
  1. Retrieve data
  2. Analyse data
  3. Validate hypothesis
- 3 possible outcomes of each hunt:
  1. Hypothesis proved: Security incident uncovered
  2. Hypothesis unproved
  3. Inconclusive result: Insufficient information to prove/ disprove
### Phase 3: Finalise
- Handover
- Document findings
- Update backlog
- 5 processes which maybe triggered as result of investigation
  - Security Incident Response: Initiate an IR processes
  - Security Monitoring: Create/ update use cases
  - Threat Intelligence: Uncover new threat actor’s TTPs
  - Vulnerability Management: Resolution of vulnerabilities
  - Recommendations for other teams

## Building a hypothesis
- Threat intelligence based: Rightfully contextualised IoCs, threat landscape, Geopolitical context
- Situational awareness based: Identify the most important assets. Try considering people, processes, business too
- Domain expertise-based - Threat hunter’s expertise
