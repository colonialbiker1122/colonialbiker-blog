+++
date = '2025-07-23T19:39:40+05:30'
draft = false
title = 'OWASP API Security Top 10'
categories = ['API Security']
+++
## 1. Broken Object level Authorisation 
- Access data / objects belonging to other users.
- Attacker authenticates as user A and retrieves data of B
- Enforce data access controls at application logic layer
- Define data access policies and implement controls


## 2. Broken authentication
- Due to poorly implemented or missing security controls
- Weak password requirements, credential stuffing, authentication information in URLs, absence of token expiry validation, insecure password storage, no captcha/ rate limiting / lockout


## 3. Broken object property level authorisation
- Mass assignment : Ability to update object elements
- Excessive data exposure : reeling unnecessary sensitive data
- Eg. set account-type=premium

## 4. Unrestricted resource consumption
- Risk : DoS, performance impact, mass data harvesting.
- Missing / inadequate rate controls, execution timeouts, max-allocation memory/ files / upload size, excessive operations or records returned in a single request

## 5. Broken function level authentication
- Improperly modify objects (create/ update / delete) to escalate privileges, replace GET → PUT / DELETE
- Modify parameters : role=admin, delete an invoice, set account balance = 0


## 6. Unrestricted access to sensitive business flows
- Application logic flow
- Implement fraudulent traffic detection and control

## 7. Server side request forgery
- Exploiting URL inputs to make request to 3rd party server
- Eg. LFI , Malware downloaded from malicious sites
- Validate and sanitise all user-supplied info (URL params)
- Ensure communication only permitted with trusted resources

## 8. Security misconfiguration
- Lack of security hardening, improperly configured permissions, missing security patches, CORS policy missing, use of bots to scan, detect and exploit misconfigurations
- Implement hardening procedures.

## 9. Improper inventory management
- Unauthorised API access via old/unused versions or through trusted 3rd parties
- Unpatched endpoints, outdated documentation, deploy/manage all APIs in gatewa

## 10. Unsafe consumption of APIs
- 3rd party APIs are exploited and then used to attack legitimate APIs relying on them.
- Validate data and evaluate security controls of 3rd APIs , encrypt API communication.
