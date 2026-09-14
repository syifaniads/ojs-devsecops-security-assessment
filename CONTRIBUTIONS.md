# My Contribution

This assessment was completed by **Kelompok 1**, a seven-person DevSecOps team. My documented team role was **Security Engineer (SAST)**. This page separates my contribution from the wider team output so that the repository can be evaluated as a portfolio artifact without implying solo authorship.

## Responsibilities I can substantiate

My work covered the following areas:

- static source-code review using **Semgrep** and manual inspection;
- REST API and admin-panel attack-surface analysis;
- authentication data-flow analysis;
- documentation of selected findings and technical risk;
- contributions to SAST/DAST documentation and checklist completion;
- contributions to the final risk/reporting repository.

## Findings attributed to me in the final report

| ID | Finding | Assessment type | Report attribution |
|---|---|---|---|
| `VUL-002` | Information Disclosure — User API Exposure | Manual / API review | Syifani |
| `VUL-013` | `phpinfo()` Exposure | SAST | Syifani |
| `VUL-014` | Potential Insecure Deserialization | SAST | Syifani |
| `VUL-015` | Potential Command Injection (`exec` / `popen`) | SAST | Syifani |

The wording **potential** is deliberate for source-code findings where a dangerous primitive was identified but exploitability depended on whether attacker-controlled input could reach the sink.

## Verifiable task evidence

A particularly clear task record is the closed organization issue:

- **[SAST] Document REST API & Admin Entry Points + Authentication Data Flow Diagram**  
  https://github.com/dso-1/Pertemuan-2-Pemetaan-Attack-Surface-OJS/issues/4

The issue was assigned to `syifaniads` and closed as completed. Its expected work included documenting REST API/admin endpoint groups, reviewing unauthenticated access, and producing an authentication-flow DFD.

## Verifiable commit evidence

Selected commits authored by `syifaniads` in the original team repositories:

- Meeting 1 — scope/documentation:  
  https://github.com/dso-1/Pertemuan-1-Kickoff-Case-1-Vulnerability-OJS/commit/874ff7749d8f36d134772071b55c22ec78b2905c
- Meeting 2 — final step-by-step documentation:  
  https://github.com/dso-1/Pertemuan-2-Pemetaan-Attack-Surface-OJS/commit/8635923836fa62d0d87e0e3ec9db1930855bf73d
- Meeting 3 — uploaded SAST/DAST artifacts:  
  https://github.com/dso-1/Pertemuan-3-Scanning-OJS-SAST-DAST-NEW/commit/83d4b4b55876f58278b0d3aa9d4b697f1d784abf
- Meeting 3 — finalized DAST checklist:  
  https://github.com/dso-1/Pertemuan-3-Scanning-OJS-SAST-DAST-NEW/commit/4631c1c59b78b2a58409aa167f7fb8826e785840
- Meeting 4 — risk-scoring repository contribution:  
  https://github.com/dso-1/Pertemuan-4-Analisis-OWASP-Risk-Scoring/commit/70b77bfcdbdef4ef1384f35670d4c52d3eaf8fab
- Meeting 5 — final repository cross-linking:  
  https://github.com/dso-1/Pertemuan-5-Finalisasi-Laporan-Rekomendasi-Mitigasi/commit/6a1085e82060f8acf873e7d7ffea039888d8eff3

For broader history, GitHub's author filter can be used on each original repository.

## Team attribution

The original team role document lists:

| Role | Team coverage |
|---|---|
| Project Lead / Scrum Master | coordination and final review |
| Security Engineers — SAST | source analysis and SAST activities |
| Security Engineers — DAST | dynamic scanning and validation |
| Documentation & Reporting | final reporting, risk and mitigation documentation |

This portfolio therefore distinguishes between **team findings** and **my directly attributable work** instead of presenting every artifact as individually authored.

## What I would improve in a production assessment

If repeating the engagement in a professional environment, I would strengthen the evidence chain by assigning a stable finding ID from discovery through remediation, storing sanitized raw tool output with hashes, separating scanner observations from manually validated vulnerabilities, and tracking each mitigation through an explicit retest result. Those improvements are reflected in how this portfolio repository is organized.
