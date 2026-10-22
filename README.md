# Automated Web Security Scanner

**IBM SkillsBuild Cyber Security 2026 — Student Project**

A lightweight Python project that checks common HTTP security headers, observes basic CORS response headers, checks whether the final URL uses HTTPS, and exports findings as JSON.

## Features
- Checks Strict-Transport-Security, Content-Security-Policy, X-Content-Type-Options, X-Frame-Options, Referrer-Policy, and Permissions-Policy.
- Observes Access-Control-Allow-Origin, Access-Control-Allow-Credentials, and Vary.
- Prints findings and remediation recommendations.
- Saves results to `scan_report.json`.

## Requirements
- Python 3.10 or later recommended
- `requests` package
- Jupyter Notebook/JupyterLab for interactive notebook execution

## Setup
```bash
python -m pip install -r requirements.txt
```
Open `Student_AutomatedWebScanner.ipynb` in Jupyter, run the cells, and set `TARGET_URL` to a site you own or are explicitly authorized to test.

## Responsible use
Only test systems you own or have explicit permission to assess. This tool makes one non-destructive GET request and is an educational baseline, not a full penetration test. Missing headers and wildcard CORS are not automatically proof of a vulnerability; validate findings in context.

## Limitations
The scanner does not crawl pages, test authenticated routes, or exhaustively test CORS behavior. See the project report for methodology, limitations, and future enhancements.
