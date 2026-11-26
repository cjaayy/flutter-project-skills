---
name: security-hygiene
description: Prevent credential leaks, injection flaws, and exposed endpoints. Use when configuring authentication, environment variables, file uploads, public forms, or headers.
---

# Security Hygiene

## Checklist
1. **Zero Hardcoded Secrets:** Load all API keys, tokens, and connection strings from environment variables. Ensure .env files are gitignored.
2. **Protect Public Surfaces:** Add rate limiting, CAPTCHA/Turnstile verification, and strict file-type/size validation on public forms and upload routes.
3. **Sanitize & Escape:** Never trust client-supplied HTML, file paths, or redirect URLs. Enforce strict Content Security Policy (CSP) headers where applicable.
4. **Verify Auth on Every Mutation:** Check session validity and user ownership on the server side for every write operation.
