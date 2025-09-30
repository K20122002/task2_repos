# task2_repos
Task 2: Analyze a Phishing Email Sample
# Phishing Email Analysis — Task 2

**Student:** Kanishga  
**Task:** Analyze a phishing email sample and provide evidence that it is malicious.

---

## What’s inside this repository
- `sample_phish.eml` — raw phishing email sample (headers + body).  
- `headers.txt` — extracted header excerpt highlighting SPF/DKIM/DMARC results.  
- `analysis.md` — detailed analysis, findings, risk rating, and recommended actions.  
- `tools_and_commands.txt` — safe commands and online tools to check links and DNS.  
- `interview_answers.txt` — short answers to common task questions.  
- `screenshots/` — folder for evidence screenshots (add your images here).

---

## How I performed the analysis (summary)
1. Saved the email as `sample_phish.eml`.  
2. Extracted and reviewed headers (looked at `Received:`, `Return-Path:`, and `Authentication-Results:`).  
3. Checked link text vs actual URL (hovered or inspected the raw `.eml`).  
4. Assessed SPF/DKIM/DMARC results — authentication failures indicate spoofing.  
5. Scanned the suspicious URL using VirusTotal / urlscan.io for reputation evidence.  
6. Compiled findings and screenshots into `analysis.md` and `screenshots/`.

---

## Key findings (short)
- Sender appears as **Google Support** but email uses `support@goog1e.com` (typo/similar-looking domain).  
- `Authentication-Results` show **SPF=fail**, **DKIM=none**, **DMARC=fail** → authentication failed.  
- Link text claims `accounts.google.com` but actual target is `secure-google.verify-account.com` → credential harvesting.  
- Risk: **High** — recommended do not click, report and delete.

---

## What you should upload as evidence
Place these files inside `screenshots/` before submission:
- `headers_view.png` — screenshot showing the raw headers or "Show original" with SPF/DKIM results.  
- `hover_link.png` — screenshot showing the real URL when hovering the link (or the URL text in the `.eml`).  
- `virustotal.png` or `urlscan.png` — scan results for the suspicious URL.

---

## How to push this repo to GitHub (quick)
```bash
git init
git add .
git commit -m "Phishing email analysis — Task 2"
# create a repository on GitHub, then:
git remote add origin https://github.com/YOUR_USERNAME/phishing-analysis.git
git branch -M main
git push -u origin main
