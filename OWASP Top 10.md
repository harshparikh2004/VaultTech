# OWASP Top 10


 

 
Cyber Security Internship 

 

(TryHackMe OWASP Top 10) 

 

 

 

 

 

 

Harsh M Parikh 

ph400764@gmail.com 

  

mailto:ph400764@gmail.com


OWASP Top 10 
 

  

HARSH PARIKH PAGE - 1 

  ph400764@gmail.com 

A01 — Broken Access Control 

Definition: Improper enforcement of user permissions allowing privilege 

escalation or unauthorized access. 

Impact: Data leakage, privilege escalation, account takeover. 

Lab / Practical notes 

• Lab objective: identify endpoints that return data for other user IDs; 

attempt forced browsing to admin endpoints. 

• Example reconnaissance commands (lab-only): 

o Enumerate endpoints in the app and test parameter tampering. 

o Use /users/{id} endpoints to check access control enforcement. 

How it can be exploited: 

• Modify a user id parameter to access another user’s data (in lab).  

• Use an authenticated low-privilege account and access an admin URL 

by changing path or ID. 

Mitigation 

• Enforce server-side authorization checks for every protected 

resource. 

• Use a central access control library, avoid relying on client-side 

controls. 

• Implement least privilege and role-based access checks on every 

request. 

TryHackMe-style lab summary 

• Steps: enumerate endpoints → login as normal user → change 

resource identifiers → observe response codes / content differences 

→ document. 

• Deliverable evidence: request/response snippets (redacted), 

explanation of check and fix. 

A02 — Cryptographic Failures 

Definition: Weak or misconfigured cryptography (e.g., weak algorithms, no 

TLS, poor key management). 



OWASP Top 10 
 

  

HARSH PARIKH PAGE - 2 

  ph400764@gmail.com 

Impact: Data exposure, broken confidentiality, credential theft. 

Lab / Practical notes 

• Check for: 

o Use of HTTP rather than HTTPS. 

o Deprecated algorithms (MD5, SHA1) or weak ciphers. 

o Sensitive data stored in plaintext. 

Mitigation 

• Use TLS 1.2/1.3 only; enforce HSTS. 

• Use well-vetted libraries and strong algorithms (AES-GCM, RSA-

2048+/ECDHE). 

• Proper key lifecycle and secret management (vaults, environment 

variables). 

A03 — Injection (SQL, NoSQL, OS, LDAP) 

Definition: Unsanitized input interpreted by an interpreter — leads to 

unauthorized commands or data. 

Impact: Data exfiltration, remote command execution, bypass auth. 

Lab / Practical notes 

• Lab objective: demonstrate how user input can change backend 

queries (lab-only, authorized). 

• Testing approach (lab-only): parameterize inputs, observe 

application errors, identify unsanitized fields. 

Mitigation 

• Use parameterized queries / prepared statements. 

• Strong input validation and ORM-safe patterns. 

• Least privilege DB users. 

A04 — Insecure Design 

Definition: Flaws introduced during design phase (missing threat 

modeling and secure defaults). 

Impact: Broad — from authentication flaws to insecure data flows. 



OWASP Top 10 
 

  

HARSH PARIKH PAGE - 3 

  ph400764@gmail.com 

Mitigation 

• Threat modeling in design phase, adopt secure design patterns, 

default-deny. 

 

A05 — Security Misconfiguration 

Definition: Misconfigured servers, cloud services, frameworks, or default 

credentials left enabled. 

Impact: Account takeover, data leakage, pivoting. 

Lab / Practical notes 

• Check publicly accessible services, directory listings, default pages, 

and permissive CORS. 

Mitigation 

• Harden images, remove default accounts, secure cloud buckets and 

services. 

 

A06 — Vulnerable and Outdated Components 

Definition: Use of components with known vulnerabilities (libraries, 

frameworks) without updates. 

Impact: Remote code execution, data leaks. 

Mitigation 

• Maintain SBOM, use dependency scanners (OSS tools), run regular 

updates and patches. 

 

A07 — Identification and Authentication Failures 

Definition: Weak authentication primitives, broken session management. 

Impact: Account takeover, privilege escalation. 

Mitigation 

• Implement MFA, protect session tokens (secure, HttpOnly), rotate 

tokens on sensitive operations. 



OWASP Top 10 
 

  

HARSH PARIKH PAGE - 4 

  ph400764@gmail.com 

 

A08 — Software and Data Integrity Failures 

Definition: Trusting unverified sources — e.g., CI/CD artifacts, unsigned 

packages. 

Impact: Supply-chain compromise. 

Mitigation 

• Verify signatures, use reproducible builds, lock down build pipelines.  

 

A09 — Security Logging and Monitoring Failures 

Definition: Lack of sufficient logging, or missing alerting for suspicious 

activity. 

Impact: Delayed detection of breaches. 

Mitigation 

• Centralized logs, alert on anomalies, retention policies, and incident 

response plans. 

 

A10 — Server-Side Request Forgery (SSRF) 

Definition: Server-side code fetches remote resources without validating 

URLs, allowing arbitrary server requests. 

Impact: Access to sensitive internal services. 

Mitigation 

• Whitelist external endpoints, restrict outbound access, validate and 

sanitize URLs. 

  



OWASP Top 10 
 

  

HARSH PARIKH PAGE - 5 

  ph400764@gmail.com 

Screenshot :  

 

 
