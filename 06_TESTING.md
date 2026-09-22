# Testing

## Test 1 - Git Status

Command:

```powershell
git status
```

Purpose:

Verify the local repository state.

---

## Test 2 - Git Push

Command:

```powershell
git push
```

Purpose:

Verify communication with GitHub.

Expected result:

```text
main -> main
```

---

## Test 3 - GitHub Actions

A test commit was created:

```powershell
git commit --allow-empty -m "Test GitHub Actions"
```

Then:

```powershell
git push
```

Result:

GitHub Actions successfully executed.

---

## Test 4 - Dependency Security

The dependency security scan completed successfully.

---

## Test 5 - CodeQL

CodeQL was added to the workflow.

The CodeQL workflow completed successfully.

---

## Test 6 - Docker Build

Command:

```powershell
docker build -t secure-cicd-lab:latest .
```

Purpose:

Verify that the application can be packaged as a Docker image.

---

## Test 7 - Docker Runtime

Command:

```powershell
docker run -d -p 5000:5000 --name secure-cicd-app secure-cicd-lab:latest
```

Purpose:

Run the application container locally.

---

## Test Result

The project successfully demonstrated:

* Git
* GitHub
* GitHub Actions
* Application testing
* Dependency scanning
* Secret detection
* CodeQL
* Docker build
* Container security
