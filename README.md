# SOP for Common Linux Commands

<p align="center">
  <img width="200" height="300" alt="Linux Logo" src="https://www.freepnglogos.com/uploads/linux-png/image-linux-logo-recommended-games-wiki-2.png" />
</p>

---

## Table of Contents

* [Introduction](#introduction)
* [Prerequisites](#prerequisites)
* [Common Commands](#common-commands)

  * [System Information & Monitoring](#a-system-information--monitoring)
  * [User & Permissions Management](#b-user--permissions-management)
  * [File & Directory Operations](#c-file--directory-operations)
  * [Network & Connectivity](#d-network--connectivity)
  * [Process & Service Management](#e-process--service-management)
  * [Package & System Updates](#f-package--system-updates)
  * [Logs & Debugging](#g-logs--debugging)
  * [Troubleshooting Commands](#h-troubleshooting-commands)
* [References](#references)

---

## Introduction

The purpose of this SOP is to provide a centralized reference of commonly used Linux commands that help users perform daily operational activities such as system monitoring, file management, networking checks, service handling, and troubleshooting.

This document helps standardize operational practices, reduce manual errors, and improve productivity while working on Linux-based servers and virtual machines.

---

## Prerequisites

Before executing any commands, ensure the following:

| Category             | Prerequisites / Requirements               |
| -------------------- | ------------------------------------------ |
| System Access        | Access to a Linux system (local or remote) |
| User Permissions     | Normal user or sudo privileges             |
| Linux Distribution   | Awareness of OS type and package manager   |
| Network Connectivity | Internet or LAN connectivity if required   |
| Command Availability | Core utilities installed                   |
| Environment Setup    | Shell access (bash / zsh)                  |

---

## Common Commands

### A. System Information & Monitoring

| Command        | Description                                 |
| :------------- | :------------------------------------------ |
| `hostname`     | Displays system hostname.                   |
| `uptime`       | Shows system running time and load average. |
| `whoami`       | Displays current logged-in user.            |
| `date`         | Displays system date and time.              |
| `top` / `htop` | Displays running processes and CPU usage.   |
| `free -h`      | Displays memory usage.                      |
| `df -h`        | Displays disk usage in readable format.     |
| `lsblk`        | Shows disk partitions.                      |
| `ps aux`       | Lists all running processes.                |

---

### B. User & Permissions Management

| Command                       | Description                 |
| :---------------------------- | :-------------------------- |
| `who`                         | Displays logged-in users.   |
| `id <username>`               | Shows user ID and groups.   |
| `groups`                      | Displays group memberships. |
| `sudo su -`                   | Switches to root user.      |
| `adduser <username>`          | Creates a new user.         |
| `chmod <mode> <file>`         | Changes file permissions.   |
| `chown <user>:<group> <file>` | Changes file ownership.     |
| `passwd <username>`           | Resets user password.       |

---

### C. File & Directory Operations

| Command                   | Description                            |
| :------------------------ | :------------------------------------- |
| `pwd`                     | Displays current directory path.       |
| `ls -lh`                  | Lists files with size and permissions. |
| `cd <path>`               | Changes directory.                     |
| `mkdir -p <dir>`          | Creates nested directories.            |
| `touch <file>`            | Creates empty file.                    |
| `cp -r <src> <dest>`      | Copies directories recursively.        |
| `mv <src> <dest>`         | Moves or renames files.                |
| `rm -i <file>`            | Deletes file with confirmation.        |
| `cat <file>`              | Displays file contents.                |
| `head <file>`             | Displays first lines of file.          |
| `tail -f <file>`          | Monitors file in real time.            |
| `find / -name <filename>` | Searches for files.                    |

---

### D. Network & Connectivity

| Command                | Description                       |
| :--------------------- | :-------------------------------- |
| `ip a`                 | Displays IP addresses.            |
| `ip route`             | Displays routing table.           |
| `ping <host>`          | Tests network connectivity.       |
| `curl <url>`           | Tests web/API endpoint.           |
| `ss -tunlp`            | Shows listening ports.            |
| `netstat -tulnp`       | Displays open ports and services. |
| `nc -zv <host> <port>` | Tests port connectivity.          |
| `nslookup <domain>`    | DNS lookup.                       |
| `traceroute <host>`    | Traces network route.             |

---

### E. Process & Service Management

| Command                       | Description                 |
| :---------------------------- | :-------------------------- |
| `ps -ef`                      | Displays running processes. |
| `grep <process>`              | Filters process output.     |
| `kill -9 <pid>`               | Force stops a process.      |
| `pkill -f <name>`             | Kills process by name.      |
| `systemctl status <service>`  | Checks service status.      |
| `systemctl start <service>`   | Starts service.             |
| `systemctl restart <service>` | Restarts service.           |
| `systemctl stop <service>`    | Stops service.              |
| `journalctl -u <service> -f`  | Follows live logs.          |

---

### F. Package & System Updates

| Command                  | Description                  |                           |
| :----------------------- | :--------------------------- | ------------------------- |
| `sudo apt update`        | Updates package list.        |                           |
| `sudo apt upgrade -y`    | Upgrades installed packages. |                           |
| `sudo apt install <pkg>` | Installs a package.          |                           |
| `sudo apt remove <pkg>`  | Removes a package.           |                           |
| `dpkg -l                 | grep <pkg>`                  | Checks installed package. |
| `which <command>`        | Shows command location.      |                           |

---

### G. Logs & Debugging

| Command                   | Description                  |                  |
| :------------------------ | :--------------------------- | ---------------- |
| `less /var/log/syslog`    | Views system logs.           |                  |
| `tail -f /var/log/syslog` | Monitors live logs.          |                  |
| `grep "error" <file>`     | Searches error messages.     |                  |
| `journalctl -xe`          | Displays recent system logs. |                  |
| `dmesg                    | tail`                        | Kernel messages. |
| `wc -l <file>`            | Counts number of lines.      |                  |

---

### H. Troubleshooting Commands

| Command                      | Use Case                      |
| :--------------------------- | :---------------------------- |
| `uptime`                     | Check system load and uptime. |
| `free -h`                    | Check memory usage.           |
| `df -h`                      | Check disk availability.      |
| `systemctl status <service>` | Verify service health.        |
| `journalctl -u <service>`    | Inspect service logs.         |
| `ss -tunlp`                  | Check port conflicts.         |
| `ping <host>`                | Validate connectivity.        |
| `sudo reboot`                | Reboot system if required.    |

---

## References

| Link                                                                               | Description                 |
| :--------------------------------------------------------------------------------- | :-------------------------- |
| [https://linuxcommand.org](https://linuxcommand.org)                               | Linux command documentation |
| [https://ubuntu.com/server/docs](https://ubuntu.com/server/docs)                   | Ubuntu Server Docs          |
| [https://access.redhat.com/documentation](https://access.redhat.com/documentation) | RedHat Documentation        |
| [https://man7.org/linux/man-pages](https://man7.org/linux/man-pages)               | Linux Man Pages             |

---
