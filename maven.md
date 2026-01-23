# SOP – pom.xml (Step-by-Step Installation Guide)

Author: Ajitesh Singh  
Created On: 22-01-2026  
Version: 1.0  
Last Updated By: Ajitesh Singh  
Last Edited On: 22-01-2026  

---

## Introduction

This document provides a Standard Operating Procedure (SOP) for configuring and using the pom.xml file in a Maven-based Java project. The pom.xml (Project Object Model) file defines project metadata, dependencies, plugins, build configuration, and version management. This SOP explains how to install Maven, configure pom.xml, validate dependencies, and build the application successfully.

---

## Purpose

The purpose of this SOP is to ensure a standardized and repeatable process for setting up Maven projects using pom.xml. It helps developers avoid dependency conflicts, build failures, and inconsistent environments by following a defined installation and configuration procedure.

---

## Key Features

- Centralized dependency management  
- Automated build lifecycle (compile, test, package)  
- Plugin-based extensibility  
- Version control for libraries  
- Reproducible builds across environments  
- Easy integration with CI/CD pipelines  

---

## Getting Started

### Pre-requisites

| License Type | Description | Commercial Use | Open Source |
|--------------|-------------|----------------|-------------|
| Apache License 2.0 | Maven is free and open-source | Yes | Yes |

---

### Software Overview

| Software | Version |
|----------|---------|
| Apache Maven | 3.8+ |
| Java JDK | 11 or higher |

---

### System Requirement

| Requirement | Minimum Recommendation |
|-------------|------------------------|
| Processor | Dual-Core |
| RAM | 4 GB or higher |
| Disk Space | 10 GB or higher |
| OS Required | Linux / Windows / macOS |

---

### Important Ports

| Port | Description |
|------|-------------|
| 22 | SSH access (if working on remote server) |
| 8080 | Application runtime port (example) |

---

### Dependencies

#### Run-time Dependency

| Run-time Dependency | Version | Description |
|---------------------|---------|-------------|
| Java JDK | 11+ | Required to compile and run Java applications |
| Maven | 3.8+ | Build automation and dependency manager |

#### Other Dependency

| Other Dependency | Version | Description |
|------------------|---------|-------------|
| Git | Latest | Source code management |
| Internet Access | — | Required to download dependencies |

---

## How to Setup / Install (pom.xml)

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

Verify:

```bash
mvn -version
```

---

#### Step 3 – Access Project Directory

Navigate to project directory:

```bash
cd salary-api
```

Confirm pom.xml exists:

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

- groupId, artifactId, version  
- Java compatibility  
- Dependencies  
- Build plugins  

---

#### Step 5 – Download Dependencies and Build

Run:

```bash
mvn clean install
```

This will:

- Download required dependencies  
- Compile source code  
- Run tests  
- Generate build artifacts  

---

#### Step 6 – Validate Build Output

Check generated files:

```bash
ls target/
```

Verify JAR file exists.

---

## Configuration

Update the following sections in pom.xml based on project needs:

- `<properties>` → Java version  
- `<dependencies>` → Add/remove libraries  
- `<build><plugins>` → Compiler and packaging plugins  
- `<repositories>` → Custom artifact repositories  

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

```text
~/.m2/repository/
target/surefire-reports/
```

---

## Disaster Recovery

- Maintain source code in Git repository.  
- Backup .m2 repository if required.  
- Store build artifacts in artifact repository (Nexus / Artifactory).  
- Maintain build scripts and documentation backups.  

---

## High Availability

- Use multiple CI runners.  
- Cache Maven dependencies.  
- Maintain mirrored artifact repositories.  
- Automate builds using Jenkins or GitHub Actions.  

---

## Troubleshooting

| Issue | Possible Cause | Solution |
|-------|----------------|----------|
| Dependency download failed | Network or proxy issue | Verify internet access |
| Build failure | Dependency conflict | Review pom.xml versions |
| Java version error | Incorrect JAVA_HOME | Set correct Java path |
| Plugin error | Plugin incompatibility | Upgrade plugin |

---

## FAQs

Is Maven free?  
Yes, it is open-source under Apache License 2.0.

Can this be used for any Java project?  
Yes, for all Maven-based projects.

Does pom.xml manage runtime behavior?  
Primarily build and dependency management.

---

## Contact Information

| Name | Email |
|------|-------|
| Ajitesh Singh | ajitesh.singh.snaatak@mygurukulam.co |

---

## References

| Link | Description |
|------|-------------|
| https://maven.apache.org | Maven official documentation |
| https://maven.apache.org/pom.html | pom.xml reference |
| https://www.jenkins.io/doc/book/installing/linux/ | CI reference |
