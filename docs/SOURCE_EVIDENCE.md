# Source Evidence

This portfolio was curated from collaborative work completed in the `dso-1` GitHub organization. The links below preserve the original team context, repository history, and individual contribution evidence.

## Original project repositories

| Stage | Repository | Purpose |
|---|---|---|
| 1 | https://github.com/dso-1/Pertemuan-1-Kickoff-Case-1-Vulnerability-OJS | project kickoff, scope, rules of engagement, initial environment documentation |
| 2 | https://github.com/dso-1/Pertemuan-2-Pemetaan-Attack-Surface-OJS | attack-surface mapping, entry points, DFD, CIA asset review, STRIDE threat model |
| 3 | https://github.com/dso-1/Pertemuan-3-Scanning-OJS-SAST-DAST-NEW | SAST, DAST, scan artifacts, manual review documentation |
| 4 | https://github.com/dso-1/Pertemuan-4-Analisis-OWASP-Risk-Scoring | OWASP-oriented risk scoring and analysis |
| 5 | https://github.com/dso-1/Pertemuan-5-Finalisasi-Laporan-Rekomendasi-Mitigasi | final report, risk register, mitigation material, and final evidence bundle |

## Final report source

The original team repository contains the final PDF report:

https://github.com/dso-1/Pertemuan-5-Finalisasi-Laporan-Rekomendasi-Mitigasi/blob/main/Laporan%20Vulnerability%20Assessment%20%E2%80%94%20OJS_Kelompok%201.pdf

The portfolio documentation in this repository is a curated interpretation of that report and the original project repositories. Where the source report is inconsistent, this repository states the limitation rather than presenting an invented correction.

## Team-role evidence

The original kickoff repository includes the team-role document:

https://github.com/dso-1/Pertemuan-1-Kickoff-Case-1-Vulnerability-OJS/blob/main/2_Daftar_Anggota_Tim_dan_Peran.md

It records **Syifani Adillah Salsabila** as **Security Engineer (SAST)**.

## Assigned issue evidence

A closed task assigned to `syifaniads` documents work on REST API/admin entry points and authentication data flow:

https://github.com/dso-1/Pertemuan-2-Pemetaan-Attack-Surface-OJS/issues/4

The issue scope includes:

- REST API endpoint documentation;
- admin-panel endpoint documentation;
- review of unauthenticated admin-route access;
- authentication data-flow analysis;
- DFD output.

## Selected commit evidence

The following commits are examples of work authored under the `syifaniads` GitHub account:

| Stage | Evidence |
|---|---|
| Kickoff / scope | https://github.com/dso-1/Pertemuan-1-Kickoff-Case-1-Vulnerability-OJS/commit/874ff7749d8f36d134772071b55c22ec78b2905c |
| Attack-surface documentation | https://github.com/dso-1/Pertemuan-2-Pemetaan-Attack-Surface-OJS/commit/8635923836fa62d0d87e0e3ec9db1930855bf73d |
| SAST/DAST artifacts | https://github.com/dso-1/Pertemuan-3-Scanning-OJS-SAST-DAST-NEW/commit/83d4b4b55876f58278b0d3aa9d4b697f1d784abf |
| DAST checklist finalization | https://github.com/dso-1/Pertemuan-3-Scanning-OJS-SAST-DAST-NEW/commit/4631c1c59b78b2a58409aa167f7fb8826e785840 |
| Risk-scoring repository | https://github.com/dso-1/Pertemuan-4-Analisis-OWASP-Risk-Scoring/commit/70b77bfcdbdef4ef1384f35670d4c52d3eaf8fab |
| Final repository cross-linking | https://github.com/dso-1/Pertemuan-5-Finalisasi-Laporan-Rekomendasi-Mitigasi/commit/6a1085e82060f8acf873e7d7ffea039888d8eff3 |

## Important sanitization note

Some historical organization artifacts contain lab-only infrastructure values and credentials in screenshots, text files, or historical commit metadata. Those values are not reproduced in this portfolio.

A reviewer who follows the original source history may therefore encounter material that is intentionally omitted here. This portfolio should be treated as the safer recruiter-facing version of the work.

## Evidence hierarchy used in this repository

When source materials disagree, the portfolio uses the following hierarchy:

1. detailed finding section of the final report for `VUL-001`–`VUL-015` names and CVSS values;
2. risk-register section for likelihood, impact, and business-priority values;
3. patch-verification appendix as evidence that re-testing occurred, but not as a reliable one-to-one finding-ID map;
4. original GitHub issues and commits for individual contribution proof.
