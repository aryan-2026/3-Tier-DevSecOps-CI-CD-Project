# 3-Tier-DevSecOps-CI-CD-Project
A complete hands-on DevSecOps project demonstrating how to build a secure CI/CD pipeline from scratch by integrating static code analysis, dependency scanning, container security, and automated deployment using Jenkins on AWS.

What This Pipeline Does (High Level)

Whenever Jenkins runs the pipeline, it performs these steps in order:

Pulls the latest code from GitHub

Runs SonarQube to analyze code quality and security

Scans dependencies using OWASP Dependency Check

Enforces Sonar Quality Gates

Scans the project filesystem using Trivy

Deploys the application using Docker Compose

If security issues are found, you’ll see them immediately in Jenkins — no guessing, no manual checking.
