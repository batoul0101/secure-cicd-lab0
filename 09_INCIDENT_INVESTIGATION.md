# CI/CD Incident Investigation

## Purpose

CI/CD is part of the organization's security attack surface.

A compromised pipeline could affect:

- Source code
- Build artifacts
- Container images
- Secrets
- Deployment

## Investigation Process

```text
Alert
  ↓
Identify Workflow
  ↓
Identify Commit
  ↓
Identify Changed Files
  ↓
Read Logs
  ↓
Find Root Cause
  ↓
Fix
  ↓
Retest
  ↓
Document
```

## Example

### Incident

The application test failed.

### Workflow Error

```text
No such file or directory: 'app.pypile'
```

### Commit

```text
ef6c41a
```

### Investigation

The workflow file was checked.

The Python compilation command contained a filename typo.

### Root Cause

Incorrect filename.

### Correct Command

```text
python -m py_compile app.py
```

### Fix

The workflow was corrected.

### Verification

New commit:

```text
3413bfb
```

The workflow then completed successfully.

## Investigation Questions

When investigating a CI/CD incident ask:

1. Which workflow ran?
2. Which commit triggered it?
3. Who pushed the commit?
4. Which files changed?
5. Which job failed?
6. What was the exact error?
7. Were secrets involved?
8. Were third-party Actions involved?
9. Was an artifact created?
10. Did the failure affect deployment?
