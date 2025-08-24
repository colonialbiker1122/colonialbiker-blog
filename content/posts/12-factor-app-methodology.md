+++
date = '2025-08-10T08:43:13+05:30'
draft = false
title = '12 Factor App Methodology'
categories = ['DevOps']
+++
### 1. Codebbase
- Version control system like Git
### 2. Build, Release, Run
- Build: Transform codebase to executable unit
- Release: Combine build with config
- Run: Run the application
### 3.Development-Production parity
- Minimise difference between deployment/ production environment.
### 4. Dependencies
- Explicitly declare all dependencies
### 5. Configuration
- Store configuration in environment variables
- Keep everything that varies between deployments in configurations
### 6. Backend services
- Do not distinguish between local/ 3rd party services
- Access all services by a URL and credentials
### 7. Processes
- Stateless
- Persistent data in a database
### 8.Port binding
- Export services by a port binding
- Declare web server library as a dependency
### 9. Concurrency
- Scalability
### 10. Disposability
- Minimal startup time and graceful termination
### 11. Logs
- Treat logs as an event stream
### 12. Admin processes
