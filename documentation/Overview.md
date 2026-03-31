# Overview

## Objective
The objective of this task is to understand the fundamentals of Cyber Security and become familiar with core concepts, threats, and defensive practices.

## What is Cyber Security?
Cyber Security is the practice of protecting systems, networks, and data from digital attacks such as unauthorized access, data breaches, malware, and denial-of-service attacks.

## Why Cyber Security is Important
- Protects sensitive data
- Prevents financial loss
- Ensures system availability
- Protects privacy and trust

## Common Cyber Threats
- Malware
- Phishing
- Ransomware
- Brute-force attacks
- Man-in-the-middle attacks

## Basic Security Practices
- Strong passwords
- Two-factor authentication
- Regular updates
- Secure network usage
- User awareness

## Conclusion
This task helped in building a foundational understanding of Cyber Security concepts which will be applied in upcoming practical tasks.

## Target Application
The selected target for this task is OWASP Juice Shop, a deliberately insecure web application developed by OWASP for security training and awareness purposes.

**URL:** https://pwning.owasp-juice.shop  
**Authorization:** Publicly available and explicitly allowed for security testing  
**Purpose:** Demonstrates common web application security vulnerabilities

## Scope of Assessment
The assessment was limited strictly to:
- Passive analysis
- Observation of security headers
- Publicly accessible application behavior

No exploitation, authentication bypass, or active attacks were performed.

## Security Header Analysis

During analysis of HTTP response headers, it was observed that some recommended security headers were missing or not properly configured.

### Findings
- Content-Security-Policy header was missing
- X-Frame-Options header was not enforced

### Impact
Missing security headers may increase the risk of:
- Cross-site scripting (XSS)
- Clickjacking attacks

### Recommendation
It is recommended to implement standard HTTP security headers such as Content-Security-Policy and X-Frame-Options to reduce exposure to common client-side attacks.

## Passive Vulnerability Scan (OWASP ZAP)

A passive vulnerability scan was conducted using OWASP ZAP against the OWASP Juice Shop application.

### Tool Used
- OWASP ZAP (Passive Scan)

### Observations
The passive scan identified several low to medium risk security issues, including:
- Missing Anti-clickjacking Header
- Content Security Policy not set
- Information disclosure through response headers

### Impact
While these issues do not immediately compromise the application, they may assist attackers in exploiting client-side vulnerabilities.

### Recommendation
It is recommended to properly configure security headers and minimize unnecessary information disclosure to enhance the security posture of the application.
