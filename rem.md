# Java Installation Guide

This guide explains how to install Java (OpenJDK) step by step on a Linux system (Ubuntu / Debian based).

---

## Prerequisites

* A Linux machine (Ubuntu / Debian)
* Internet connectivity
* User with sudo privileges
* Terminal access

---

## Step 1: Check If Java Is Already Installed

Open the terminal and run:

```
java -version
```

If Java is already installed, the version will be displayed.
If not installed, a command not found message will appear.

---

## Step 2: Update Package Repository

Update the system package list:

```
sudo apt update
```

---

## Step 3: Install Java

Choose the Java version you want to install.

Install OpenJDK 8

```
sudo apt install -y openjdk-8-jdk
```

Install OpenJDK 11

```
sudo apt install -y openjdk-11-jdk
```

Install OpenJDK 17 (Recommended)

```
sudo apt install -y openjdk-17-jdk
```

---

## Step 4: Verify Installation

Confirm Java installation:

```
java -version
```

---

## Step 5: Set Default Java Version (Optional)

If multiple versions are installed:

```
sudo update-alternatives --config java
```

Select the required version from the list.

---

## Step 6: Set JAVA_HOME (Optional)

Find Java path:

```
readlink -f $(which java)
```

Edit profile file:

```
nano ~/.bashrc
```

Add the following lines:

```
export JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64
export PATH=$PATH:$JAVA_HOME/bin
```

Apply changes:

```
source ~/.bashrc
```

Verify:

```
echo $JAVA_HOME
```

---

## Installation Complete

Java is now installed and ready for use.

---

## References

* [https://openjdk.org](https://openjdk.org)
* [https://ubuntu.com/server/docs/java](https://ubuntu.com/server/docs/java)

---
