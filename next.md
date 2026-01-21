# Installation via Bash Script

This document explains how to install software using a generic Bash script. The script supports multiple versions, upgrades, installation through package managers, and tarball-based installation. It is designed to provide a flexible and repeatable installation process across Linux environments.

---

## Overview

The Bash installer automates the installation of software by allowing users to:
- Choose the software version to install
- Install using a package manager or tarball
- Upgrade existing installations
- Validate the installation automatically

This approach reduces manual effort and ensures consistent setup across systems.

---

## Supported Features

| Feature | Description |
|--------|-------------|
| Multi-version support | Allows selection of specific versions |
| Upgrade handling | Supports upgrading existing installations |
| Package manager installation | Uses system package managers like apt or yum |
| Tarball installation | Installs directly from compressed archives |
| Validation | Verifies installation after setup |
| Logging | Captures installation output |

---

## Prerequisites

| Requirement | Description |
|-------------|-------------|
| Operating System | Linux-based system |
| Shell | Bash |
| Privileges | sudo access |
| Tools | curl / wget, tar |
| Network | Internet access for downloads |

---

## Directory Structure

```
installer/
├── install.sh
├── config.env
└── logs/
```

---

## Configuration

Configuration values can be stored in a `.env` file or passed as environment variables.

Example:

```bash
SOFTWARE_NAME=python
INSTALL_METHOD=package
VERSION=3.11
```

---

## Installation Using Package Manager

This method installs software using the system package manager.

Example snippet:

```bash
sudo apt update
sudo apt install -y python3
```

Verify installation:

```bash
python3 --version
```

---

## Installation Using Tarball

This method installs software from a compressed archive.

Example snippet:

```bash
VERSION=3.11.1
URL="https://www.python.org/ftp/python/$VERSION/Python-$VERSION.tgz"

wget $URL
tar -xzf Python-$VERSION.tgz
cd Python-$VERSION
./configure
make
sudo make install
```

Verify installation:

```bash
python3 --version
```

---

## Version Selection

Users can dynamically select the version during execution.

Example:

```bash
read -p "Enter version to install: " VERSION
```

---

## Upgrade Support

If the software is already installed, the script can upgrade it.

Package manager upgrade:

```bash
sudo apt upgrade python3 -y
```

Tarball upgrade:

Re-run the installer with a newer version.

---

## Validation and Verification

| Validation Step | Command |
|------------------|----------|
| Check version | `python3 --version` |
| Verify binary path | `which python3` |
| Validate installation | `python3 -c "print('OK')"` |

---

## Logging

Installation logs can be captured for troubleshooting.

Example:

```bash
./install.sh | tee logs/install.log
```

---

## Error Handling

The script validates:
- Network connectivity
- Required tools availability
- Installation success
- Version compatibility

If a failure occurs, the script exits with an error message.

---

## Contact

| Name | Email | GitHub |
|------|-------|--------|
| Ajitesh Singh | ajitesh.singh.snaatak@mygurukulam.co | ajitesh0007 |

---

## References

- https://www.gnu.org/software/bash/
- https://www.python.org/downloads/
- https://ubuntu.com/server/docs

---
