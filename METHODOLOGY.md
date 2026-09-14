# Methodology

This portfolio preserves the methodology described in the team assessment while presenting it in a cleaner engineering format.

## 1. Scope and rules of engagement

The assessment targeted **Open Journal Systems (OJS) 3.3.0-8** in a controlled lab environment. The tested stack included Apache, PHP, and MariaDB/MySQL.

The scope covered:

- public application endpoints;
- login, password reset, registration, and session behavior;
- REST API endpoints;
- submission and file-upload workflows;
- administrative routes;
- server configuration and security headers;
- selected third-party libraries and application dependencies;
- selected source-code paths relevant to authorization, database access, file handling, plugins, and rendering.

Testing constraints included:

- no intentional denial-of-service activity;
- no destructive data modification;
- no full extraction of sensitive data;
- grey-box testing with limited system understanding;
- work conducted under an authorized university lab context.

## 2. Reconnaissance and enumeration

Reconnaissance was used to understand the exposed application and server surface before deeper testing.

Tools documented in the assessment included:

- **WhatWeb** — technology fingerprinting;
- **Nmap** — service and port discovery during the practical workflow;
- **Gobuster** — directory and file enumeration;
- HTTP header inspection — server and application-version exposure review.

The goal was to identify candidate entry points rather than treat every discovered endpoint as a vulnerability.

## 3. Attack-surface mapping and threat modeling

The team documented application entry points across authentication, file upload, user-controlled input, REST APIs, and administrative functionality.

Threat modeling used a structured approach that included:

- attack-surface diagrams;
- critical-asset identification using confidentiality, integrity, and availability considerations;
- STRIDE-oriented threat analysis;
- authentication data-flow analysis.

A simplified portfolio view is available in [docs/ARCHITECTURE.md](./docs/ARCHITECTURE.md).

## 4. Static Application Security Testing (SAST)

### Automated analysis

**Semgrep** was used to identify dangerous or security-sensitive code patterns, including:

- `unserialize()` usage;
- command execution primitives such as `exec()` / `popen()` / shell execution;
- `eval()` usage;
- file-manipulation primitives;
- patterns potentially relevant to injection or unsafe deserialization.

The assessment also references **PHP_CodeSniffer / security-audit style review** for PHP quality and insecure coding patterns.

### Manual source review

Manual review focused on historically sensitive areas such as:

- authorization policies;
- database access objects;
- file-management and upload logic;
- generic plugins;
- template rendering.

The important distinction used in this portfolio is:

> A dangerous function call is not automatically a confirmed exploitable vulnerability. Exploitability depends on data flow, attacker control, validation, authorization, and runtime context.

This is why source findings such as deserialization and command execution are described as **potential** where the report did not prove an end-to-end exploit path.

## 5. Dynamic Application Security Testing (DAST)

The dynamic testing stack included:

- **OWASP ZAP** — passive/active web checks and response-header analysis;
- **Nikto** — server misconfiguration and information-disclosure checks;
- **SQLMap** — selected SQL injection validation;
- **Burp Suite Intruder** — manual authentication/brute-force testing;
- **Postman / curl / browser** — endpoint behavior, authorization, and manual validation.

Dynamic checks covered areas such as:

- authentication protection;
- API authorization;
- security headers;
- cookie flags;
- HTTPS enforcement;
- directory browsing;
- server/version disclosure;
- XSS behavior;
- IDOR/access-control behavior;
- file-upload restrictions.

## 6. Manual validation

Automated findings were not intended to stand alone. The assessment used manual checks to verify whether observed behavior was meaningful.

Examples from the report include:

- testing API endpoints with and without authentication;
- checking whether predictable IDs resulted in unauthorized data access;
- testing whether XSS payloads were executed or encoded;
- evaluating upload controls through multiple application workflows;
- checking admin routes with unauthenticated or lower-privilege sessions;
- reviewing whether SQL injection payloads changed application behavior.

## 7. Risk analysis

The report used two related but distinct concepts:

### Technical severity

Detailed findings include **CVSS v3.1** vectors and base scores.

### Business priority

The risk register also used an OWASP-style model:

```text
Risk = Likelihood × Impact
```

This portfolio keeps those dimensions separate because a technical severity score and an organizational remediation priority are not necessarily the same thing.

See [RISK_REGISTER.md](./RISK_REGISTER.md).

## 8. Mitigation planning

Recommendations were organized into three horizons:

- **0–7 days** — immediate/high-priority hardening;
- **7–30 days** — medium-term security improvements;
- **30–90 days** — strategic secure-development and operational improvements.

See [MITIGATION.md](./MITIGATION.md).

## 9. Verification / re-testing

The final report describes re-testing using the same or comparable tools to check whether recommended controls were effective. This included automated re-scanning, exploit re-testing, and configuration validation.

Because the report's patch-verification appendix uses finding IDs that do not consistently match the canonical detailed findings, this portfolio treats that appendix as **team verification evidence with an ID-mapping limitation**, rather than silently relabeling it.

See [VERIFICATION.md](./VERIFICATION.md).

## 10. Standards and references used by the project

The team report cites or aligns its process with:

- OWASP Testing Guide;
- OWASP Top 10 / OWASP API security concepts;
- PTES (Penetration Testing Execution Standard);
- CVSS v3.1;
- CWE identifiers for individual findings.

This repository is a portfolio representation of that assessment, not an independent security certification of OJS as a product.
