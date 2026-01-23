# Installation Guide – Java (Step-by-Step Installation Guide)

| **Author**    | **Created On** | **Version** | **Last Updated By** | **Reviewer L0** | **Reviewer L1** | **Reviewer L2** |
| ------------- | -------------- | ----------- | ------------------- | --------------- | --------------- | --------------- |
| Ajitesh Singh | 21-01-2026     | v1          | Ajitesh Singh       | Komal Jaiswal   | Akshit Kapil    | Mahesh          |

---

## 📌 Table of Contents

1. Introduction
2. Purpose
3. Key Features
4. Getting Started
5. Software Overview
6. System Requirements
7. Important Ports
8. Dependencies
9. Installation (Java)
10. Configuration
11. Maintenance
12. Monitoring
13. Disaster Recovery
14. High Availability
15. Troubleshooting
16. FAQs
17. Contact Information
18. References

---

## Introduction

This document provides a step-by-step installation guide for **Java (OpenJDK)** on Linux systems. It explains how to install Java, verify the installation, configure environment variables, and validate that Java is running correctly. This guide follows a standard documentation template for consistency and clarity.

---

## Purpose

The purpose of this document is to ensure a standardized and repeatable process for installing Java across environments. It helps users avoid configuration errors, version mismatches, and environment inconsistencies while setting up Java for development or production usage.

---

## Key Features

* Platform independent (Write once, run anywhere)
* Secure and stable Java Virtual Machine (JVM)
* Strong memory management and performance optimization
* Large ecosystem of libraries and frameworks
* Supports enterprise and cloud-native applications
* Easy integration with DevOps and CI/CD pipelines

---

## Getting Started

### Pre-requisites

| License Type          | Description                                | Commercial Use | Open Source |
| --------------------- | ------------------------------------------ | -------------- | ----------- |
| GPL / OpenJDK License | Java is free and open-source under OpenJDK | Yes            | Yes         |

---

## Software Overview

| Software       | Version                   |
| -------------- | ------------------------- |
| Java (OpenJDK) | 11 / 17 (LTS Recommended) |

---

## System Requirements

| Requirement | Minimum Recommendation               |
| ----------- | ------------------------------------ |
| Processor   | Dual-Core                            |
| RAM         | 4 GB or higher                       |
| Disk Space  | 10 GB or higher                      |
| OS Required | Linux (Ubuntu / Amazon Linux / RHEL) |

---

## Important Ports

| Port | Description                              |
| ---- | ---------------------------------------- |
| 22   | SSH access (if working on remote server) |
| 8080 | Java application runtime port (example)  |
| 8443 | Secure application port (HTTPS)          |

---

## Dependencies

### Run-time Dependency

| Run-time Dependency | Version | Description                                   |
| ------------------- | ------- | --------------------------------------------- |
| Java JDK            | 11 / 17 | Required to compile and run Java applications |

### Other Dependency

| Other Dependency | Version | Description       |
| ---------------- | ------- | ----------------- |
| curl / wget      | Latest  | Download packages |
| unzip            | Latest  | Extract archives  |

---

## Installation – Java

### Step-by-Step Installation Guide

#### Step 1 – Update System Packages

```bash
sudo apt update
```

---

#### Step 2 – Install Java

```bash
sudo apt install openjdk-17-jdk -y
```

---

#### Step 3 – Verify Installation

```bash
java -version
```

---

#### Step 4 – Configure JAVA_HOME (Optional but Recommended)

Edit environment file:

```bash
sudo nano /etc/environment
```

Add:

```
JAVA_HOME="/usr/lib/jvm/java-17-openjdk-amd64"
```

Reload configuration:

```bash
source /etc/environment
echo $JAVA_HOME
```

---

#### Step 5 – Test Java Execution

```bash
javac -version
```

---

## Configuration

Configuration includes setting environment variables such as `JAVA_HOME`, updating PATH, and defining JVM options based on application needs.

Example:

```bash
export JAVA_OPTS="-Xms512m -Xmx1024m"
```

---

## Maintenance

Common maintenance commands:

