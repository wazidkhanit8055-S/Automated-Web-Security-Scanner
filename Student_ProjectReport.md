# Project Report: Automated Web Security Scanner

**Program:** IBM SkillsBuild Cyber Security 2026  
**Student name:** ____________________  
**Institution / batch:** ____________________  
**Submission date:** ____________________

## 1. Abstract
This Python project inspects a website's HTTP response for six common security headers, observes basic Cross-Origin Resource Sharing (CORS) response headers, checks whether the final URL uses HTTPS, and saves findings in JSON. It is a lightweight learning aid, not a complete security assessment.

## 2. Problem statement
Web applications can be deployed without important browser security headers or with CORS settings broader than intended. A repeatable script can help developers and learners collect basic configuration observations for manual review.

## 3. Objectives
- Check Strict-Transport-Security, Content-Security-Policy, X-Content-Type-Options, X-Frame-Options, Referrer-Policy, and Permissions-Policy.
- Observe Access-Control-Allow-Origin and Access-Control-Allow-Credentials.
- Check the final response URL's scheme.
- Produce structured findings and recommendations in JSON.

## 4. Technologies
- Python 3.10+
- Requests library
- Jupyter Notebook
- Python standard library (JSON, URL parsing, timestamps)

## 5. Methodology
1. Accept and validate an HTTP or HTTPS URL.
2. Make one GET request with a timeout and follow redirects.
3. Inspect selected security headers.
4. Observe basic CORS headers and provide contextual notes.
5. Check whether the final URL uses HTTPS.
6. Print results and save scan_report.json.

## 6. Expected output
The notebook reports the HTTP status, final URL, timestamp, header presence and observed values, CORS observations, and remediation guidance. Results depend on the target and must be captured during actual execution; no scan results are fabricated in this report.

## 7. Ethical use
Only test websites you own or are explicitly authorized to assess. The scanner does not exploit vulnerabilities, bypass authentication, brute-force credentials, or perform load testing.

## 8. Limitations
- Header presence alone cannot determine whether a website is secure.
- CORS behavior varies by route, origin, method, and credentials; this project does not exhaustively test variations.
- It does not crawl pages or test authenticated routes.
- Severity labels are triage hints and require manual validation.

## 9. Future enhancements
- Add cookie attribute checks.
- Add CSV/HTML report export.
- Add automated unit tests using mocked responses.
- Compare results against an approved security baseline.

## 10. Conclusion
This project demonstrates a repeatable Python-based workflow for checking a small set of web security configuration signals. It supports learning and manual review but is not a substitute for professional security testing.

## References
- MDN HTTP headers: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers
- MDN CORS: https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS
- OWASP Secure Headers Project: https://owasp.org/www-project-secure-headers/
- Requests documentation: https://requests.readthedocs.io/
