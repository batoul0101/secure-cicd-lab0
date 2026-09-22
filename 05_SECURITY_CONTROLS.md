# Security Controls

## 1. Source Code Protection

Git provides traceability for source-code changes.

Each change is associated with a commit.

## 2. Application Testing

Command:

```powershell
python -m py_compile app.py
```

Purpose:

Detect syntax errors.

## 3. Dependency Security

Tool:

pip-audit

Purpose:

Detect known vulnerabilities in Python dependencies.

## 4. Secret Detection

Tool:

Gitleaks

Purpose:

Detect accidentally committed secrets.

Examples:

* Passwords
* API keys
* Tokens
* Private keys

## 5. Static Application Security Testing

Tool:

CodeQL

Purpose:

Analyze source code for security vulnerabilities.

## 6. Container Security

Tool:

Trivy

Purpose:

Scan the Docker image for known vulnerabilities.

## 7. Workflow Security

The CI/CD workflow itself is an attack surface.

Important security areas:

* Workflow permissions
* Third-party Actions
* Secrets
* Pull Requests
* Runner security
* Supply-chain security

## 8. Defense in Depth

The project uses multiple security controls:

```text
Application Test
       +
Dependency Scan
       +
Secret Detection
       +
CodeQL
       +
Container Scan
```

No single security control is relied upon alone.
