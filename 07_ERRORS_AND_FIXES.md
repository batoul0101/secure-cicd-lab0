# Errors and Fixes

## Error 1 - GitHub Actions Billing / Runner

### Error

```text
The job was not started because recent account payments have failed or your spending limit needs to be increased.
```

### Cause

GitHub Actions could not start the runner because of the account/usage restriction.

### Action

The GitHub account and repository settings were checked.

The workflow was tested again after resolving the issue.

### Verification

```powershell
git commit --allow-empty -m "Test GitHub Actions"
git push
```

The workflow successfully executed.

---

## Error 2 - Wrong Python Filename

### Error

```text
Run python -m py_compile app.pypile app.py

[Errno 2] No such file or directory: 'app.pypile'
```

### Cause

The workflow contained:

```text
app.pypile
```

instead of:

```text
app.py
```

### Fix

Changed the command to:

```text
python -m py_compile app.py
```

### Result

The workflow succeeded.

Commit:

```text
3413bfb
```

Message:

```text
Fix application test
```

---

## Error 3 - Dockerfile Extension

### Error

```text
fatal: pathspec 'Dockerfile' did not match any files
```

### Investigation

The file was:

```text
Dockerfile.txt
```

instead of:

```text
Dockerfile
```

### Fix

Renamed:

```text
Dockerfile.txt
```

to:

```text
Dockerfile
```

### Result

The Dockerfile was successfully committed.

---

## Error 4 - Docker Engine Not Running

### Error

```text
failed to connect to the docker API
```

### Cause

Docker Desktop Linux Engine was not running.

### Fix

Docker Desktop was started.

### Test

```powershell
docker build -t secure-cicd-lab:latest .
```

### Result

Docker successfully started the build.

---

## Error 5 - GitHub Authentication

### Message

```text
info: please complete authentication in your browser...
```

### Meaning

Git required GitHub authentication.

### Fix

Complete the authentication process in the browser.

### Result

Push completed successfully.

---

## Troubleshooting Method

For every error:

```text
Error
  ↓
Read Error Message
  ↓
Identify Component
  ↓
Find Root Cause
  ↓
Apply Fix
  ↓
Run Test Again
  ↓
Verify Result
  ↓
Document
```
