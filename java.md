# Installation Guide – Step by Step Installation Guide for Java

| Author | Created On | Version | Last Updated By | Reviewer L0 | Reviewer L1 | Reviewer L2 |
|--------|------------|---------|------------------|-------------|-------------|-------------|
| Ajitesh Singh | 21-01-2026 | v1 | Ajitesh Singh | Komal Jaiswal | Akshit Kapil | Mahesh |


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
9. Installation  
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

## 1. Introduction
This document provides a step-by-step installation guide for **Java (OpenJDK)** in README.md format. It explains how to install Java, verify the installation, configure environment variables, and validate that Java is running correctly on Linux systems.

---

## 2. Purpose
The purpose of this guide is to ensure a standardized and repeatable process for installing Java across environments. It minimizes configuration errors, version mismatches, and setup inconsistencies.

---

## 3. Key Features
- Platform independent (Write once, run anywhere)  
- Secure and stable JVM  
- High performance and scalability  
- Large ecosystem and community support  
- Cloud and container friendly  
- Easy CI/CD integration  

---

## 4. Getting Started

### Pre-requisites

| License Type | Description | Commercial Use | Open Source |
|--------------|-------------|----------------|-------------|
| OpenJDK License | Free and open-source Java distribution | Yes | Yes |

---

## 5. Software Overview

| Software | Version |
|----------|---------|
| Java (OpenJDK) | 11 / 17 (LTS Recommended) |

---

## 6. System Requirements

| Requirement | Minimum Recommendation |
|-------------|------------------------|
| Processor | Dual-Core |
| RAM | 4 GB or higher |
| Disk Space | 10 GB or higher |
| OS Required | Linux (Ubuntu / Amazon Linux / RHEL) |

---

## 7. Important Ports

| Port | Description |
|------|-------------|
| 22 | SSH access |
| 8080 | Java application runtime port |
| 8443 | Secure application port (HTTPS) |

---

## 8. Dependencies

### Run-time Dependency

| Dependency | Version | Description |
|------------|---------|-------------|
| Java JDK | 11 / 17 | Required to compile and run Java applications |

### Other Dependency

| Dependency | Version | Description |
|------------|---------|-------------|
| curl / wget | Latest | Download packages |
| unzip | Latest | Extract archives |

---

## 9. Installation

### Step 1 – Update System Packages
```bash
sudo apt update
```

### Step 2 – Install Java
```bash
sudo apt install openjdk-17-jdk -y
```

### Step 3 – Verify Installation
```bash
java -version
javac -version
```

### Step 4 – Configure JAVA_HOME (Optional)
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

### Step 5 – Test Java Execution
```bash
java --help
```

---

## 10. Configuration
Configuration includes environment variables and JVM parameters.

Example:
```bash
export JAVA_OPTS="-Xms512m -Xmx1024m"
```

---

## 11. Maintenance

Update Java:
```bash
sudo apt update
sudo apt upgrade openjdk-17-jdk
```

Check version:
```bash
java -version
```

---

## 12. Monitoring

Check Java processes:
```bash
ps -ef | grep java
```

Check open ports:
```bash
netstat -tulnp | grep java
```

Logs (application dependent):
```
/var/log/<application-name>/
```

---

## 13. Disaster Recovery
- Maintain backups of configuration files.  
- Keep VM snapshots or AMIs.  
- Store installation scripts securely.  
- Document recovery procedures.  

---

## 14. High Availability
- Deploy multiple Java instances.  
- Use load balancers.  
- Implement auto scaling or Kubernetes.  
- Monitor application health.  

---

## 15. Troubleshooting

| Issue | Possible Cause | Solution |
|------|----------------|----------|
| java command not found | Java not installed | Reinstall Java |
| Wrong Java version | Multiple versions installed | Use update-alternatives |
| Permission denied | Insufficient privileges | Use sudo |
| Application not starting | Port conflict | Check logs and ports |

---

## 16. FAQs

**Is Java free?**  
Yes, OpenJDK is open-source and free.

**Can Java run on cloud platforms?**  
Yes, Java runs on AWS, Azure, GCP, and on-prem.

**Which version should I use?**  
Java 17 LTS is recommended.

---

## 17. Contact Information

| Name | Email |
|------|-------|
| Ajitesh Singh | ajitesh.singh.snaatak@mygurukulam.co |

---

## 18. References

| Link | Description |
|------|-------------|
| https://openjdk.org | OpenJDK official documentation |
| https://docs.oracle.com/javase/ | Oracle Java documentation |
