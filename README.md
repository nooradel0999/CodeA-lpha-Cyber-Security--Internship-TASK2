# CodeA-lpha-Cyber-Security--Internship-TASK3
Task 3: Secure Coding Review
File: task3_secure_coding_review.py
A static code analysis tool that scans source code for common security vulnerabilities, maps them to CWE identifiers, and generates actionable reports.
Overview
This tool performs pattern-based vulnerability detection using regular expressions across multiple programming languages. It identifies insecure coding patterns that could lead to exploitation and provides remediation guidance.
Detected Vulnerabilities (12 Categories)
| Category                 | Severity     | CWE     | Description                                             |
| ------------------------ | ------------ | ------- | ------------------------------------------------------- |
| SQL Injection            | **CRITICAL** | CWE-89  | Unsanitized user input concatenated into SQL queries    |
| Command Injection        | **CRITICAL** | CWE-78  | User input passed to system shell commands              |
| Insecure Deserialization | **CRITICAL** | CWE-502 | Unsafe use of `pickle.loads()`, `yaml.load()`, `eval()` |
| Hardcoded Secrets        | **HIGH**     | CWE-798 | Passwords, API keys, tokens embedded in source code     |
| XSS Vulnerability        | **HIGH**     | CWE-79  | Unescaped user output in HTML/templates                 |
| Path Traversal           | **HIGH**     | CWE-22  | User-controlled file paths without validation           |
| SSRF Vulnerability       | **HIGH**     | CWE-918 | Server-Side Request Forgery via user URLs               |
| Weak Cryptographic Hash  | **MEDIUM**   | CWE-328 | Use of MD5 or SHA1 for security purposes                |
| Debug Mode Enabled       | **MEDIUM**   | CWE-489 | `DEBUG=True` in production environments                 |
| Insecure CORS            | **MEDIUM**   | CWE-942 | Wildcard `Access-Control-Allow-Origin: *`               |
| Insecure Random          | **LOW**      | CWE-338 | `random` module used for cryptographic purposes         |
| Hardcoded IP Addresses   | **LOW**      | CWE-547 | IP addresses hardcoded instead of configuration         |


Features

| Feature                 | Description                                           |
| ----------------------- | ----------------------------------------------------- |
| Multi-Language Support  | Python, JavaScript, PHP, Java, Go, Ruby               |
| CWE Mapping             | Every finding linked to MITRE CWE database            |
| Severity Classification | CRITICAL / HIGH / MEDIUM / LOW                        |
| Colored Console Output  | Readable, categorized vulnerability reports           |
| JSON Export             | Machine-readable reports for CI/CD integration        |
| Built-in Test App       | Auto-generates vulnerable Flask app for demonstration |


Features
