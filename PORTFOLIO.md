# Portfolio Summary

## OJS DevSecOps Security Assessment

**Role:** Group Lead (Ketua Kelompok) & Security Engineer (SAST)  
**Project type:** Collaborative application-security assessment  
**Environment:** Open Journal Systems (OJS) lab deployment  
**Year:** 2026

### One-line summary

Led a seven-person DevSecOps security-assessment team while contributing hands-on SAST and application-security analysis across attack-surface mapping, source review, manual validation, risk analysis, remediation planning, and re-testing of an OJS deployment.

### Portfolio description

Served as **Group Lead** and **Security Engineer (SAST)** for an end-to-end vulnerability assessment of Open Journal Systems in an authorized university lab. On the coordination side, I helped keep weekly assessment stages aligned, connected deliverables across SAST, DAST, risk analysis, and reporting, and supported consolidation into the final assessment package. On the technical side, my work focused on SAST/source review, REST API and admin attack-surface analysis, authentication data-flow analysis, vulnerability documentation, and selected assessment artifacts.

The project used Semgrep, OWASP ZAP, Nikto, SQLMap, Gobuster, WhatWeb, Burp Suite, Postman, and manual review, with CVSS v3.1 and likelihood/impact scoring used for risk analysis.

The final assessment documented issues across authentication, access control, security configuration, transport/session security, information disclosure, and security-sensitive source-code primitives. This repository presents the work conservatively: team output and individual contribution are separated, raw secrets are removed, and inconsistencies in the original report are explicitly documented.

### Skills demonstrated

- Security Project Leadership / Team Coordination
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

- [My contribution, leadership context, and commit proof](./CONTRIBUTIONS.md)
- [Assessment methodology](./METHODOLOGY.md)
- [Canonical findings](./FINDINGS.md)
- [Risk register](./RISK_REGISTER.md)
- [Mitigation roadmap](./MITIGATION.md)
- [Verification notes](./VERIFICATION.md)
- [Original team source repositories](./docs/SOURCE_EVIDENCE.md)

## CV-ready bullet options

**Leadership + security**

- Led a seven-person DevSecOps assessment team while contributing hands-on SAST, API/admin attack-surface analysis, authentication data-flow review, vulnerability documentation, and cross-stage coordination from scope definition through risk analysis and re-testing.

**Security-focused**

- Conducted SAST and manual source review for an OJS security assessment, analyzing API/admin attack surfaces and identifying information-disclosure, diagnostic-exposure, deserialization, and command-execution risk patterns; documented findings with OWASP/CWE mapping and CVSS-based severity.

**DevSecOps-focused**

- Coordinated and contributed to a multi-stage DevSecOps assessment workflow spanning reconnaissance, threat modeling, SAST/DAST, manual validation, risk scoring, mitigation planning, and re-testing using Semgrep, OWASP ZAP, Nikto, SQLMap, Gobuster, and related tooling.

**Concise portfolio card**

> **OJS DevSecOps Security Assessment** — Led a seven-person application-security assessment of an Open Journal Systems lab deployment covering attack-surface mapping, SAST/DAST, manual validation, CVSS risk analysis, mitigation, and re-testing. Role: Group Lead & Security Engineer (SAST).

## Interview discussion points

A technical reviewer may reasonably ask about:

- how I coordinated work across SAST, DAST, reporting, and risk-analysis tracks;
- how automated SAST findings were distinguished from confirmed exploitability;
- why CVSS severity and business remediation priority can differ;
- how API access-control findings were validated;
- how negative test results reduce false positives;
- how I handled inconsistencies between team artifacts during final consolidation;
- why stable finding IDs matter during remediation and re-testing;
- how secrets and sensitive lab evidence should be handled in public portfolios.

The supporting documents in this repository are structured so those questions can be answered from evidence rather than from an unverified project claim.