```bash
sudo apt update
sudo apt upgrade openjdk-17-jdk
java -version
```

---

## Monitoring

Check if Java process is running:

```bash
ps -ef | grep java
```

Check listening ports:

```bash
netstat -tulnp | grep java
```

Log locations (application dependent):

```
/var/log/<application-name>/
```

---

## Disaster Recovery

* Maintain backups of configuration files.
* Keep installation scripts documented.
* Maintain VM snapshots or AMIs.
* Use Infrastructure as Code for quick recovery.

---

## High Availability

* Deploy Java applications across multiple servers.
* Use Load Balancers for traffic distribution.
* Implement Auto Scaling or Kubernetes.
* Monitor application health continuously.

---

## Troubleshooting

| Issue                    | Possible Cause                           | Solution                      |
| ------------------------ | ---------------------------------------- | ----------------------------- |
| java command not found   | Java not installed or PATH misconfigured | Reinstall Java / Verify PATH  |
| Wrong Java version       | Multiple Java versions installed         | Configure update-alternatives |
| Permission denied        | Insufficient privileges                  | Use sudo                      |
| Application not starting | Port conflict or config error            | Check logs and ports          |

---

## FAQs

**Is Java free?**
Yes, OpenJDK is open-source and free to use.

**Can Java run on all cloud platforms?**
Yes, Java works on AWS, Azure, GCP, and on-prem environments.

**Which Java version should I use?**
Java 17 LTS is recommended for production.

---

## Contact Information

| Name          | Email                                                                               |
| ------------- | ----------------------------------------------------------------------------------- |
| Ajitesh Singh | [ajitesh.singh.snaatak@mygurukulam.co](mailto:ajitesh.singh.snaatak@mygurukulam.co) |

---

## References

