# SOP: Software Installation via Bash Script

| Author | Created On | Version | Last Updated By | Internal Reviewer | Reviewer L0 | Reviewer L1 | Reviewer L2 |
|--------|------------|---------|------------------|-------------------|-------------|-------------|-------------|
| Ajitesh Singh | 21-01-2026 | v1.0 | Ajitesh Singh | NA | NA | NA | NA |

---

## Table of Contents

- [Introduction](#introduction)
- [Purpose](#purpose)
- [Pre-requisites](#pre-requisites)
- [Key Features](#key-features)
- [Supported Installation Methods](#supported-installation-methods)
- [Directory Structure](#directory-structure)
- [Installation Using Package Manager](#installation-using-package-manager)
- [Installation Using Tarball](#installation-using-tarball)
- [Version Management and Upgrade](#version-management-and-upgrade)
- [Validation and Verification](#validation-and-verification)
- [Maintenance](#maintenance)
- [Contact](#contact)
- [References](#references)

---

## Introduction

This document describes a standard approach for installing software using a generic Bash script. The script supports multiple software versions, installation via package managers, tarball-based installations, and upgrade automation. It ensures consistent and repeatable installations across environments.

---

## Purpose

- Automate software installation using Bash  
- Support multiple versions and upgrades  
- Enable installation via package manager and tarball  
- Reduce manual configuration errors  
- Improve deployment consistency  

---

## Pre-requisites

| Requirement | Description |
|-------------|-------------|
| Operating System | Linux-based system |
| Shell | Bash shell available |
| Privileges | sudo access |
| Network | Internet access (optional for package installs) |
| Tools | curl, wget, tar |

---

## Key Features

| Feature | Description |
|---------|-------------|
| Multi-Version Support | Install different versions |
| Upgrade Handling | Upgrade existing installations |
| Package Manager | Install via apt/yum |
| Tarball Install | Install from compressed archive |
| Validation | Automatic verification |
| Logging | Installation logs |

---

## Supported Installation Methods

| Method | Description |
|--------|-------------|
| Package Manager | Install via system repositories |
| Tarball | Install from compressed archive |
| Custom Version | User-defined version selection |
| Upgrade Mode | Replace existing version |

---

## Directory Structure

```
installer/
├── install.sh
├── config.env
└── logs/
```

---

## Installation Using Package Manager

### Example Script

```bash
#!/bin/bash
PACKAGE_NAME="python3"

sudo apt update
sudo apt install -y $PACKAGE_NAME

$PACKAGE_NAME --version
```

---

## Installation Using Tarball

### Example Script

```bash
#!/bin/bash
VERSION="3.11.1"
URL="https://www.python.org/ftp/python/$VERSION/Python-$VERSION.tgz"

wget $URL
tar -xzf Python-$VERSION.tgz
cd Python-$VERSION
./configure
make
sudo make install
```

---

## Version Management and Upgrade

### Select Version Dynamically

```bash
read -p "Enter version to install: " VERSION
```

### Upgrade Example

```bash
sudo apt upgrade python3 -y
```

or re-run tarball installer with newer version.

---

## Validation and Verification

| Check | Command |
|-------|---------|
| Verify Installation | `python3 --version` |
| Verify Path | `which python3` |
| Verify Binary | `ls /usr/local/bin/python3` |

---

## Maintenance

| Task | Command |
|------|---------|
| Update Packages | `sudo apt update && sudo apt upgrade` |
| Cleanup Tar Files | `rm -rf Python-*` |
| Logs Review | `cat logs/install.log` |

---

## Contact

| Name | Email Address | GitHub | URL |
|------|---------------|--------|-----|
| Ajitesh Singh | ajitesh.singh.snaatak@mygurukulam.co | ajitesh0007 | https://github.com/ajitesh0007 |

---

## References

| Link | Description |
|------|-------------|
| https://www.gnu.org/software/bash/ | Bash Documentation |
| https://www.python.org/downloads/source/ | Python Tarball Downloads |
| https://ubuntu.com/server/docs | Ubuntu Documentation |

---
