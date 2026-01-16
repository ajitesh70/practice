# SOP for Software Management


---

## Table of Contents
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)

- <details>
  
    <summary><a href="#procedure">Procedure</b></a></summary>
    
    - [Installing Software](#installing-software)
    - [Updating Software](#updating-software)
    - [Removing Software](#removing-software)
    - [Verifying Software Information](#verifying-software-information)
  </details>
  
- [Best Practices](#best-practices)
- [Troubleshooting Tips](#troubleshooting-tips)
- [Contact Information](#contact-information)
- [References](#references)

---

## Introduction
This Standard Operating Procedure (SOP) provides a structured method for managing software on Ubuntu systems using the APT (Advanced Package Tool) package manager.
It ensures consistent, secure, and efficient software installation, updating, and removal processes for both beginners and system administrators.

## Prerequisites
Before performing software management tasks:
  - Ensure you have sudo privileges.
  - Confirm an active internet connection.
  - Update repository information:

        sudo apt update 
<img width="1150" height="481" alt="apt update" src="https://github.com/user-attachments/assets/6cfa839d-cd01-45fd-967c-98836009aad8" />

## Procedure
  ### Installing Software
  Install new software using:
            
    sudo apt install <package-name>
   ### Example:
    sudo apt install tree
   <img width="1240" height="589" alt="apt install tree" src="https://github.com/user-attachments/assets/75b6313f-4824-4114-a921-c5fa279bd8ba" />

### Common Flags:
    -y → Automatically confirms installation.
    -q → Quiet mode (Suppresses unnecessary output. Great for clean logs or scripts.)
    --no-install-recommends → Installs only essential components.
    --reinstall → Reinstall an existing package (Reinstalls the specified package, useful if a program is corrupted.)
   ### Example with flags:
    sudo apt install -y --no-install-recommends vim
    sudo apt install -y -q curl (Installs curl quietly (minimal output).)
<img width="1302" height="586" alt="with flag -y -q curl" src="https://github.com/user-attachments/assets/8e826270-fb6c-4167-93aa-708b671e65ea" />
      
    sudo apt install --reinstall htop (Forces a clean reinstallation of htop.)
 <img width="1202" height="540" alt="reinstall flag" src="https://github.com/user-attachments/assets/a85bd871-a3a0-44fa-80af-5e7ebee8676e" />

 ### Updating Software
  Keep your system and applications up to date:
        
    sudo apt update (refreshes the list of available packages.)
    sudo apt upgrade (installs the newest versions of all installed packages.)
 <img width="1813" height="643" alt="apt upgrade" src="https://github.com/user-attachments/assets/0aeee596-3c2f-433a-ab4c-a0d755bbe73d" />

 ### For a full upgrade (handles dependencies):
    sudo apt full-upgrade
  ### Clean up unnecessary files:
    sudo apt autoremove (Removes unused dependencies)
    sudo apt clean (Deletes cached .deb files (Frees disk space))
<img width="818" height="180" alt="image" src="https://github.com/user-attachments/assets/9f1bfac2-c288-4e73-97e3-a2aecb6445de" />

  ### Removing Software
  To remove software packages:
    Remove the package (keep configurations):
           
    sudo apt remove tree
  <img width="1031" height="293" alt="remove tree" src="https://github.com/user-attachments/assets/833f2f40-ffe6-4ed7-8338-c4f3e7045ec8" />

Remove package with configurations:
     
    sudo apt purge <package-name>
<img width="1003" height="263" alt="purge" src="https://github.com/user-attachments/assets/4aafc0fa-6c6a-4e0c-a2da-2e3345d8d09f" />

  Remove unused dependencies:
     
    sudo apt autoremove
  
  ### Verifying Software Information
  Check installed packages and details:
    List installed package:
     
    dpkg -l | grep <package-name> (To check whether a package is installed)
<img width="1403" height="46" alt="grep tree" src="https://github.com/user-attachments/assets/8b0f2e82-4e62-46e6-9034-226c16c4ecbd" />

  Show package details:
    
    apt show <package-name> (To display detailed information about the package)
 <img width="1399" height="447" alt="apt show package" src="https://github.com/user-attachments/assets/3c6d2e35-f51c-43bd-b4d4-a46f2ae8c85f" />

 Search available packages:
  
    apt search <keyword>
## Best Practices
- Always run sudo apt update before installations or upgrades.
- Review changes before confirming (Y).
- Avoid mixing package managers (apt, snap, flatpak).
- Regularly run sudo apt upgrade to maintain system security.
- Use sudo apt autoremove to clean up unused packages.

## Troubleshooting Tips
| **Issue**           | **Solution**                                |
| ------------------- | ------------------------------------------- |
| Package not found   | Run `sudo apt update`                       |
| Broken dependencies | Run `sudo apt --fix-broken install`         |
| Low disk space      | Run `sudo apt clean && sudo apt autoremove` |
| Check system space  | Run `df -h`                                 |



---

## References

| Topic                         | Link                                                            | Description                                                |
|-------------------------------|-----------------------------------------------------------------|------------------------------------------------------------|
| APT Manual Page               | https://manpages.ubuntu.com/manpages/jammy/en/man8/apt.8.html   | Ref for command syntax and operational details of APT.     |
| APT Package Manager Overview  | https://phoenixnap.com/kb/apt-package-manager                   | Comprehensive guide explaining the functions and operations of the APT package manager
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
