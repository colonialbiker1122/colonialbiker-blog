+++
date = '2025-09-07T22:44:18+05:30'
draft = false
title = 'MITRE ATT&CK - Enterprise - Execution'
+++
- Adversary is trying to run malicious code on local/remote system

## Cloud Administration Command 
- Abuse cloud management services like AWS systems manager/ Azure run command to remotely run scripts in VMs

## Command & Scripting Interpreter
- Unix shell, Windows CMD, PowerShell etc
  - PowerShell: Info-discovery, code execution, start process cmdlet etc
  - AppleScript: macOS scripting language, AppleEvent messages can locate open windows, send keystrokes, interact locally/ remotely etc
  - Windows command shell: Command can be invoked remotely by SSH etc
  - Unix Shell: Primary command prompt on Linux/ MacOS systems
  - Visual Basic: Has interoperability with many windows technologies like native API and component object model, Supported in .NET framework etc
  - Python
  - JavaScript: JS can be executed in runtime environment even outside the browser 
  - Network device CLI: To execute payloads
  - CloudAPI: CLIs in browser shells, SDKs, Azure for PowerShell etc
  - AutoHotKey & AutoIT: Scripting language to automate windows tasks

## Container Administration Command 
- Docker daemon, Kubelet etc

## Deploy container
- Deploy a new container to execute/ download malware, configured without network rules, user limitations etc to bypass defences 
- Example: Attempt to deploy privileged/ vulnerable container, escape host and access other control.

## Exploitation for client execution
- Exploit software vulnerabilities in client environment

## Interprocess Communication
- Abuse IPC mechanism for local code execution 
  - Component Object Model: Use Windows COM for local code execution 
  - Dynamic data exchange: Use Windows DDE to execute arbitrary commands
  - XCP services : by MacOS

## Native API 
- Interact with native OS API to execute behaviours

## Scheduled tasks/ jobs 
- Scheduling tasks in local/ remote systems
  - At: Executable in Windows/ Mac/ Linux to perform task scheduling
  - Cron: Time based job scheduler for unix-like OS
  - Scheduled task: Windows task scheduler for initial/ recurring code execution
  - Systemd timers: Alternatives to cron. Can be remotely activated
  - Container orchestration job: kubernetes etc

## Serverless Execution 
- Compute engines, application integration services etc

## Shared Modules 
- Executable files loaded into processes to provide access to reusable code like custom functions, invoke OS API functions etc

## Software deployment tools 
- SCCM, HBSS, Altiris, AWS system Manager etc 

## System Services 
- Abuse services for one-time or temporary execution 
  - Launctl: Interfaces with Launchd, server management framework for MacOS
  - Service execution: Abuse Windows Service Control Manager (services.exe)

## User Execution
- Rely on actions by user to gain execution 
  - Malicious link: link leading to code executions 
  - Malicious file: .doc, .pdf, .xls, .rtf, .scr, .exe, .lnk, .pif, .cpl
  - Malicious image: AWS amazon machine images, GCP images etc
 
## Windows Management Instrumentation 
- Admin feature to access Windows system components
