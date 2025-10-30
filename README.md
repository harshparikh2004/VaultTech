# Vault-Tec — Second Month Submission — Harsh M Parikh

**Cyber Security Internship — Second Month**
**Author:** Harsh M Parikh
**Email:** [ph400764@gmail.com](mailto:ph400764@gmail.com)
**Date:** 31 October 2025



## Purpose

This repository contains my submission for Vault-Tec Security’s second month tasks:

1. OWASP Top 10 (TryHackMe-style writeups)
2. PicoCTF — 40 challenge summaries
3. Bug Bounty (OWASP Juice Shop) — simulated/educational report
   All reports are provided in **Markdown (.md)** for easy browsing on GitHub and **PDF (.pdf)** for formal submission.



## Repo structure

```
/README.md
/OWASP_Top_10_Report.md
/OWASP_Top_10_Report.pdf
/PicoCTF_40_Challenges_Report.md
/PicoCTF_40_Challenges_Report.pdf
/Bug_Bounty_Report_JuiceShop.md
/Bug_Bounty_Report_JuiceShop.pdf
/Proof_of_Completion.md        # optional short single-page statement
/Proof_of_Completion.pdf       # optional PDF
/artifacts/                    # screenshots, HAR files, command-output images (redacted)
```

---

## How to review (quick)

* View Markdown files directly on GitHub for readable, clickable content.
* Open the `.pdf` files for the formal / printable submission artifacts.
* Artifacts (screenshots, HARs) are under `/artifacts/`. Sensitive values (API keys, live-site PII) are **redacted**.



## How I prepared the files

* Markdown files were created/cleaned from lab notes and PDF exports to preserve formatting and readability.
* PDFs are export-ready (formatted for printing and emailing).
* All active testing was performed **only** on authorized training targets (TryHackMe, PicoCTF, OWASP Juice Shop). No unauthorized testing of third-party sites was done.



## Convert Markdown → PDF (recommended)

Option A — **pandoc** (CLI, reproducible)

```bash
# install pandoc (if necessary)
# Ubuntu/Debian: sudo apt-get install pandoc texlive-xetex
pandoc OWASP_Top_10_Report.md -o OWASP_Top_10_Report.pdf --pdf-engine=xelatex
pandoc PicoCTF_40_Challenges_Report.md -o PicoCTF_40_Challenges_Report.pdf --pdf-engine=xelatex
pandoc Bug_Bounty_Report_JuiceShop.md -o Bug_Bounty_Report_JuiceShop.pdf --pdf-engine=xelatex
```

Option B — **VSCode / Browser**

* Open `.md` in VSCode, use Markdown preview, then `File → Print → Save as PDF`.
* Or paste into Word / Google Docs and export as PDF.



## Commit & push (exact commands)

```bash
git init                      # if not already a git repo
git add .
git commit -m "Second month submission — OWASP, PicoCTF, Bug Bounty — Harsh Parikh"
git branch -M main            # optional: set branch to main
git remote add origin <ssh-or-https-repo-url>
git push -u origin main
```

Suggested commit message:
`Second month submission — OWASP, PicoCTF, Bug Bounty — Harsh Parikh`



## Email for submission (copy-paste)

To: [vaulttecconsultancy@gmail.com](mailto:vaulttecconsultancy@gmail.com)
Subject: Vault-Tec — Second Month Submission — Harsh Parikh

```
Dear Vault-Tec Team,

Please find attached my submission for the second month tasks (OWASP Top 10 lab summaries, PicoCTF challenge write-ups, and a simulated bug bounty report on OWASP Juice Shop).

GitHub Repository:
https://github.com/<your-username>/VaultTec-SecondMonth-HarshParikh

Attached PDFs:
- OWASP_Top_10_Report.pdf
- PicoCTF_40_Challenges_Report.pdf
- Bug_Bounty_Report_JuiceShop.pdf
- Proof_of_Completion.pdf (optional)

All active testing was performed only on authorized lab targets (TryHackMe, PicoCTF, OWASP Juice Shop). If you require original HARs, screenshots, or additional lab artifacts, I can provide them on request.

Best regards,  
Harsh M Parikh  
ph400764@gmail.com
```

Replace `<your-username>` with your GitHub username.



## Artifacts & evidence

* Place screenshots and HAR/HTTP traces in `/artifacts/`.
* Filenames should be descriptive, e.g.:

  * `artifacts/owasp_command_injection_poc.png`
  * `artifacts/pico_pcap_snapshot.png`
  * `artifacts/juice_shop_idor_response.har`
* Always ensure redaction of any real credentials or third-party PII before committing.



## Notes on legality & ethics

* All testing described in this repo was performed on **authorized training targets** only.
* Do **not** run any of the described offensive tests against live third-party systems without written permission.
* If Vault-Tec wishes, I can provide additional artifacts or live demo access to the lab environment used.



## Checklist (before sending)

* [ ] All `.md` and `.pdf` files present and named as above.
* [ ] `/artifacts/` contains screenshots referenced in reports.
* [ ] Repo pushed to GitHub and link confirmed working.
* [ ] PDFs attached to email to [vaulttecconsultancy@gmail.com](mailto:vaulttecconsultancy@gmail.com).
* [ ] Proof_of_Completion.pdf attached (optional).



## Contact

If you need any edits, extra screenshots, or a single consolidated ZIP of the repo, ping me here or email: **[ph400764@gmail.com](mailto:ph400764@gmail.com)**


**Prepared by:**
**Harsh M Parikh** — Vault-Tec Security intern
30 October 2025



