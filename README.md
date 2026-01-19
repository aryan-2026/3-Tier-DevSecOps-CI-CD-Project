# 3-Tier-DevSecOps-CI-CD-Project
A complete hands-on DevSecOps project demonstrating how to build a secure CI/CD pipeline from scratch by integrating static code analysis, dependency scanning, container security, and automated deployment using Jenkins on AWS.

## What This Pipeline Does

1. Pulls the latest code from GitHub  
2. Runs SonarQube to analyze code quality and security  
3. Scans dependencies using OWASP Dependency Check  
4. Enforces Sonar Quality Gates  
5. Scans the project filesystem using Trivy  
6. Deploys the application using Docker Compose  

## Pipeline Flow
GitHub Repository
↓
Jenkins Pipeline
↓
SonarQube (SAST)
↓
OWASP Dependency Check (SCA)
↓
Quality Gate Validation
↓
Trivy Filesystem Scan
↓
Docker Compose Deployment

## Prerequisites

- Jenkins installed and running
- Docker & Docker Compose installed
- SonarQube running
- Trivy installed
- OWASP Dependency Check plugin installed
- Jenkins configured to run Docker commands
- Required Jenkins plugins:
  - SonarQube Scanner
  - OWASP Dependency Check
  - Docker Pipeline
  - Git
  - Quality Gates

Stage-by-Stage Explanation
1. Code Clone

Pulls latest code from GitHub devops branch.

2. SonarQube Scan (SAST)

Scans code for bugs, vulnerabilities, code smells, and security issues.

3. OWASP Dependency Check (SCA)

Scans third-party libraries against CVE databases.

4. Quality Gate

Validates code quality before deployment.

5. Trivy Filesystem Scan

Detects vulnerable packages, misconfigurations, and secrets.

6. Docker Compose Deployment

Deploys the application in detached mode using Docker Compose.

![Jenkins Pipeline](https://github.com/aryan-2026/3-Tier-DevSecOps-CI-CD-Project/blob/main/pipeline.png)
![Stage View](https://github.com/aryan-2026/3-Tier-DevSecOps-CI-CD-Project/blob/main/stages.png)
![CI/CD Build](https://github.com/aryan-2026/3-Tier-DevSecOps-CI-CD-Project/blob/main/build.png)


## Final Outcome

- Automated secure CI/CD pipeline
- Early vulnerability detection
- Clean and repeatable deployments
- Real DevSecOps workflow
