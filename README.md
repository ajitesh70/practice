# SOP for Common Linux Commands


<p align="center">
  <img width="200" height="300" alt="Linux Logo" src="https://www.freepnglogos.com/uploads/linux-png/image-linux-logo-recommended-games-wiki-2.png" />
</p>





## Table of Contents

- [Introduction](#Introduction)
- [Prerequisites](#prerequisites)
- [Common Commands](#common-commands)
  - [System Information & Monitoring](#a-system-information--monitoring)
  - [User & Permissions Management](#b-user--permissions-management)
  - [File & Directory Operations](#c-file--directory-operations)
  - [Network & Connectivity](#d-network--connectivity)
  - [Process & Service Management](#e-process--service-management)
  - [Package & System Updates](#f-package--system-updates)
  - [Logs & Debugging](#g-logs--debugging)
  - [Troubleshooting Commands](#h-troubleshooting-commands)
- [References](#references)

---

## Introduction


The purpose of this SOP is to provide a **centralized reference** of essential Linux commands for managing, monitoring, and troubleshooting the **virtual machine (VM)**.
It standardizes DevOps operations and minimizes errors during setup and maintenance.


---

## Prerequisites

Before executing any commands, ensure the following:


| **Category**                | **Prerequisites / Requirements**                                                                       |
| --------------------------- | ------------------------------------------------------------------------------------------------------ |
| **System Access**           | Access to a Linux system (local/remote); valid user credentials; basic terminal knowledge              |
| **User Permissions**        | Normal user for basic commands; `sudo` or root privileges for admin tasks; ensure `sudo` is configured |
| **Linux Distribution**      | Identify distro (Ubuntu, CentOS, RHEL, etc.); know the package manager (`apt`, `yum`, `dnf`, `zypper`) |
| **Network Connectivity**    | Internet or LAN access if needed; verify using `ping` or `curl`                                        |
| **Command Availability**    | Confirm core utilities installed: `ls`, `cat`, `grep`, `awk`, `find`, `tar`, `vi`, etc.                |
| **Environment Setup**       | Ensure correct `$PATH` (`/bin`, `/usr/bin`, `/usr/local/bin`); shell available (`bash`, `zsh`)         |

---
a
## Common Commands

### A. System Information & Monitoring
| Command | Description |
|:--|:--|
| `whoami` | Displays current logged-in user. |
| `date` | Displays system date and time. |
| `top` / `htop` | Displays running processes and usage statistics. |
| `free -m` | Displays memory usage in MB. |
| `df -h` | Displays disk usage in human-readable format. |
| `du -sh <directory>` | Shows total size of a directory. |
| `ps aux` | Lists all running processes. |

---

### B. User & Permissions Management
| Command | Description |
|:--|:--|
| `who` | Displays all currently logged-in users. |
| `id <username>` | Displays UID, GID, and group info of a user. |
| `sudo su -` | Switches to root user. |
| `chmod <mode> <file>` | Changes file permissions. |
| `chown <user>:<group> <file>` | Changes file ownership. |
| `passwd <username>` | Resets user password. |

---

### C. File & Directory Operations
| Command | Description |
|:--|:--|
| `ls -la` | Lists files with permissions and details. |
| `cd <path>` | Changes current working directory. |
| `mkdir <dir>` | Creates a new directory. |
| `cp <src> <dest>` | Copies files or directories. |
| `mv <src> <dest>` | Moves or renames files/directories. |
| `rm -rf <dir>` | Deletes directories recursively (**Use with caution**). |
| `cat <file>` | Displays contents of a file. |
| `nano <file>` / `vim <file>` | Opens a file for editing. |
| `find / -name <filename>` | Searches for files by name. |

---

### D. Network & Connectivity
| Command | Description |
|:--|:--|
| `ip a`                 | Lists network interfaces and IP addresses.           |
| `ping <hostname>`      | Tests connectivity to a remote host.                 |
| `curl -I <url>`        | Fetches HTTP response headers (quick health check).  |
| `netstat -tulnp`       | Lists open ports and listening services.             |
| `ss -tuln`             | Modern replacement for `netstat` to view open ports. |
| `sudo lsof -i :<port>` | Shows which process is using a port.                 |
| `nslookup <domain>`    | Performs a DNS lookup for a domain.                  |
| `dig <domain>`         | Advanced DNS query tool.                             |
| `traceroute <host>`    | Traces packet route to a destination.                |
| `curl <url>`           | Tests API/URL responses.                             |

---

### E. Process & Service Management
| Command | Description |
|:--|:--|
| `systemctl status <service>` | Checks service status. |
| `systemctl start <service>` | Starts a service. |
| `systemctl restart <service>` | Restarts a service. |
| `systemctl stop <service>` | Stops a service. |
| `ps -ef` | Searches for a process. |
| `pkill -f <process>` | Kills processes matching a pattern. |
| `journalctl -u <service> -f` | Follows live service logs. |

---

### F. Package & System Updates
| Command | Description |
|:--|:--|
| `sudo apt update` | Updates package index. |
| `sudo apt upgrade -y` | Installs available updates. |
| `sudo apt install <pkg>` | Installs new package. |
| `sudo apt remove <pkg>` | Removes a package. |
| `dpkg -l \| grep <pkg>`| Checks installed package list. |

---

### G. Logs & Debugging
| Command | Description |
|:--|:--|
| `tail -f /var/log/syslog` | Streams live system logs. |
| `cat /var/log/dmesg` | Displays kernel messages. |
| `less /var/log/<service>.log` | Reads service logs. |
| `grep "error" /var/log/<service>.log` | Searches for errors in logs. |
| `journalctl -xe` | Shows detailed recent system logs. |

---

### H. Troubleshooting Commands
| Command | Use Case |
|:--|:--|
| `sudo systemctl status <service>` | Check if a service is active or failed. |
| `curl http://localhost:8081/health` | Test API health endpoints. |
| `tail -n 50 /var/log/<service>.log` | View last 50 lines of service logs. |
| `df -h` | Check available disk space (common crash cause). |
| `sudo reboot` | Reboot VM if necessary. |

---



---

## References
| Link | Description |
|:--|:--|
| [OT-Microservices GitHub](https://github.com/OT-MICROSERVICES) | Project source repository |
| [Linux Command Reference](https://linuxcommand.org) | Comprehensive Linux command guide |
| [Go Language Docs](https://golang.org/doc/) | Official Go documentation |
| [Python Docs](https://docs.python.org/3/) | Official Python documentation |
| [Java Docs](https://docs.oracle.com/en/java/) | Official Java documentation |

---
