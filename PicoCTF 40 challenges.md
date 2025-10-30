# PicoCTF — 40 Challenge Summaries  

### Cyber Security Internship  
*(PicoCTF Tasks — Vault-Tec Security)*  

**Author:** Harsh M Parikh  
**Email:** ph400764@gmail.com  

---

## Summary

This file contains 40 concise challenge write-ups across categories: **Forensics, Cryptography, Web Exploitation, Reverse Engineering, and General Skills.**  
Each entry includes the challenge title, concept, approach, and key learning outcomes derived from solving them.

---

## Forensics (1–10)

1. **Dumpster Dive (Forensics)**  
   - **Concept:** Recover hidden data from a provided file.  
   - **Approach:** Use `binwalk`, `strings`, and `foremost` to extract hidden files or data.  
   - **Learning:** File carving basics and metadata extraction.

2. **Image Stego (Forensics)**  
   - **Concept:** LSB steganography.  
   - **Approach:** `steghide extract -sf image.png` or use Python scripts to read LSB data.  
   - **Learning:** How data can be embedded in images and extracted using analysis tools.

3. **PCAP Analysis (Forensics)**  
   - **Concept:** Network capture analysis.  
   - **Approach:** Analyze `.pcap` with `Wireshark` or `tshark` to identify traffic patterns and extract data.  
   - **Learning:** Identify credentials and artifacts from network traces.

4–10. Memory dump analysis, ZIP password recovery, EXIF metadata extraction, audio steganography, and hidden partition challenges.  
   - **Tools:** `volatility`, `exiftool`, `audacity`, `fcrackzip`, and `autopsy`.  
   - **Learning:** Digital forensics workflow and artifact recovery.

---

## Cryptography (11–18)

11. **Caesar Cipher (Crypto)**  
   - **Concept:** Simple substitution cipher.  
   - **Approach:** Brute-force shift or use frequency analysis.  
   - **Learning:** Basic cryptographic principles and key rotation understanding.

12. **RSA Weak Key (Crypto)**  
   - **Concept:** Factorization of a small RSA modulus.  
   - **Approach:** Use `rsatool` or factoring scripts to derive private key and decrypt ciphertext.  
   - **Learning:** The importance of secure key generation and key size in RSA.

13–18. XOR cipher, base encodings, modular arithmetic puzzles, and AES padding oracle examples.  
   - **Learning:** Understanding encryption modes, key reuse weaknesses, and mathematical cipher logic.

---

## Web Exploitation (19–28)

19. **Simple SQLi (Web)**  
   - **Concept:** SQL injection via unsanitized input.  
   - **Approach:** Test `' OR '1'='1` (lab-only), and automate exploitation with `sqlmap`.  
   - **Learning:** Input sanitization, parameterized queries, and ORM safety.

20. **Stored XSS (Web)**  
   - **Concept:** Persistent Cross-Site Scripting.  
   - **Approach:** Find input fields that reflect HTML, test benign payloads in a lab environment.  
   - **Learning:** Contextual output encoding and enforcing CSP policies.

21–28. CSRF token misconfiguration, cookie tampering, insecure authentication, and access control flaws.  
   - **Learning:** Safe web testing methodologies and defense strategies.

---

## Reverse / Binary Exploitation (29–34)

29. **Basic Reversing (Reverse)**  
   - **Concept:** Reverse-engineer small binaries to extract flags.  
   - **Approach:** Use `strings`, `gdb`, and `ghidra` to analyze control flow.  
   - **Learning:** Function tracing and understanding compiled program logic.

30–34. Crackme challenges, buffer overflow basics, and format string vulnerability analysis (lab-only).  
   - **Tools:** `objdump`, `radare2`, and `pwndbg`.  
   - **Learning:** Memory safety concepts and low-level debugging.

---

## General Skills / Miscellaneous (35–40)

35. **Linux PrivEsc (General)**  
   - **Concept:** Find privilege escalation opportunities in Linux.  
   - **Approach:**  
     - `sudo -l`  
     - `find / -perm -4000 -type f 2>/dev/null`  
   - **Learning:** Importance of permissions and SUID configurations in system hardening.

36–40. Scripting, network scanning, and encoding challenges using `bash` and `python`.  
   - **Learning:** Problem-solving and automation for cybersecurity tasks.

---

## Conclusion

Completing these 40 PicoCTF challenges helped me strengthen my understanding of **forensics, cryptography, web vulnerabilities, and reverse engineering**.  
Each challenge reinforced my ability to approach problems analytically and apply real-world cybersecurity tools effectively.

**Key Tools Used:**  
`Wireshark`, `tshark`, `binwalk`, `openssl`, `sqlmap`, `Burp Suite`, `Python`, `nmap`, `gdb`

---

**Prepared by:**  
**Harsh M Parikh**  
ph400764@gmail.com  
30 October 2025
