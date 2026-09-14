# Assessment Limitations

This repository is intentionally explicit about what the project can and cannot prove.

## Environment-specific results

The assessment was performed against a specific lab deployment of OJS 3.3.0-8 and its surrounding configuration. Findings influenced by server settings, runtime versions, enabled features, or local deployment choices may not apply to other OJS installations.

## Grey-box scope

The team had limited system understanding and source access. This improved analysis compared with a pure black-box test, but it was not equivalent to a full white-box product security review.

## No destructive testing

The rules of engagement excluded destructive actions and intentional denial-of-service activity. Therefore, availability impact and some high-risk exploitation paths were not fully exercised.

## Automated tooling limitations

Tools such as Semgrep, OWASP ZAP, Nikto, SQLMap, Gobuster, and WhatWeb can produce false positives, false negatives, or observations that require contextual validation. The project combined automated output with manual review, but not every scanner result received the same depth of validation.

## SAST finding confidence

Dangerous primitives such as `unserialize()` and operating-system command execution functions were identified in source. Their presence is security-relevant, but end-to-end exploitability depends on attacker-controlled input, validation, reachable code paths, authorization, and runtime conditions.

The portfolio therefore describes these as **potential** risks where the report did not prove a complete exploit chain.

## Report consistency

The final team report contains documentation inconsistencies, including:

- executive-summary severity counts that do not fully reconcile with detailed CVSS values;
- business-priority labels that differ from technical CVSS severity for some findings;
- patch-verification rows that reuse `VUL-xxx` identifiers for different issue names.

Rather than hide these issues, this portfolio documents them in [RISK_REGISTER.md](./RISK_REGISTER.md) and [VERIFICATION.md](./VERIFICATION.md).

## Portfolio curation

This repository does not duplicate the full OJS source tree or every raw artifact from the team organization repositories. The goal is to present evidence that is relevant to a recruiter or senior security reviewer while reducing accidental exposure of lab credentials and unrelated coursework artifacts.

Original source repositories and proof links are preserved in [docs/SOURCE_EVIDENCE.md](./docs/SOURCE_EVIDENCE.md).
