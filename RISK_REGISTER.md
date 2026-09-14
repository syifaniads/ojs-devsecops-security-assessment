# Risk Register

The original assessment used two different views of risk:

1. **CVSS v3.1** for technical severity.
2. **Likelihood × Impact** for remediation priority.

Keeping these separate is important. A finding may have a high technical CVSS score but a lower business priority if exploitability or likelihood is assessed differently in the lab context.

## Canonical risk table

| ID | Finding | CVSS | CVSS severity | Likelihood | Impact | Risk score | Report priority |
|---|---|---:|---|---:|---:|---:|---|
| `VUL-001` | Broken Authentication | 8.1 | High | 5 | 5 | 25 | High |
| `VUL-002` | User API Exposure | 6.5 | Medium | 5 | 4 | 20 | High |
| `VUL-003` | Error Disclosure | 5.3 | Medium | 4 | 3 | 12 | Medium |
| `VUL-004` | Directory Browsing | 3.7 | Low | 4 | 2 | 8 | Low |
| `VUL-005` | Missing X-Frame-Options | 4.3 | Medium | 3 | 3 | 9 | Low |
| `VUL-006` | Missing CSP | 5.4 | Medium | 4 | 3 | 12 | Medium |
| `VUL-007` | No HTTPS Enforcement | 5.3 | Medium | 4 | 4 | 16 | Medium |
| `VUL-008` | Missing X-Content-Type-Options | 4.3 | Medium | 3 | 3 | 9 | Low |
| `VUL-009` | Cookie Without HttpOnly | 4.3 | Medium | 4 | 3 | 12 | Medium |
| `VUL-010` | Cookie Without SameSite | 4.3 | Medium | 4 | 3 | 12 | Medium |
| `VUL-011` | Server Version Disclosure | 3.7 | Low | 3 | 2 | 6 | Low |
| `VUL-012` | ETag Information Leak | 3.7 | Low | 3 | 2 | 6 | Low |
| `VUL-013` | `phpinfo()` Exposure | 5.3 | Medium | 4 | 3 | 12 | Medium |
| `VUL-014` | Potential Insecure Deserialization | 7.3 | High | 3 | 5 | 15 | Medium |
| `VUL-015` | Potential Command Injection | 7.2 | High | 3 | 5 | 15 | Medium |

## Prioritization used by the team report

The report's mitigation ordering placed the issues approximately as follows:

1. `VUL-001` — Broken Authentication
2. `VUL-002` — API Exposure / Broken Access Control
3. `VUL-007` — No HTTPS Enforcement
4. `VUL-014` and `VUL-015` — potentially high-impact source-code risks
5. `VUL-003`, `VUL-006`, `VUL-009`, `VUL-010`, `VUL-013` — misconfiguration / disclosure group
6. remaining lower-priority hardening issues

## Why the counts do not perfectly match the executive summary

The original report states an executive-summary distribution of **0 Critical, 2 High, 7 Medium, 6 Low**. That distribution does not exactly reconcile with either:

- the detailed CVSS values in `VUL-001`–`VUL-015`, or
- the later likelihood × impact priority table.

This portfolio intentionally does **not** invent a corrected count. Instead:

- the detailed finding pages remain the source for CVSS values;
- the risk-register table above preserves the likelihood/impact scores and priorities shown later in the report;
- the discrepancy is treated as a documentation-quality lesson.

## Professional takeaway

For a production security program, each finding should have one stable identifier and separately tracked fields for:

- technical severity;
- exploitability confidence;
- asset/business impact;
- remediation owner;
- target date;
- remediation status;
- retest evidence.

That structure prevents severity and status drift across executive summaries, technical findings, and verification reports.
