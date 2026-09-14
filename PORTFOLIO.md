# Portfolio Summary

## OJS DevSecOps Security Assessment

**Role:** Group Lead (Ketua Kelompok) & Security Engineer (SAST)  
**Project type:** Collaborative application-security / DevSecOps project  
**Environment:** Open Journal Systems (OJS) authorized lab + related group engineering workstreams  
**Year:** 2026

### One-line summary

Led a seven-person DevSecOps security-assessment team while contributing hands-on SAST and application-security analysis across attack-surface mapping, source review, manual validation, risk analysis, remediation planning, and re-testing of an OJS deployment, within a broader group project that also included containerized application delivery, Jenkins CI/CD, Go Reserve, and SAST-tool experimentation.

### Portfolio description

Served as **Group Lead** and **Security Engineer (SAST)** for an end-to-end vulnerability assessment of Open Journal Systems in an authorized university lab. On the coordination side, I helped keep weekly assessment stages aligned, connected deliverables across SAST, DAST, risk analysis, application work, and reporting, and supported consolidation into the final assessment package. On the technical side, my work focused on SAST/source review, REST API and admin attack-surface analysis, authentication data-flow analysis, vulnerability documentation, and selected assessment artifacts.

The OJS assessment used Semgrep, OWASP ZAP, Nikto, SQLMap, Gobuster, WhatWeb, Burp Suite, Postman, and manual review, with CVSS v3.1 and likelihood/impact scoring used for risk analysis.

The wider `dso-1` project ecosystem also includes:

- **Go Reserve** — TanStack Start / TypeScript / Prisma / PostgreSQL room-reservation application;
- **Jenkins + Docker CI/CD** — container build, transfer, remote VM deployment, database setup, and post-deploy verification;
- **LLM vs Semgrep SAST** — a hands-on comparison of contextual LLM analysis and rule-based static analysis.

A recruiter can inspect the complete ecosystem in [`docs/PROJECT_ECOSYSTEM.md`](./docs/PROJECT_ECOSYSTEM.md).

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
- Semgrep Custom Rules
- Jenkins CI/CD Concepts
- Dockerized Deployment Workflow
- Application Delivery / Post-deploy Verification
- LLM-assisted vs Rule-based SAST Evaluation
- Git / GitHub Collaborative Workflow

### Direct evidence

- [My contribution, leadership context, and commit proof](./CONTRIBUTIONS.md)
- [Assessment methodology](./METHODOLOGY.md)
- [Canonical findings](./FINDINGS.md)
- [Risk register](./RISK_REGISTER.md)
- [Mitigation roadmap](./MITIGATION.md)
- [Verification notes](./VERIFICATION.md)
- [Complete DevSecOps project ecosystem](./docs/PROJECT_ECOSYSTEM.md)
- [Original team source repositories and attribution model](./docs/SOURCE_EVIDENCE.md)
- [Sanitized Semgrep artifact](./artifacts/semgrep/custom_rules.yaml)
- [Sanitized Jenkins pipeline example](./artifacts/ci-cd/Jenkinsfile.example)

## Contribution-history caveat

Some project work was performed from a shared / other team laptop. Git therefore did not always record the work under the `syifaniads` identity. The portfolio uses direct commits, assigned issues, report attribution, documented responsibilities, and project artifacts together rather than treating the Git author filter as a complete contribution counter.

For credibility, a commit recorded under another person's/local identity is not automatically relabeled as mine without additional evidence. See [`CONTRIBUTIONS.md`](./CONTRIBUTIONS.md) and [`docs/SOURCE_EVIDENCE.md`](./docs/SOURCE_EVIDENCE.md).

## CV-ready bullet options

**Leadership + security**

- Led a seven-person DevSecOps assessment team while contributing hands-on SAST, API/admin attack-surface analysis, authentication data-flow review, vulnerability documentation, and cross-stage coordination from scope definition through risk analysis and re-testing.

**Security-focused**

- Conducted SAST and manual source review for an OJS security assessment, analyzing API/admin attack surfaces and identifying information-disclosure, diagnostic-exposure, deserialization, and command-execution risk patterns; documented findings with OWASP/CWE mapping and CVSS-based severity.

**DevSecOps-focused**

- Coordinated a multi-workstream DevSecOps project spanning OJS vulnerability assessment, SAST/DAST, CVSS risk treatment, Docker/Jenkins delivery workflows, and security-tool experimentation, while contributing directly to SAST/API analysis and CI/CD architecture documentation.

**Concise portfolio card**

> **OJS DevSecOps Security Assessment** — Led a seven-person application-security assessment of an Open Journal Systems lab deployment covering attack-surface mapping, SAST/DAST, manual validation, CVSS risk analysis, mitigation, and re-testing, within a wider DevSecOps project ecosystem. Role: Group Lead & Security Engineer (SAST).

## Interview discussion points

A technical reviewer may reasonably ask about:

- how I coordinated work across SAST, DAST, application, deployment, reporting, and risk-analysis tracks;
- how automated SAST findings were distinguished from confirmed exploitability;
- why CVSS severity and business remediation priority can differ;
- how API access-control findings were validated;
- how negative test results reduce false positives;
- how I handled inconsistencies between team artifacts during final consolidation;
- why stable finding IDs matter during remediation and re-testing;
- how the Jenkins/Docker delivery flow was structured;
- why LLM-based and rule-based SAST can be complementary;
- how shared-device Git identities can complicate contribution attribution;
- how secrets and sensitive lab evidence should be handled in public portfolios.

The supporting documents in this repository are structured so those questions can be answered from evidence rather than from an unverified project claim.
