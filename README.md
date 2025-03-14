Secure File Sharing Platform

Project Overview

The Secure File Sharing Platform is a web-based application designed to facilitate secure and efficient file sharing between users. The platform addresses key security challenges such as unauthorized access, data breaches, and interception during transmission by integrating robust security measures including end-to-end encryption, multi-factor authentication, and role-based access control.

Team Members

Mohsin Wazir (2022309)

Ibrahim Imran (2022301)

Zain Memon (2022630)

Sagar Kumar (2022522)

Features

1. User Authentication

OAuth 2.0: Secure login via Google, Microsoft, or email-based authentication.

Multi-Factor Authentication (MFA): OTP verification for enhanced security.

2. End-to-End Encryption

AES-256 Encryption: Ensures files at rest are protected.

TLS Protocol: Secures transmission of files between users.

3. Access Control

Role-Based Access Control (RBAC): Permissions for admins, uploaders, and viewers.

Time-limited access links for external users.

4. File Integrity and Anti-Tampering

Digital Signatures: Verify file authenticity and integrity.

Checksum Verification: Detects file corruption or tampering.

5. Activity Monitoring

Detailed Logs: Tracks upload, download, and access activities.

Alerts: Detects suspicious activities such as multiple failed login attempts.

6. Secure File Deletion

Secure wipe algorithms: Ensure permanent file deletion.

Security Measures

Authentication: OAuth 2.0 and MFA for strong verification, token-based session management.

Encryption: AES-256 for stored files, SSL/TLS for secure transmission, encrypted metadata.

Access Control: RBAC with custom policies, time-based access expiry.

Monitoring and Alerts: Real-time monitoring, anomaly detection, and backup options.

Technology Stack

Frontend: HTML5, CSS3, JavaScript (React or Angular)

Backend: Node.js or Django for handling APIs

Database: MySQL or MongoDB with encryption for stored data

Security Libraries: OpenSSL for encryption, JWT for authentication tokens

Expected Challenges

Balancing encryption security with file upload/download speed.

Securely managing key distribution and storage.

Ensuring compliance with data protection regulations (e.g., GDPR).

Conclusion

The Secure File Sharing Platform provides a secure and efficient solution for sharing files while mitigating risks such as unauthorized access, data breaches, and tampering. By leveraging strong encryption, authentication, and access control mechanisms, the platform ensures confidentiality, integrity, and availability of shared files.










# Threat Modeling & Risk Assessment

## Overview
This repository provides an in-depth analysis of threat modeling and risk assessment for securing a system. It outlines potential attack vectors, evaluates their risk levels, and proposes effective mitigation strategies to enhance security.

## 1. Identifying Attack Vectors
Attack vectors are the potential pathways attackers may exploit to compromise the system. Below are the key attack vectors categorized by system components:

### **Component-wise Potential Attack Vectors**
| Component | Potential Attack Vectors |
|-----------|--------------------------|
| User Authentication | Credential stuffing, Phishing attacks, MFA bypass |
| End-to-End Encryption | Man-in-the-middle (MITM) attacks, Key compromise, Weak encryption implementation |
| Access Control (RBAC) | Privilege escalation, Broken access control |
| File Storage & Transmission | Data leakage via metadata, Unauthorized access to stored files |
| File Integrity & Anti-Tampering | Digital signature forgery, Checksum collision attacks |
| Secure File Deletion | Data recovery from deleted files |

## 2. Risk Levels & Security Mitigation Strategies
| Attack Vector | Risk Level | Mitigation Strategies |
|--------------|-----------|----------------------|
| Credential Stuffing & Phishing | High | Enforce strong password policies, Implement account lockout, Use phishing-resistant MFA (FIDO2, WebAuthn) |
| MFA Bypass | Medium | Implement device fingerprinting, Use time-based OTPs (TOTP) instead of SMS |
| MITM Attacks | High | Enforce TLS 1.3, Use certificate pinning in client applications |
| Key Compromise | High | Implement HSM for key storage, Use periodic key rotation |
| Weak Encryption Implementation | Medium | Use AES-256 encryption, Conduct security audits |
| Privilege Escalation | High | Implement least privilege principle, Conduct access control audits |
| Broken Access Control | High | Implement server-side access validation, Perform role-based penetration testing |
| Data Leakage via Metadata | Medium | Encrypt metadata, Mask metadata from unauthorized users |
| Unauthorized File Access | High | Apply zero-trust principles, Implement granular access control policies |
| Digital Signature Forgery | Medium | Use SHA-3, BLAKE2, Ensure private keys remain confidential |
| Checksum Collision Attacks | Low | Use SHA-256 or SHA-3 |
| Data Recovery from Deleted Files | Medium | Use secure deletion algorithms (DoD 5220.22-M, Gutmann method) |

## 3. Summary & Security Best Practices
1. **Zero-Trust Security Model** - Continuously verify all access requests.
2. **Regular Security Audits & Penetration Testing** - Identify vulnerabilities proactively.
3. **Strong Authentication & Authorization** - Use MFA, OAuth 2.0, and strict RBAC policies.
4. **Secure File Handling** - Encrypt files at rest and in transit with AES-256 and TLS 1.3.
5. **Activity Monitoring & Incident Response** - Implement real-time anomaly detection.

## 4. Data Visualization
To better understand security risks and mitigation effectiveness, the following data visualizations can be implemented:
- **Risk Level Distribution:** Displays the number of attack vectors categorized as High, Medium, or Low risk.
- **Attack Vector Frequency:** Illustrates the proportion of different attack vectors in the system.
- **Mitigation Strategy Effectiveness:** Tracks the effectiveness of implemented security measures over a six-month period.

 5. References
 **NIST Cybersecurity Framework** ([https://www.nist.gov/cyberframework](https://www.nist.gov/cyberframework))
 **OWASP Security Guidelines** ([https://owasp.org/](https://owasp.org/))







