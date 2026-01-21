# SOP: Common Linux Commands

| Author | Created On | Version | Last Updated By | Internal Reviewer | Reviewer L0 | Reviewer L1 | Reviewer L2 |
|--------|------------|---------|------------------|-------------------|-------------|-------------|-------------|
| Ajitesh | 21-01-2026 | v1.0 | Ajitesh | NA | NA | NA | NA |

---

## Table of Contents

- [Introduction](#introduction)
- [Pre-requisites](#pre-requisites)
- [Purpose](#purpose)
- [Key Features](#key-features)
- [Getting Started](#getting-started)
- [Software Overview](#software-overview)
- [System Requirement](#system-requirement)
- [Important Ports](#important-ports)
- [Dependencies](#dependencies)
- [How to Setup / Install](#how-to-setup--install)
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

This document provides a Standard Operating Procedure (SOP) for commonly used Linux commands. It enables users to perform basic system tasks such as monitoring system resources, managing files, validating network connectivity, and controlling running services safely and efficiently.

---

## Pre-requisites

| Requirement | Description |
|-------------|-------------|
| Operating System | Linux-based system |
| User Access | Valid login credentials |
| Privileges | Sudo access when required |
| Terminal Access | Command-line interface |
| Basic Knowledge | Familiarity with Linux commands |

---

## Purpose

- Provide consistent command usage  
- Improve operational efficiency  
- Reduce human errors  
- Support troubleshooting activities  

---

## Key Features

| Feature | Description |
|--------|-------------|
| Beginner Friendly | Simple and practical |
| Clear Examples | Commands shown clearly |
| Structured Format | Easy navigation |
| Platform Independent | Works on most Linux systems |
| Operational Ready | Production safe usage |

---

## Getting Started

### License

| License Type | Description | Commercial Use | Open Source |
|--------------|-------------|----------------|-------------|
| GNU GPL | Free and open-source | Yes | Yes |

---

## Software Overview

| Software | Version |
|----------|---------|
| Linux Shell (bash) | Default |

---

## System Requirement

| Requirement | Minimum Recommendation |
|-------------|------------------------|
| Processor | Dual Core |
| RAM | 2 GB or higher |
| Disk Space | 10 GB or higher |
| OS Required | Linux |

---

## Important Ports

| Port | Description |
|------|-------------|
| 22 | SSH remote access |
| 80 | Web services |
| 443 | Secure web services |

---

## Dependencies

### Run-time Dependency

| Dependency | Version | Description |
|------------|---------|-------------|
| Bash | Default | Command execution |
| Coreutils | Default | File and system utilities |

### Other Dependency

| Dependency | Version | Description |
|------------|---------|-------------|
| Curl | Latest | API testing |
| Net-tools | Latest | Network utilities |

---

## How to Setup / Install

Verify user access:
```
whoami
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

| Name | Email | GitHub |
|------|--------|--------|
| Ajitesh | ajitesh@example.com | ajitesh |

---

## References

| Link | Description |
|------|-------------|
| https://linuxcommand.org | Linux documentation |
| https://man7.org/linux/man-pages | Linux manual pages |
| https://ubuntu.com/server/docs | Ubuntu documentation |

---
