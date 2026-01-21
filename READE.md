# SOP: Common Linux Commands

| Author | Created On | Version | Last Updated By | Internal Reviewer | Reviewer L0 | Reviewer L1 | Reviewer L2 |
|--------|------------|---------|------------------|-------------------|-------------|-------------|-------------|
| Ajitesh Singh | 21-01-2026 | v1 | Ajitesh Singh | Neha, Anirudh, Rahul | Komal Jaiswal | Akshit Kapil | Mahesh |

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

This document provides a Standard Operating Procedure (SOP) for frequently used Linux commands. It helps users perform basic system tasks such as monitoring system health, managing files, validating network connectivity, and controlling running processes.

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
| Easy to Read | Tabular format |
| Real Examples | Practical usage |
| Logical Grouping | Categorized sections |
| Beginner Friendly | Simple language |
| Operational Ready | Production safe |

---

## Environment Verification

| Command | Description | Example |
|--------|-------------|---------|
| `whoami` | Displays current user | `whoami` |
| `echo $SHELL` | Shows active shell | `/bin/bash` |
| `ls --version` | Verifies command availability | `ls (GNU coreutils) 9.1` |

---

## Command Reference

### System Monitoring

| Command | Description | Example |
|--------|-------------|---------|
| `uptime` | Shows system running time | `uptime → 2:10 up 3 days, load average: 0.05` |
| `free -h` | Displays memory usage | `free -h → Mem: 7.7Gi used` |
| `df -h` | Shows disk utilization | `df -h → /dev/sda1 40% used` |
| `top` | Displays live processes | `top → PID 1203 nginx using CPU` |
| `hostname` | Shows system name | `hostname → web-server-01` |

---

### File Operations

| Command | Description | Example |
|--------|-------------|---------|
| `pwd` | Displays current directory | `/home/ubuntu/projects` |
| `ls -lh` | Lists files in detail | `config.yml 2K README.md 5K` |
| `mkdir <dir>` | Creates directory | `mkdir logs` |
| `touch <file>` | Creates empty file | `touch notes.txt` |
| `cp <src> <dest>` | Copies file | `cp report.txt backup.txt` |
| `mv <src> <dest>` | Renames/moves file | `mv old.log new.log` |
| `rm <file>` | Deletes file | `rm temp.txt` |
| `cat <file>` | Displays file content | `cat notes.txt → Hello World` |

---

### User & Permission Commands

| Command | Description | Example |
|--------|-------------|---------|
| `whoami` | Shows logged-in user | `ubuntu` |
| `id <user>` | Displays user identity | `id ubuntu → uid=1000` |
| `groups` | Shows user groups | `groups → sudo docker` |
| `chmod <mode> <file>` | Changes permissions | `chmod 755 app.sh` |
| `chown <user>:<grp> <file>` | Changes ownership | `chown root:root config.conf` |
| `passwd <user>` | Changes password | `passwd devuser` |

---

### Network Commands

| Command | Description | Example |
|--------|-------------|---------|
| `ip a` | Displays IP addresses | `eth0 → 192.168.1.10` |
| `ping <host>` | Tests connectivity | `ping google.com → time=20ms` |
| `curl <url>` | Tests HTTP endpoint | `curl http://localhost:8080/health` |
| `ss -tunlp` | Shows listening ports | `LISTEN 0.0.0.0:22` |
| `hostname -I` | Shows system IP | `192.168.1.10` |

---

### Process & Service Commands

| Command | Description | Example |
|--------|-------------|---------|
| `ps aux` | Lists running processes | `nginx PID 1234 running` |
| `kill <pid>` | Terminates process | `kill 1234` |
| `systemctl status <svc>` | Shows service status | `systemctl status nginx → active` |
| `systemctl restart <svc>` | Restarts service | `systemctl restart nginx` |
| `journalctl -xe` | Displays system logs | `error: service failed` |

---

## Contact

| Name | Email Address | GitHub | URL |
|------|---------------|--------|-----|
| Ajitesh Singh | ajitesh.singh.snaatak@mygurukulam.co | ajitesh0007 | https://github.com/ajitesh0007 |

---

## References

| Link | Description |
|------|-------------|
| [https://linuxcommand.org](https://linuxcommand.org/lc3_man_page_index.php) | Linux command documentation |
| [https://man7.org/linux/man-pages](https://linux.die.net/man/) | Linux manual pages |

---
