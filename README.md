# 📘 SOP – Common Linux Commands Reference

<p align="center">
  <img width="220" height="280" alt="Linux Logo" src="https://www.freepnglogos.com/uploads/linux-png/image-linux-logo-recommended-games-wiki-2.png" />
</p>

---

## Purpose

This document provides a quick reference for frequently used Linux commands.
It helps users perform daily operational tasks such as file handling, system monitoring, networking checks, service management, and troubleshooting in a standardized way.

This SOP is useful for students, system administrators, and DevOps engineers working with Linux environments.

---

## Scope

This SOP applies to:

* Linux servers and virtual machines
* Local development environments
* Cloud instances (AWS, Azure, GCP)
* Ubuntu, Debian, CentOS, RHEL based systems

---

## Prerequisites

| Area         | Requirement                                  |
| ------------ | -------------------------------------------- |
| Access       | Login access to Linux system (SSH / Console) |
| Permissions  | Normal user or sudo access                   |
| Knowledge    | Basic terminal usage                         |
| OS Awareness | Identify Linux distribution                  |
| Network      | Internet connectivity                        |
| Tools        | Core Linux utilities installed               |

---

## Table of Contents

* [System Information & Monitoring](#system-information--monitoring)
* [User & Permission Management](#user--permission-management)
* [File & Directory Management](#file--directory-management)
* [Network Diagnostics](#network-diagnostics)
* [Process & Service Management](#process--service-management)
* [Package Management](#package-management)
* [Logs & Debugging](#logs--debugging)
* [Basic Troubleshooting Workflow](#basic-troubleshooting-workflow)
* [Safety Guidelines](#safety-guidelines)
* [References](#references)

---

## System Information & Monitoring

| Command    | Description               | Example    |
| ---------- | ------------------------- | ---------- |
| `hostname` | Displays system hostname  | `hostname` |
| `uptime`   | Shows system running time | `uptime`   |
| `free -h`  | Memory usage              | `free -h`  |
| `df -h`    | Disk utilization          | `df -h`    |
| `top`      | Live CPU monitoring       | `top`      |
| `vmstat`   | Resource statistics       | `vmstat 1` |
| `lsblk`    | Disk layout               | `lsblk`    |

---

## User & Permission Management

| Command   | Description        | Example                    |
| --------- | ------------------ | -------------------------- |
| `whoami`  | Current user       | `whoami`                   |
| `groups`  | User groups        | `groups`                   |
| `adduser` | Create user        | `sudo adduser devuser`     |
| `chmod`   | Change permissions | `chmod 755 script.sh`      |
| `chown`   | Change ownership   | `chown user:user file.txt` |
| `su -`    | Switch to root     | `su -`                     |

---

## File & Directory Management

| Command    | Description        | Example              |
| ---------- | ------------------ | -------------------- |
| `pwd`      | Current directory  | `pwd`                |
| `ls -lh`   | List files         | `ls -lh`             |
| `mkdir -p` | Create directories | `mkdir -p logs/app`  |
| `touch`    | Create file        | `touch test.txt`     |
| `cp -r`    | Copy directory     | `cp -r src backup/`  |
| `mv`       | Move / rename      | `mv old.txt new.txt` |
| `rm -i`    | Safe delete        | `rm -i file.txt`     |
| `head`     | First lines        | `head file.log`      |
| `tail`     | Last lines         | `                    |