| Link                                                                                                                                                                                                                                                                                                                                                                                                        | Description                    |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------ |
| [https://openjdk.org](https://openjdk.org)                                                                                                                                                                                                                                                                                                                                                                  | OpenJDK official documentation |
| [https://docs.oracle.com/javase/](https://docs.oracle.com/javase/)                                                                                                                                                                                                                                                                                                                                          | Oracle Java Documentation      |
| [https://www.jenkins.io/doc/book/installing/linux/](https://www.jenkins.io/doc/book/installing/linux/)                                                                                                                                                                                                                                                                                                      | CI reference                   |
| This document provides a Standard Operating Procedure (SOP) for configuring and using the `pom.xml` file in a Maven-based Java project. The `pom.xml` (Project Object Model) file defines project metadata, dependencies, plugins, build configuration, and version management. This SOP explains how to install Maven, configure `pom.xml`, validate dependencies, and build the application successfully. |                                |

---

## Purpose

The purpose of this SOP is to ensure a standardized and repeatable process for setting up Maven projects using `pom.xml`. It helps developers avoid dependency conflicts, build failures, and inconsistent environments by following a defined installation and configuration procedure.

---

## Key Features

* Centralized dependency management
* Automated build lifecycle (compile, test, package)
* Plugin-based extensibility
* Version control for libraries
* Reproducible builds across environments
* Easy integration with CI/CD pipelines

---

## Getting Started

### Pre-requisites

| License Type       | Description                   | Commercial Use | Open Source |
| ------------------ | ----------------------------- | -------------- | ----------- |
| Apache License 2.0 | Maven is free and open-source | Yes            | Yes         |

---

## Software Overview

| Software     | Version      |
| ------------ | ------------ |
| Apache Maven | 3.8+         |
| Java JDK     | 11 or higher |

---

## System Requirements

| Requirement | Minimum Recommendation  |
| ----------- | ----------------------- |
| Processor   | Dual-Core               |
| RAM         | 4 GB or higher          |
| Disk Space  | 10 GB or higher         |
| OS Required | Linux / Windows / macOS |

---

## Important Ports

| Port | Description                              |
| ---- | ---------------------------------------- |
| 22   | SSH access (if working on remote server) |
| 8080 | Application runtime port (example)       |

---

## Dependencies

### Run-time Dependency

| Run-time Dependency | Version | Description                                   |
| ------------------- | ------- | --------------------------------------------- |
| Java JDK            | 11+     | Required to compile and run Java applications |
| Maven               | 3.8+    | Build automation and dependency manager       |

### Other Dependency

| Other Dependency | Version | Description                       |
| ---------------- | ------- | --------------------------------- |
| Git              | Latest  | Source code management            |
| Internet Access  | —       | Required to download dependencies |

---

## Installation – pom.xml

### Step-by-Step Installation Guide

#### Step 1 – Install Java

Verify Java installation:

```bash
java -version
```

If not installed:

```bash
sudo apt update
sudo apt install openjdk-11-jdk -y
```

---

#### Step 2 – Install Maven

Install Maven:

```bash
sudo apt install maven -y
```

Verify installation:

```bash
mvn -version
```

---

#### Step 3 – Access Project Directory

Navigate to project directory:

```bash
cd salary-api
```

Confirm `pom.xml` exists:

```bash
ls pom.xml
```

---

#### Step 4 – Review pom.xml

Open file:

```bash
vi pom.xml
```

Verify:

* `groupId`, `artifactId`, `version`
* Java compatibility
* Dependencies
* Build plugins

---

#### Step 5 – Download Dependencies and Build

Run:

```bash
mvn clean install
```

This will:

* Download required dependencies
* Compile source code
* Run tests
* Generate build artifacts

---

#### Step 6 – Validate Build Output

Check generated files:

```bash
ls target/
```

Verify JAR file exists.

---

## Configuration

Update the following sections in `pom.xml` based on project needs:

* `<properties>` → Java version
* `<dependencies>` → Add or remove libraries
* `<build><plugins>` → Compiler and packaging plugins
* `<repositories>` → Custom artifact repositories

Example:

```xml
<properties>
    <java.version>11</java.version>
</properties>
```

---

## Maintenance

Common maintenance commands:

```bash
mvn clean
mvn versions:display-dependency-updates
mvn clean package
mvn test
```

---

## Monitoring

Validate project build and execution:

```bash
mvn validate
mvn test
```

Log locations:

```
~/.m2/repository/
target/surefire-reports/
```

---

## Disaster Recovery

* Maintain source code in Git repository.
* Backup `.m2` repository if required.
* Store build artifacts in artifact repository (Nexus / Artifactory).
* Maintain build scripts and documentation backups.

---

## High Availability

* Use multiple CI runners.
* Cache Maven dependencies.
* Maintain mirrored artifact repositories.
* Automate builds using Jenkins or GitHub Actions.

---

## Troubleshooting

| Issue                      | Possible Cause         | Solution                  |
| -------------------------- | ---------------------- | ------------------------- |
| Dependency download failed | Network or proxy issue | Verify internet access    |
| Build failure              | Dependency conflict    | Review `pom.xml` versions |
| Java version error         | Incorrect JAVA_HOME    | Set correct Java path     |
| Plugin error               | Plugin incompatibility | Upgrade plugin            |

---

## FAQs

**Is Maven free?**
Yes, it is open-source under Apache License 2.0.

**Can this be used for any Java project?**
Yes, for all Maven-based projects.

**Does pom.xml manage runtime behavior?**
Primarily build and dependency management.

---

## Contact Information

| Name          | Email                                                                               |
| ------------- | ----------------------------------------------------------------------------------- |
| Ajitesh Singh | [ajitesh.singh.snaatak@mygurukulam.co](mailto:ajitesh.singh.snaatak@mygurukulam.co) |

---

## References

| Link                                                                                                   | Description                  |
| ------------------------------------------------------------------------------------------------------ | ---------------------------- |
| [https://maven.apache.org](https://maven.apache.org)                                                   | Maven official documentation |
| [https://maven.apache.org/pom.html](https://maven.apache.org/pom.html)                                 | pom.xml reference            |
| [https://www.jenkins.io/doc/book/installing/linux/](https://www.jenkins.io/doc/book/installing/linux/) | CI reference                 |
