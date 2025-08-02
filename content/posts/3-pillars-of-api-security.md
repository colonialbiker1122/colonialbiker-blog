+++
date = '2025-08-02T12:56:34+05:30'
draft = false
title = '3 Pillars of API Security'
+++
## 1. Governance
- Know your APIs
  - Get full inventory of APIs : Purpose, owner, documentation etc.
  - Standardise and enforce API deployment process
  - Check for existence of shadow/ rogue APIs, proper validation, governance at gateway and marketplace.
  - API Documentation : Mandatory
  - API development standards: style guides, authentication requirements, versioning, PII tracking
- Threat modelling:
  - Identify APIs, business flows, data access paths
  - Assess: vulnerabilities, logic flows, access controls, 3rd party risks
  - Probability:
  - Impact: Understand the damage/ loss/ consequences
  - Mitigation: Develop plans to assess the risk and mitigation strategies
- OpenAPI specification AKA Swagger
- Design guides:
  - Authentication: Type (token/ certificate etc.), how to implement.
  - Authorisation: Who has access to what
  - Naming conventions: URIs as nouns, methods as verbs, pluralisation, hierarchy, case, language
  - Error codes: status code, reference ID , human readable
  - Versioning: when to increment, when not to
  - Units/ formats/ standards: date/time, timezone

## 2. Testing
- Data security:
  - Access Control
  - Excessive/ Sensitive Data Exposure
  - File / directory exposure
  - Encryption at rest
- Business logic: 
  - Cross-account access
  - API function abuse
  - RBAC: Role-based Access Control
  - Pen-testing
- API security
  - Unsecured endpoints
  - Authentication exploits
  - Enumeration
  - Application DoS, Rate Limiting
  - Missing SSL/ TLS issues
  - Injection, fuzzing
  - Server Side Request Forgery
## 3. Monitoring
- Runtime protection
  - Policy enforcement
  - Authentication
  - Traffic filtering
- Threat detection
  - Fraudulent traffic
  - Distributed attacks
  - Incident Response
- Control validation
  - Verify API controls
  - Uncover anomalies
- API Discovery sources
  - API gateway
  - Web Application Firewall
  - Code repository
  - Application crawling
