# OWASP Top 10

### Cyber Security Internship  
*(TryHackMe OWASP Top 10)*  

**Author:** Harsh M Parikh  
**Email:** ph400764@gmail.com  

---

## A01 — Broken Access Control

**Definition:**  
Improper enforcement of user permissions allowing privilege escalation or unauthorized access.  

**Impact:**  
Data leakage, privilege escalation, account takeover.  

**Lab / Practical Notes:**  
- Lab objective: Identify endpoints that return data for other user IDs; attempt forced browsing to admin endpoints.  
- Example reconnaissance commands (lab-only):  
  - Enumerate endpoints in the app and test parameter tampering.  
  - Use `/users/{id}` endpoints to check access control enforcement.  

**How it can be exploited:**  
- Modify a user ID parameter to access another user’s data (in lab).  
- Use an authenticated low-privilege account and access an admin URL by changing the path or ID.  

**Mitigation:**  
- Enforce server-side authorization checks for every protected resource.  
- Use a central access control library, avoid relying on client-side controls.  
- Implement least privilege and role-based access checks on every request.  

**TryHackMe-style lab summary:**  
- Steps: Enumerate endpoints → login as normal user → change resource identifiers → observe response codes/content differences → document.  
- Deliverable evidence: Request/response snippets (redacted), explanation of check and fix.  

---

## A02 — Cryptographic Failures

**Definition:**  
Weak or misconfigured cryptography (e.g., weak algorithms, no TLS, poor key management).  

**Impact:**  
Data exposure, broken confidentiality, credential theft.  

**Lab / Practical Notes:**  
Check for:  
- Use of HTTP rather than HTTPS.  
- Deprecated algorithms (MD5, SHA1) or weak ciphers.  
- Sensitive data stored in plaintext.  

**Mitigation:**  
- Use TLS 1.2/1.3 only; enforce HSTS.  
- Use well-vetted libraries and strong algorithms (AES-GCM, RSA-2048+/ECDHE).  
- Proper key lifecycle and secret management (vaults, environment variables).  

---

## A03 — Injection (SQL, NoSQL, OS, LDAP)

**Definition:**  
Unsanitized input interpreted by an interpreter — leads to unauthorized commands or data.  

**Impact:**  
Data exfiltration, remote command execution, authentication bypass.  

**Lab / Practical Notes:**  
- Lab objective: Demonstrate how user input can change backend queries (lab-only, authorized).  
- Testing approach: Parameterize inputs, observe application errors, identify unsanitized fields.  

**Mitigation:**  
- Use parameterized queries/prepared statements.  
- Strong input validation and ORM-safe patterns.  
- Least privilege database users.  

---

## A04 — Insecure Design

**Definition:**  
Flaws introduced during the design phase (missing threat modeling and secure defaults).  

**Impact:**  
Broad — from authentication flaws to insecure data flows.  

**Mitigation:**  
- Perform threat modeling during design.  
- Adopt secure design patterns.  
- Follow the “default deny” principle.  

---

## A05 — Security Misconfiguration

**Definition:**  
Misconfigured servers, cloud services, frameworks, or default credentials left enabled.  

**Impact:**  
Account takeover, data leakage, pivoting.  

**Lab / Practical Notes:**  
- Check for publicly accessible services, directory listings, default pages, and permissive CORS.  

**Mitigation:**  
- Harden images, remove default accounts, secure cloud buckets and services.  

---

## A06 — Vulnerable and Outdated Components

**Definition:**  
Use of components with known vulnerabilities (libraries, frameworks) without updates.  

**Impact:**  
Remote code execution, data leaks.  

**Mitigation:**  
- Maintain a Software Bill of Materials (SBOM).  
- Use dependency scanners (OSS tools).  
- Apply regular updates and security patches.  

---

## A07 — Identification and Authentication Failures

**Definition:**  
Weak authentication primitives or broken session management.  

**Impact:**  
Account takeover, privilege escalation.  

**Mitigation:**  
- Implement multi-factor authentication (MFA).  
- Protect session tokens (secure, HttpOnly).  
- Rotate tokens on sensitive operations.  

---

## A08 — Software and Data Integrity Failures

**Definition:**  
Trusting unverified sources — e.g., CI/CD artifacts, unsigned packages.  

**Impact:**  
Supply-chain compromise.  

**Mitigation:**  
- Verify signatures.  
- Use reproducible builds.  
- Lock down build pipelines.  

---

## A09 — Security Logging and Monitoring Failures

**Definition:**  
Lack of sufficient logging or missing alerting for suspicious activity.  

**Impact:**  
Delayed detection of breaches.  

**Mitigation:**  
- Centralize logs.  
- Configure alerts for anomalies.  
- Apply log retention and incident response procedures.  

---

## A10 — Server-Side Request Forgery (SSRF)

**Definition:**  
Server-side code fetches remote resources without validating URLs, allowing arbitrary server requests.  

**Impact:**  
Access to sensitive internal services.  

**Mitigation:**  
- Whitelist external endpoints.  
- Restrict outbound access.  
- Validate and sanitize URLs.  

---

## Screenshot

*(Insert your Command Injection screenshot or proof image here)*  

---

**Prepared by:**  
**Harsh M Parikh**  
ph400764@gmail.com
