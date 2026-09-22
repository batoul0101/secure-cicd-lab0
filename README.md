# Secure CI/CD Lab

## Project Overview

This project demonstrates a Secure CI/CD Pipeline designed to integrate cybersecurity controls into the software development lifecycle.

The project uses a simple Python application and integrates security checks into GitHub Actions.

The objective is to detect security and quality issues before application changes progress toward deployment.

---

## Project Goal

The main goal is to protect application code during the CI/CD lifecycle.

The pipeline performs automated checks for:

- Application errors
- Dependency vulnerabilities
- Exposed secrets
- Source-code security issues
- Docker image security

---

## Project Architecture

```text
Developer
    |
    v
Git Repository
    |
    v
GitHub Repository
    |
    v
GitHub Actions
    |
    +----------------------+
    |                      |
    v                      v
Application Test       Security Checks
                           |
              +------------+------------+
              |            |            |
              v            v            v
         Dependency    Secret       CodeQL
            Scan       Detection      SAST
              |            |            |
              +------------+------------+
                           |
                           v
                     Docker Build
                           |
                           v
                  Docker Image Scan
                           |
                           v
                    Security Gate
                           |
                           v
                    Build Candidate
