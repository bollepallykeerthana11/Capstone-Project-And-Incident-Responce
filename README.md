# Capstone-Project-And-Incident-Responce
# 🔐 Capstone Project and Incident Response

## 📌 Project Overview

This capstone project focuses on conducting a practical **Web Application Penetration Test** using **Kali Linux** and **Damn Vulnerable Web Application (DVWA)**.

The assessment was performed in a controlled local lab environment to identify common web application security vulnerabilities, collect evidence, document security findings, and demonstrate a basic incident-response workflow.

The project combines two important cybersecurity activities:

- 🔎 Web Application Security Testing
- 🚨 Incident Detection and Response

The objective is to understand how vulnerabilities can be identified, validated in a controlled environment, documented with evidence, and followed by appropriate mitigation and incident-response recommendations.

---

## 🎯 Objectives

The main objectives of this project are:

- Perform reconnaissance and security testing against a deliberately vulnerable web application.
- Identify common web application vulnerabilities.
- Validate vulnerabilities in a controlled environment.
- Capture screenshots and terminal outputs as evidence.
- Document security findings and their potential impact.
- Simulate detection of suspicious activity through logs.
- Demonstrate a basic incident-response process.
- Recommend mitigation and security-hardening measures.
- Prepare professional cybersecurity documentation.

---

## 🧪 Project Environment

The project was conducted in an isolated/local testing environment.

### Target

**Damn Vulnerable Web Application (DVWA)**

DVWA is intentionally designed for security testing and learning purposes.

### Testing Platform

**Kali Linux**

Kali Linux was used as the primary security-testing environment.

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| Kali Linux | Security testing environment |
| DVWA | Vulnerable web application used as the target |
| Nmap | Network reconnaissance and scanning |
| Burp Suite | Web application request/response analysis |
| Browser Developer Tools | Web application inspection |
| Linux Terminal | Command execution and evidence collection |
| DVWA Logs / Incident Log | Detection and incident documentation |

---

## 🔍 Testing Methodology

The penetration-testing process followed a structured approach:

### 1. Reconnaissance

The target environment was identified and basic information about the application and available services was collected.

### 2. Scanning

Network and service scanning was performed to identify accessible services and understand the target environment.

### 3. Web Application Assessment

DVWA modules were tested to identify common vulnerabilities and weaknesses.

### 4. Controlled Exploitation

Identified vulnerabilities were safely validated within the intentionally vulnerable DVWA environment.

### 5. Evidence Collection

Screenshots, terminal outputs, HTTP requests/responses, and log entries were collected to support the findings.

### 6. Documentation

Each identified issue was documented with its description, impact, evidence, and recommended mitigation.

---

## 🔥 Vulnerabilities Tested

The assessment included testing for common web application vulnerabilities such as:

### SQL Injection

SQL Injection testing was performed to demonstrate how improperly handled user input can affect database queries.

**Potential Impact:**
- Unauthorized access to database information
- Data exposure
- Data manipulation
- Authentication bypass in vulnerable applications

**Recommended Mitigation:**
- Use parameterized queries/prepared statements.
- Validate and sanitize user input.
- Apply least-privilege database permissions.
- Avoid dynamically constructed SQL queries.

---

### Cross-Site Scripting (XSS)

XSS testing was performed to identify whether malicious client-side input could be executed by the application.

**Potential Impact:**
- Session compromise
- Malicious script execution
- User data exposure
- Website defacement

**Recommended Mitigation:**
- Implement proper output encoding.
- Validate and sanitize user input.
- Use Content Security Policy (CSP).
- Configure secure cookie attributes.

---

### Command Injection

Command Injection testing was performed to demonstrate the security risks of allowing untrusted input to reach operating-system commands.

**Potential Impact:**
- Unauthorized command execution
- System compromise
- Information disclosure
- Potential lateral movement

**Recommended Mitigation:**
- Avoid executing operating-system commands with user-controlled input.
- Use allowlists for permitted values.
- Validate input strictly.
- Run services with minimum required privileges.

---

## 🚨 Incident Response Simulation

As part of the project, a basic incident-response scenario was simulated using security events and log entries.

The incident-response workflow followed these stages:

### 1. Detection

Suspicious activities were identified through application activity and incident-log entries.

Examples included events related to:

- SQL Injection
- Cross-Site Scripting
- Command Injection

### 2. Analysis

The recorded activity was reviewed to determine the type of attack and the potentially affected application component.

### 3. Containment

The affected vulnerable functionality should be isolated or temporarily disabled while investigation and remediation are performed.

### 4. Eradication

The root cause of the vulnerability should be addressed through secure coding practices, input validation, access control, and configuration hardening.

### 5. Recovery

The application can be restored after remediation and verification testing confirms that the vulnerability has been addressed.

### 6. Post-Incident Review

The incident findings, evidence, impact, and recommended preventive controls are documented for future security improvement.

---

## 📊 Security Findings

| Finding | Severity | Category | Recommended Action |
|---------|----------|----------|--------------------|
| SQL Injection | High | Injection | Use prepared statements and input validation |
| Cross-Site Scripting | Medium | Client-Side Injection | Apply output encoding and CSP |
| Command Injection | Critical | OS Command Injection | Avoid unsafe command execution and use strict allowlists |

> **Note:** Severity classifications are based on the potential impact demonstrated in the controlled lab environment and should be validated against the specific application context.

---

## 📸 Evidence

The repository contains evidence collected during the practical assessment, including:

- Network scanning results
- Terminal outputs
- DVWA vulnerability testing
- Web application screenshots
- HTTP request/response analysis
- Vulnerability evidence
- Incident-log entries
- Security findings and recommendations

---

## 📁 Project Structure

```text
Capstone-Project-And-Incident-Responce/
│
├── README.md
│
├── screenshots/
│   ├── reconnaissance/
│   ├── scanning/
│   ├── vulnerabilities/
│   └── incident-response/
│
├── scans/
│   └── scan-results.txt
│
├── logs/
│   └── incident.log
│
├── reports/
│   └── capstone-report.pdf
│
└── video/
    └── final-presentation.mp4
