# Findings

This page consolidates the 15 canonical finding IDs from the detailed findings section of the final team report. Sensitive lab values and raw exploitation details are intentionally omitted.

> The original report contains inconsistencies between its executive-summary counts, detailed CVSS severities, risk-priority table, and later patch-verification numbering. This portfolio uses the detailed `VUL-001`–`VUL-015` section as the canonical naming source and documents the mismatch instead of silently rewriting the record.

## Consolidated findings

| ID | Finding | OWASP category | CWE | CVSS v3.1 | Technical severity | Attributed discoverer |
|---|---|---|---|---:|---|---|
| `VUL-001` | Broken Authentication — Brute Force Login | A07 Identification & Authentication Failures | CWE-307 | 8.1 | High | Scorpian |
| `VUL-002` | Information Disclosure — User API Exposure | A01 Broken Access Control | CWE-200 | 6.5 | Medium | Syifani |
| `VUL-003` | Application Error Disclosure / Debug Info | A05 Security Misconfiguration | CWE-209 | 5.3 | Medium | Omar |
| `VUL-004` | Directory Browsing Enabled | A05 Security Misconfiguration | CWE-548 | 3.7 | Low | Ian |
| `VUL-005` | Missing X-Frame-Options / Clickjacking Exposure | A05 Security Misconfiguration | CWE-1021 | 4.3 | Medium | Ian |
| `VUL-006` | Missing Content-Security-Policy | A05 Security Misconfiguration | CWE-693 | 5.4 | Medium | Omar |
| `VUL-007` | HTTP Only / No HTTPS Enforcement | A02 Cryptographic Failures | CWE-319 | 5.3 | Medium | Omar |
| `VUL-008` | Missing X-Content-Type-Options | A05 Security Misconfiguration | CWE-693 | 4.3 | Medium | Omar |
| `VUL-009` | Session Cookie Without HttpOnly | A02 Cryptographic Failures | CWE-1004 | 4.3 | Medium | Ian |
| `VUL-010` | Session Cookie Without SameSite | A02 Cryptographic Failures | CWE-1275 | 4.3 | Medium | Omar |
| `VUL-011` | Server Version Disclosure | A05 Security Misconfiguration | CWE-200 | 3.7 | Low | Omar |
| `VUL-012` | ETag Information Leak | A05 Security Misconfiguration | CWE-200 | 3.7 | Low | Omar |
| `VUL-013` | `phpinfo()` Exposure | A05 Security Misconfiguration | CWE-200 | 5.3 | Medium | Syifani |
| `VUL-014` | Potential Insecure Deserialization | A08 Software & Data Integrity Failures | CWE-502 | 7.3 | High | Syifani |
| `VUL-015` | Potential Command Injection | A03 Injection | CWE-78 | 7.2 | High | Syifani |

## Assessment themes

The findings group naturally into several recurring themes:

- **Authentication and access control** — repeated-login protection and user-data exposure.
- **Transport and session security** — HTTPS enforcement and cookie attributes.
- **Server hardening** — directory indexing, response headers, version disclosure, and diagnostic exposure.
- **Source-code risk** — dangerous deserialization and operating-system command primitives that require data-flow validation before exploitability can be confirmed.

## Important interpretation notes

### Scanner observation vs confirmed vulnerability

The project combined automated findings with manual review. A security-sensitive function or missing header is not automatically equivalent to an end-to-end exploit. This portfolio therefore distinguishes between confirmed runtime behavior and potential source-code risk.

### VUL-014 and VUL-015

The report assigns CVSS 7.3 and 7.2 respectively, but the source evidence shown in the report primarily demonstrates discovery of dangerous primitives in code. Exploitability depends on whether attacker-controlled input reaches those sinks and whether the runtime context makes exploitation possible. The wording **potential** is retained for that reason.

### Negative results

The larger assessment also documented cases where suspected issues were not reproduced, including selected SQL injection, XSS, API IDOR, unauthorized-admin access, and plugin-upload scenarios. Those negative results are useful because they show that the workflow included validation rather than treating every observation as exploitable.

For prioritization, see [RISK_REGISTER.md](./RISK_REGISTER.md). For remediation, see [MITIGATION.md](./MITIGATION.md).
