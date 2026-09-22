# CI/CD Workflow

## Trigger

The GitHub Actions workflow runs when code is pushed to the main branch.

It also runs for Pull Requests targeting main.

## Workflow

```text
Git Push
   |
   v
GitHub Actions
   |
   v
Checkout Code
   |
   v
Python Setup
   |
   v
Application Test
   |
   v
Dependency Scan
   |
   v
Secret Detection
   |
   v
CodeQL SAST
   |
   v
Docker Build
   |
   v
Container Security Scan
   |
   v
Security Result
