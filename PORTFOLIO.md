# Portfolio Summary

## OJS DevSecOps Security Assessment

**Role:** Security Engineer (SAST)  
**Project type:** Collaborative application-security assessment  
**Environment:** Open Journal Systems (OJS) lab deployment  
**Year:** 2026

### One-line summary

Performed source-code and application-security analysis as part of a seven-person DevSecOps team, covering attack-surface mapping, SAST/DAST, manual validation, CVSS/risk analysis, remediation planning, and re-testing of an OJS deployment.

### Portfolio description

Contributed to an end-to-end vulnerability assessment of Open Journal Systems in an authorized university lab. My work focused on SAST and source review, REST API/admin attack-surface analysis, authentication data-flow analysis, vulnerability documentation, and assessment artifacts. The project used Semgrep, OWASP ZAP, Nikto, SQLMap, Gobuster, WhatWeb, Burp Suite, Postman, and manual review, with CVSS v3.1 and likelihood/impact scoring used for risk analysis.

The final assessment documented issues across authentication, access control, security configuration, transport/session security, information disclosure, and security-sensitive source-code primitives. This repository presents the work conservatively: team output and individual contribution are separated, raw secrets are removed, and inconsistencies in the original report are explicitly documented.

### Skills demonstrated

- Application Security Testing
- Static Application Security Testing (SAST)
- Dynamic Application Security Testing (DAST)
- Manual Source-Code Review
- Threat Modeling / Attack-Surface Mapping
- REST API Security Review
- Authentication and Authorization Analysis
- OWASP / CWE Mapping
- CVSS v3.1 Risk Assessment
- Security Misconfiguration Review
- Vulnerability Documentation
- Remediation Planning
- Re-testing / Verification
- Git / GitHub Collaborative Workflow

### Direct evidence

- [My contribution and commit proof](./CONTRIBUTIONS.md)
- [Assessment methodology](./METHODOLOGY.md)
- [Canonical findings](./FINDINGS.md)
- [Risk register](./RISK_REGISTER.md)
- [Mitigation roadmap](./MITIGATION.md)
- [Verification notes](./VERIFICATION.md)
- [Original team source repositories](./docs/SOURCE_EVIDENCE.md)

## CV-ready bullet options

**Security-focused**

- Conducted SAST and manual source review for an OJS security assessment, analyzing API/admin attack surfaces and identifying information-disclosure, diagnostic-exposure, deserialization, and command-execution risk patterns; documented findings with OWASP/CWE mapping and CVSS-based severity.

**DevSecOps-focused**

- Contributed to a seven-person DevSecOps assessment workflow spanning reconnaissance, threat modeling, SAST/DAST, manual validation, risk scoring, mitigation planning, and re-testing using Semgrep, OWASP ZAP, Nikto, SQLMap, Gobuster, and related tooling.

**Concise portfolio card**

> **OJS DevSecOps Security Assessment** — Application-security assessment of an Open Journal Systems lab deployment covering attack-surface mapping, SAST/DAST, manual validation, CVSS risk analysis, mitigation, and re-testing. Role: Security Engineer (SAST).

## Interview discussion points

A technical reviewer may reasonably ask about:

- how automated SAST findings were distinguished from confirmed exploitability;
- why CVSS severity and business remediation priority can differ;
- how API access-control findings were validated;
- how negative test results reduce false positives;
- why stable finding IDs matter during remediation and re-testing;
- how secrets and sensitive lab evidence should be handled in public portfolios.

The supporting documents in this repository are structured so those questions can be answered from evidence rather than from an unverified project claim.
