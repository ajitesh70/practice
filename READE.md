# SOP: Common Linux Commands

| Author | Created On | Version | Last Updated By | Internal Reviewer | Reviewer L0 | Reviewer L1 | Reviewer L2 |
|--------|------------|---------|------------------|-------------------|-------------|-------------|-------------|
| Ajitesh Singh | 21-01-2026 | v1.2 | Ajitesh Singh | NA | NA | NA | NA |

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
| Real Examples | Practical commands |
| Logical Grouping | Categorized sections |
| Beginner Friendly | Simple language |
| Operational Ready | Production safe |

---

## Environment Verification

No installation is required. Most Linux distributions include the required tools.

| Command | Purpose | Example |
|--------|---------|---------|
| `whoami` | Verify current user | `whoami` |
| `echo $SHELL` | Check active shell | `echo $SHELL` |
| `ls --version` | Verify command availability | `ls --version` |

---

## Command Reference

### System Monitoring

| Command | Description | Example |
|--------|-------------|---------|
| `uptime` | Shows system running time | `uptime` |
| `free -h` | Displays memory usage | `free -h` |
| `df -h` | Shows disk usage | `df -h` |
| `top` | Displays running processes | `top` |
| `hostname` | Shows system name | `hostname` |

---

### File Operations

| Command | Description | Example |
|--------|-------------|---------|
| `pwd` | Shows current directory | `pwd` |
| `ls -lh` | Lists files with details | `ls -lh` |
| `mkdir demo` | Creates directory | `mkdir demo` |
| `touch demo.txt` | Creates file | `touch demo.txt` |
| `cp demo.txt backup.txt` | Copies file | `cp demo.txt backup.txt` |
| `mv backup.txt archive.txt` | Renames file | `mv backup.txt archive.txt` |
| `rm archive.txt` | Deletes file | `rm archive.txt` |
| `cat demo.txt` | Displays file content | `cat demo.txt` |

---

### User & Permission Commands

| Command | Description | Example |
|--------|-------------|---------|
| `whoami` | Displays logged-in user | `whoami` |
| `id` | Shows user identity | `id` |
| `groups` | Displays user groups | `groups` |
| `chmod 755 script.sh` | Changes permissions | `chmod 755 script.sh` |
| `chown user:user file.txt` | Changes ownership | `chown user:user file.txt` |
| `passwd user1` | Changes password | `passwd user1` |

---

### Network Commands

| Command | Description | Example |
|--------|-------------|---------|
| `ip a` | Shows IP addresses | `ip a` |
| `ping google.com` | Tests connectivity | `ping google.com` |
| `curl http://localhost` | Tests URL/API | `curl http://localhost` |
| `ss -tunlp` | Shows listening ports | `ss -tunlp` |
| `hostname -I` | Displays system IP | `hostname -I` |

---

### Process & Service Commands

| Command | Description | Example |
|--------|-------------|---------|
| `ps aux` | Lists running processes | `ps aux` |
| `kill <pid>` | Terminates process | `kill 1234` |
| `systemctl status ssh` | Checks service status | `systemctl status ssh` |
| `systemctl restart ssh` | Restarts service | `systemctl restart ssh` |
| `journalctl -xe` | Displays system logs | `journalctl -xe` |

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
