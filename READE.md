# SOP: Common Linux Commands

| Author | Created On | Version | Last Updated By | Internal Reviewer | Reviewer L0 | Reviewer L1 | Reviewer L2 |
|--------|------------|---------|------------------|-------------------|-------------|-------------|-------------|
| Ajitesh Singh | 21-01-2026 | v1.1 | Ajitesh Singh | NA | NA | NA | NA |

---

## Table of Contents

- [Introduction](#introduction)
- [Pre-requisites](#pre-requisites)
- [Purpose](#purpose)
- [Key Features](#key-features)
- [Environment Verification](#environment-verification)
- [Command Reference](#command-reference)
  - [System Monitoring](#system-monitoring)
  - [File Operations](#file-operations)
  - [User & Permission Commands](#user--permission-commands)
  - [Network Commands](#network-commands)
  - [Process & Service Commands](#process--service-commands)
- [Contact](#contact)
- [References](#references)

---

## Introduction

This document provides a Standard Operating Procedure (SOP) for frequently used Linux commands. It helps users perform basic system tasks such as monitoring system health, managing files, checking network connectivity, and controlling running processes.

The SOP focuses on clarity, correctness, and practical usage.

---

## Pre-requisites

| Requirement | Description |
|-------------|-------------|
| Operating System | Linux-based system |
| User Access | Valid login credentials |
| Privileges | Sudo access when required |
| Terminal | Command-line interface |
| Basic Knowledge | Familiarity with Linux shell |

---

## Purpose

- Standardize usage of common Linux commands  
- Improve operational efficiency  
- Reduce execution errors  
- Support troubleshooting and learning  

---

## Key Features

| Feature | Description |
|--------|-------------|
| Simple Commands | Easy to understand syntax |
| Real Examples | Commands reflect real usage |
| Structured Layout | Categorized for clarity |
| Distribution Independent | Works on most Linux systems |
| Operational Ready | Safe for daily operations |

---

## Environment Verification

No installation is required. Most Linux distributions include the required commands by default.

Verify user identity:
```
whoami
```

Verify shell availability:
```
echo $SHELL
```

Verify basic command availability:
```
ls --version
```

---

## Command Reference

### System Monitoring
```
uptime
free -h
df -h
top
hostname
```

---

### File Operations
```
pwd
ls -lh
mkdir demo
touch demo.txt
cp demo.txt backup.txt
mv backup.txt archive.txt
rm archive.txt
cat demo.txt
```

---

### User & Permission Commands
```
whoami
id
groups
chmod 755 script.sh
chown user:user file.txt
passwd user1
```

---

### Network Commands
```
ip a
ping google.com
curl http://localhost
ss -tunlp
hostname -I
```

---

### Process & Service Commands
```
ps aux
kill <pid>
systemctl status ssh
systemctl restart ssh
journalctl -xe
```

---

## Contact

| Name | Email Address | GitHub | URL |
|------|---------------|--------|-----|
| Ajitesh Singh | ajitesh.singh.snaatak@mygurukulam.co | ajitesh0007 | https://github.com/ajitesh0007 |

---

## References

| Link | Description |
|------|-------------|
| https://linuxcommand.org | Linux command documentation |
| https://man7.org/linux/man-pages | Linux manual pages |
| https://ubuntu.com/server/docs | Ubuntu server documentation |

---
