# Commands Reference

## Git

```powershell
git --version
git init
git status
git add .
git commit -m "Commit message"
git push
git push -u origin main
git remote -v
```

## GitHub Remote

```powershell
git remote add origin https://github.com/batoul0101/secure-cicd-lab.git
```

## Test GitHub Actions

```powershell
git commit --allow-empty -m "Test GitHub Actions"
git push
```

## Python

```powershell
python -m py_compile app.py
```

## Docker

```powershell
docker --version
docker compose version
docker build -t secure-cicd-lab:latest .
docker images
docker ps
docker run -d -p 5000:5000 --name secure-cicd-app secure-cicd-lab:latest
docker stop secure-cicd-app
docker rm secure-cicd-app
```

## PowerShell

```powershell
pwd
dir
cd C:\Secure-CICD-Lab
```

## Open CI Workflow

```powershell
notepad .github\workflows\ci.yml
```
