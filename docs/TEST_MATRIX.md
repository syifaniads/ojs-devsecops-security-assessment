# Test Matrix

This matrix summarizes representative areas covered by the broader team assessment. It includes both positive findings and negative validation results because a mature security review should record what was tested and what did **not** reproduce.

| Area | Test objective | Outcome represented in project |
|---|---|---|
| Login protection | resistance to repeated login attempts | protection gap documented in `VUL-001` |
| Login injection | determine whether selected credential fields behaved as SQL injection points | selected tests did not reproduce SQL injection |
| Authentication bypass | check whether login could be bypassed with malformed or missing inputs | selected tests did not reproduce bypass |
| Password reset | compare valid/invalid account behavior and repeated requests | no direct account enumeration observed; rate-limit weakness noted in working evidence |
| Registration | assess repeated automated registration controls | automation-resistance weakness noted in working evidence |
| User API | review unauthenticated data exposure | information disclosure documented in `VUL-002` |
| Submission API | test unauthenticated resource access / predictable identifiers | selected requests were denied; no IDOR reproduced in that path |
| Context API | test unauthenticated metadata access | selected requests were denied |
| Admin dashboard | test direct unauthenticated access | access redirected/blocked by authentication |
| Admin user management | compare privileged vs non-privileged access | RBAC behavior observed in selected tests |
| Search input | reflected XSS validation | selected payloads were encoded/sanitized; no XSS reproduced |
| Article / issue metadata | stored XSS validation | selected payloads were not executed in tested paths |
| Profile fields | stored XSS validation | selected payloads were not executed in tested path |
| Security headers | inspect framing, CSP, MIME-type protections | multiple hardening gaps documented |
| Session cookie | inspect browser security attributes | HttpOnly / SameSite gaps documented |
| Transport | review HTTPS enforcement | cleartext HTTP condition documented |
| Server exposure | review banners, directory indexing, ETag behavior | information-disclosure / hardening findings documented |
| Source diagnostics | search for exposed diagnostic functions | `phpinfo()` usage documented in `VUL-013` |
| Deserialization | identify unsafe deserialization primitives | potential risk documented in `VUL-014` |
| OS command execution | identify command-execution primitives | potential risk documented in `VUL-015` |

## Why negative results are included

A scanner-heavy portfolio can look shallow if every observation is presented as a vulnerability. Negative results demonstrate that the assessment also asked whether a suspected weakness was actually reproducible.

Examples from the working evidence include:

- denied access to protected API resources;
- working role-based access restrictions in selected admin flows;
- encoded/sanitized XSS test inputs;
- selected SQL injection tests that did not demonstrate injection behavior.

These results do not prove the entire application is secure in those categories. They only describe the specific paths and conditions tested during the lab exercise.

## Evidence caveat

Some exploratory working notes contain observations that were not promoted into the final canonical `VUL-001`–`VUL-015` list. This portfolio therefore keeps the canonical finding list separate from broader test coverage rather than mixing exploratory evidence into the final risk register.
