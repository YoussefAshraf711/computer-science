[العربي](./14-cybersecurity_ar.md)

# <a name="-14-cybersecurity"></a>🔒 Chapter 14: Cybersecurity

## 1. What is it?

Cybersecurity is the practice and technology of protecting computer systems, networks, devices, and data from malicious attacks, damage, or unauthorized access. It is a continuous battle between defenders (Blue Team) and attackers (Red Team).

The primary goal is to maintain the CIA Triad of information security:
 * `Confidentiality`: Ensuring that data is read only by authorized individuals.
 * `Integrity`: Ensuring that data is not tampered with or altered.
 * `Availability`: Ensuring that systems and data are available to legitimate users when needed.

## 2. What does the specialist do?

A cybersecurity analyst or engineer is the "digital guardian." Their responsibilities are broad and include:
 * Monitoring systems: Monitoring networks and systems for any suspicious activity.
 * Incident response: Analyzing security alerts and responding immediately to incidents when they occur.
 * Vulnerability assessment: Conducting periodic assessments and penetration testing to find weaknesses before attackers do.
 * Managing security tools: Implementing and managing tools like firewalls, intrusion detection systems, and antivirus software.
 * Developing security policies: Writing and implementing security policies and procedures within the organization.
 * User awareness: Educating employees about security best practices to avoid attacks like phishing.

## 3. Sub-domains

 * Network Security: Focuses on securing the network infrastructure.
 * Application Security (AppSec): Focuses on finding and fixing vulnerabilities in software and application code.
 * Cloud Security: Specializes in securing cloud environments.
 * Incident Response: The "firefighters" who respond to security incidents as they happen.
 * Penetration Testing: The "ethical hacker" who simulates attacks to discover vulnerabilities.
 * Digital Forensics: Investigating after a breach to find out what happened and who is responsible.
 * Governance, Risk, and Compliance (GRC): Focuses on policies, standards, and legal requirements.

## 4. Expanded Key Concepts

 * `Threat vs. Vulnerability vs. Risk`:
     * `Threat`: A potential danger (e.g., a hacker).
     * `Vulnerability`: A weakness that can be exploited (e.g., an unpatched server).
     * `Risk`: The likelihood of a threat exploiting a vulnerability and the resulting impact.
 * `Defense in Depth`: A strategy of having multiple layers of protection. If one layer fails, another layer is there to stop the attack.
 * `Zero Trust`: A modern security model that assumes no user or device can be trusted by default, even if it is inside the network. It requires strict verification for every access request.
 * `Encryption`: Symmetric encryption (using one key) and Asymmetric encryption (using a pair of keys, public and private).

## 5. Expanded Tools & Technologies

 * Network Security: Firewalls, IDS/IPS (Intrusion Detection/Prevention Systems like Snort), VPNs.
 * Endpoint Security: Antivirus/EDR (Advanced antivirus solutions like CrowdStrike).
 * Security Information and Event Management (SIEM): Splunk, QRadar (for analyzing security logs from multiple sources).
 * Vulnerability Scanning: Nessus, Qualys.
 * Penetration Testing: Metasploit, Burp Suite, Nmap, and the Kali Linux operating system.
 * Authentication: MFA/2FA (Multi-Factor Authentication), OAuth, SAML.

## 6. In-Depth Workflow

Project: A security analyst responds to a potential breach incident.

 1. Detection: An alert fires in the SIEM system: "Multiple failed login attempts followed by a successful login from an unknown IP address for a high-privilege account."
 2. Investigation: The on-duty analyst begins to investigate. They confirm the IP address is from a country where no employees work. This is highly suspicious. They check the real user's activity and find them logged in from a normal IP at the same time. This confirms the account has been compromised.
 3. Containment: The immediate goal is to stop the damage. The analyst takes two actions:
     * Forces a password reset for the compromised account and terminates all its active sessions, kicking out the attacker.
     * Temporarily blocks the malicious IP address at the firewall level.
 4. Eradication: As part of the incident response team, the analyst investigates what the attacker did. They analyze logs to see the commands executed and files accessed. They ensure the attacker did not install any malware or backdoors.
 5. Recovery: Systems are restored from a clean backup if necessary, and the account is re-enabled for the legitimate user after securely verifying their identity.
 6. Post-mortem: The team holds a blameless meeting to determine the root cause, which was "a weak password and no multi-factor authentication (MFA) enabled."
 7. Lessons Learned: The company enforces a new policy requiring mandatory MFA for all accounts and starts a password security awareness campaign.

## 7. Common Job Roles

 * Security Analyst (SOC Analyst)
 * Penetration Tester (Ethical Hacker)
 * Security Engineer
 * Incident Responder
 * Digital Forensics Analyst
 * Security Architect

## 8. A-Z Glossary
<details>
<summary>Click to expand/collapse the glossary</summary>

| Term | Explanation |
|---|---|
| **`Blue Team`** | The team responsible for defending systems. |
| **`Brute Force Attack`** | An attack that tries to guess a password by trying every possible combination. |
| **`Bug Bounty`** | Programs offered by companies to security researchers who discover vulnerabilities in their systems. |
| **`Cross-Site Scripting (XSS)`** | An attack where malicious scripts are injected into websites to be displayed to other users. |
| **`DDoS`** | Distributed Denial of Service attack, overwhelming a server with requests to take it offline. |
| **`Digital Signature`** | Used to ensure the integrity of content and the identity of the sender. |
| **`EDR`** | Endpoint Detection and Response, advanced antivirus solutions. |
| **`Exploit`** | Code or a method that takes advantage of a specific security vulnerability. |
| **`Hashing`** | Converting data into a unique, fixed-length string to ensure it has not been altered. |
| **`Honeypot`** | A decoy system intentionally set up to attract attackers and study their methods. |
| **`IDS/IPS`** | Intrusion Detection System / Intrusion Prevention System. |
| **`Malware`** | Malicious software (viruses, worms, trojans, ransomware). |
| **`MFA`** | Multi-Factor Authentication, requires two or more methods of identity verification. |
| **`Penetration Testing`** | Simulating a cyber attack on a system to evaluate its security. |
| **`Phishing`** | A social engineering attack to steal credentials. |
| **`Ransomware`** | A type of malware that encrypts a victim's files and demands a ransom. |
| **`Red Team`** | The team responsible for simulating attacks and testing defenses. |
| **`SIEM`** | Security Information and Event Management, a tool that collects and analyzes security logs from multiple sources. |
| **`Social Engineering`** | The art of manipulating people into revealing confidential information. |
| **`SQL Injection`** | An attack where malicious SQL commands are injected into database queries. |
| **`Vulnerability`** | A weakness in a system or application that can be exploited. |
| **`Zero-Day Exploit`** | An attack that exploits an unknown security vulnerability for which no patch has been released. |

</details>

[⬆️ Back to Table of Contents](README.md)