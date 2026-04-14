---
name: sec-audit
description: Security audit — use when the user asks to audit security, check for vulnerabilities, review for OWASP issues, find security bugs, or harden the codebase.
---

# Security Audit

Audit the current file or project for security vulnerabilities.

Check every OWASP Top 10 category relevant to this codebase:
- A01 Broken Access Control
- A02 Cryptographic Failures (secrets in code, weak algos)
- A03 Injection (SQL, command, SSTI, SSRF, path traversal)
- A04 Insecure Design
- A05 Security Misconfiguration (CORS, headers, debug modes)
- A06 Vulnerable Components (outdated deps)
- A07 Auth failures (hardcoded creds, weak sessions)
- A08 Integrity failures (unsigned deps, unsafe deserialization)
- A09 Logging failures (logging secrets, insufficient logging)
- A10 SSRF

Output per finding:
- **Severity**: CRITICAL / HIGH / MEDIUM / LOW
- **Location**: file:line
- **Issue**: what the vulnerability is
- **Exploit**: how it could be abused
- **Fix**: exact code change
