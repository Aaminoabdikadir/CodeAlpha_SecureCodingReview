# Secure Coding Review Report - CodeAlpha Internship

## Overview
This project presents a security code review of a sample authentication module, identifying common vulnerabilities such as hardcoded credentials and demonstrating how to remediate them following secure coding best practices.

## Identified Vulnerabilities & Findings
1. **Hardcoded Credentials (CWE-798):**
   - **Issue:** Storing plaintext passwords directly in the source code exposes sensitive administrative access if the repository is leaked.
   - **Risk:** High. Unauthorized access to critical systems.
2. **Lack of Input Hashing / Salting:**
   - **Issue:** Comparing passwords in plain text instead of cryptographic hashes.

## Remediation & Best Practices (Secure Code)
- Removed hardcoded credentials from the source code.
- Implemented environment variables (`os.environ`) and cryptographic hashing (`hashlib`) to securely manage authentication data.