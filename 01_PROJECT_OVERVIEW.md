# Secure CI/CD Lab

## Project Purpose

This project demonstrates how cybersecurity controls can be integrated into a CI/CD pipeline.

The project is designed from a cybersecurity perspective, focusing on protecting:

- Source code
- Dependencies
- Secrets
- Application code
- CI/CD workflows
- Docker images
- Build processes

## Project Environment

Operating System:
Windows

Tools:

- Git
- GitHub
- GitHub Actions
- Python
- Flask
- Docker
- CodeQL
- Trivy
- Gitleaks
- pip-audit

## Project Flow

Developer
↓
Local Git Repository
↓
GitHub Repository
↓
GitHub Actions
↓
Application Test
↓
Dependency Security Scan
↓
Secret Detection
↓
CodeQL SAST
↓
Docker Build
↓
Container Security Scan
↓
Secure Delivery

## Main Security Controls

1. Application syntax testing
2. Dependency vulnerability scanning
3. Secret detection
4. Static Application Security Testing
5. Docker image scanning

## Security Objective

The objective is to detect security and quality problems as early as possible in the software delivery process.

## Repository

https://github.com/batoul0101/secure-cicd-lab
