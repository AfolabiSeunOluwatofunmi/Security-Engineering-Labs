# Lab Report: TryHackMe - Offensive Security Intro

## 📋 Executive Summary
This laboratory exercise documents practical web application penetration testing concepts completed on the `TryHackMe` platform. The engagement focused on offensive security fundamentals, including reconnaissance, identifying hidden administrative endpoints, and exploiting insecure direct object references or flawed authorization controls within a simulated banking environment.

---

## 🛠️ Environment & Tools
* **Platform:** TryHackMe (Offensive Security Intro Module)
* **Target Application:** Simulated Web Banking Portal
* **Key Techniques:** Directory/Page Discovery, Web Parameter Manipulation, Access Control Testing

---

## 🔍 Attack Walkthrough & Findings

### 1. Reconnaissance & Hidden Page Discovery
* **Objective:** Locate unlinked or hidden directories/pages within the target application.
* **Findings:** Successfully navigated through initial discovery phases to identify administrative panels and hidden routing paths that are not exposed via the primary user interface navigation links.

### 2. Authorization Testing & Parameter Manipulation
* **Objective:** Test backend validation on financial transaction endpoints (`/bank-transfer`).
* **Execution:** Utilized the discovered administrative interface and tested parameter manipulation by submitting target account identifiers (e.g., account number `8881`) and simulated transaction amounts.
* **Impact:** Demonstrated how inadequate server-side input validation and missing function-level access controls can lead to unauthorized balance modifications and privilege escalation vulnerabilities.

---

## 🛡️ Remediation & Defensive Hardening
1. **Enforce Role-Based Access Control (RBAC):** Ensure all administrative routes and function endpoints verify user session privileges before rendering data or executing actions.
2. **Server-Side Transaction Validation:** Implement rigorous multi-step validation checks on financial transfers to prevent client-side parameter tampering.
3. **Directory Obfuscation & Security Through Design:** Never rely on hiding URLs through obscurity (security through obscurity); enforce strict authentication across all application endpoints.

---
*Author: Afolabi Seun Oluwatofunmi | Cloud & AI Security Engineering Practitioner*
