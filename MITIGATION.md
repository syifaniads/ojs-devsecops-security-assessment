# Mitigation Roadmap

The final team report organized remediation into short-, medium-, and long-term actions. This portfolio preserves that structure while grouping related controls into an engineering roadmap.

## 0–7 days — immediate controls

Focus: reduce exposure from the highest-priority findings and remove avoidable security weaknesses.

| Area | Priority actions | Related findings |
|---|---|---|
| Authentication | Add rate limiting, progressive backoff or lockout, and additional anti-automation controls | `VUL-001` |
| API access control | Require authentication and explicit role/authorization checks for sensitive endpoints; minimize returned user data | `VUL-002` |
| Transport security | Enforce HTTPS and prepare secure-cookie handling | `VUL-007`, `VUL-009`, `VUL-010` |
| Error handling | Disable detailed production error output and keep diagnostics server-side | `VUL-003` |
| Browser hardening | Add anti-framing, CSP, and MIME-sniffing protections appropriate to the application | `VUL-005`, `VUL-006`, `VUL-008` |
| Server hardening | Disable directory browsing, reduce version disclosure, review ETag behavior, remove exposed diagnostics | `VUL-004`, `VUL-011`, `VUL-012`, `VUL-013` |
| Dangerous code paths | Review deserialization and operating-system command call sites, especially trust boundaries and data flow | `VUL-014`, `VUL-015` |

## 7–30 days — platform hardening

Focus: make the security baseline consistent instead of relying on individual point fixes.

### Platform and dependency lifecycle

- move PHP and other runtime components to supported versions;
- update OJS and third-party dependencies using a tested upgrade path;
- document patch ownership and maintenance windows;
- add dependency and runtime version checks to routine security review.

### Session and authentication security

- regenerate session identifiers after privilege-changing events such as login;
- define a password policy appropriate to the environment;
- standardize cookie attributes;
- add monitoring for abnormal authentication activity.

### API security

- apply consistent authentication and authorization middleware/policies;
- implement least-privilege role checks;
- reduce unnecessary response data;
- log access to sensitive endpoints;
- apply rate limiting where abuse is plausible.

### Secure configuration management

- separate development, staging, and production settings;
- define a repeatable Apache/PHP/application hardening baseline;
- keep debug behavior disabled in production;
- review default settings before release.

### Logging and monitoring

- centralize security-relevant application and web-server logs;
- define alerting for repeated authentication failures and suspicious access patterns;
- retain logs long enough for investigation and audit needs.

## 30–90 days — secure engineering maturity

Focus: prevent recurrence through process and architecture.

### Secure SDLC / DevSecOps

- run SAST and DAST regularly in the delivery lifecycle;
- add security-focused code review for authentication, authorization, file handling, serialization, and command execution;
- track findings in a stable vulnerability-management workflow;
- require explicit closure evidence for high-risk items.

### Stronger identity protection

- introduce MFA for privileged roles where feasible;
- strengthen protections against credential stuffing and automated abuse;
- monitor privileged-account events.

### Continuous assurance

- perform periodic penetration testing and configuration review;
- review security headers and session behavior after significant changes;
- maintain a dependency and patch-management process;
- periodically re-evaluate threat models as functionality changes.

### Security governance

- document secure-coding expectations;
- define a vulnerability triage and disclosure process;
- train developers on recurring weakness classes observed in the assessment;
- assign remediation ownership and deadlines by risk.

## Recommended remediation record format

For professional use, each finding should be tracked with fields similar to:

```text
Finding ID
Asset / component
Technical severity
Business priority
Owner
Remediation action
Target date
Status
Retest method
Retest result
Evidence reference
```

The final report's patch-verification appendix shows why this matters: finding-number drift made some verification rows difficult to map back to the original findings. A stable remediation record prevents that ambiguity.
