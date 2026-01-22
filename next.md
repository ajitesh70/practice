# Python Installation via Generic Bash Script

This documentation explains how to install Python using a generic Bash script.  
The script supports installing multiple Python versions, upgrading existing installations, and installing Python either from a package manager or from a tarball source.

---

## Overview

The Bash installer provides a standardized way to install Python across Linux systems. Users can select the Python version and installation method during execution. The script automatically validates the installation and ensures consistency across environments.

Supported capabilities:
- Install multiple Python versions
- Upgrade existing Python installation
- Install using package manager (apt/yum)
- Install using tarball (source build)

---

## Prerequisites

| Requirement | Description |
|-------------|-------------|
| Operating System | Linux-based system |
| Shell | Bash |
| Privileges | sudo access |
| Network | Internet access |
| Tools | curl or wget, tar |

---

## Directory Structure

```
python-installer/
├── install.sh
├── config.env
└── logs/
```

---

## Configuration

The installer can accept configuration values from a configuration file or user input.

Example `config.env`:

```bash
PYTHON_VERSION=3.11
INSTALL_METHOD=package
```

Supported values:
- `PYTHON_VERSION` → Desired Python version
- `INSTALL_METHOD` → `package` or `tarball`

---

## Installation Using Package Manager

This method installs Python using the system package manager.

Example:

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

This method installs Python from source.

Example:

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

## Multi-Version Support

The script allows installing multiple Python versions on the same system.

Example:

```bash
python3.8 --version
python3.11 --version
```

Users can switch versions using symbolic links or update-alternatives if configured.

---

## Upgrade Support

The installer supports upgrading Python to a newer version.

Package manager upgrade:

```bash
sudo apt upgrade python3 -y
```

Tarball upgrade:

Re-run the installer with a newer version number.

---

## Validation

After installation, validate the setup:

| Validation | Command |
|------------|----------|
| Check version | `python3 --version` |
| Verify path | `which python3` |
| Test execution | `python3 -c "print('Python OK')"` |

---

## Logging

Installation logs can be captured for troubleshooting.

Example:

```bash
./install.sh | tee logs/install.log
```

---

## Contact

| Name | Email | GitHub |
|------|-------|--------|
| Ajitesh Singh | ajitesh.singh.snaatak@mygurukulam.co | ajitesh0007 |

---

## References

- https://www.python.org/downloads/
- https://docs.python.org/3/
- https://www.gnu.org/software/bash/

---
