# Source Evidence

This portfolio was curated from collaborative work completed in the `dso-1` GitHub organization. The links below preserve the original team context, repository history, and individual contribution evidence.

## Core OJS project repositories

| Stage | Repository | Purpose |
|---|---|---|
| 1 | https://github.com/dso-1/Pertemuan-1-Kickoff-Case-1-Vulnerability-OJS | project kickoff, scope, rules of engagement, OJS lab initialization |
| 2 | https://github.com/dso-1/Pertemuan-2-Pemetaan-Attack-Surface-OJS | attack-surface mapping, entry points, DFD, CIA asset review, STRIDE threat model |
| 3 | https://github.com/dso-1/Pertemuan-3-Scanning-OJS-SAST-DAST-NEW | SAST, DAST, scan artifacts, manual review documentation, custom Semgrep rules |
| 4 | https://github.com/dso-1/Pertemuan-4-Analisis-OWASP-Risk-Scoring | OWASP mapping, CVSS calculation, risk register and risk matrix |
| 5 | https://github.com/dso-1/Pertemuan-5-Finalisasi-Laporan-Rekomendasi-Mitigasi | final report, risk register, mitigation material, PoC/demo references, final evidence bundle |

## Broader organization repositories relevant to the group's DevSecOps work

The organization contains additional project repositories beyond the five-stage OJS assessment:

| Repository | What it contains | Attribution treatment in this portfolio |
|---|---|---|
| https://github.com/dso-1/project | Jenkins pipeline, Docker deployment flow, Python app, Go Reserve `app-web`, CI/CD architecture material | referenced as broader team project; one presentation commit by `syifaniads` is linked below |
| https://github.com/dso-1/kelompok1_website | Go Reserve room-reservation application using TanStack Start, TypeScript, Prisma and PostgreSQL | referenced as team output; no `syifaniads` commits found through GitHub author filter |
| https://github.com/dso-1/sast-llm | LLM-based SAST vs Semgrep comparison project, vulnerable samples, custom rules, report generator | referenced as related team/course work; no `syifaniads` commits found through GitHub author filter |
| https://github.com/dso-1/.github | organization-level configuration | not treated as a standalone portfolio project |

See [`ORIGINAL_ARTIFACT_INVENTORY.md`](./ORIGINAL_ARTIFACT_INVENTORY.md) for a fuller explanation of these repository boundaries.

## Final report source

The original team repository contains the final PDF report:

https://github.com/dso-1/Pertemuan-5-Finalisasi-Laporan-Rekomendasi-Mitigasi/blob/main/Laporan%20Vulnerability%20Assessment%20%E2%80%94%20OJS_Kelompok%201.pdf

The portfolio documentation in this repository is a curated interpretation of that report and the original project repositories. Where the source report is inconsistent, this repository states the limitation rather than presenting an invented correction.

## Role evidence and clarification

The original kickoff repository includes the team-role document:

https://github.com/dso-1/Pertemuan-1-Kickoff-Case-1-Vulnerability-OJS/blob/main/2_Daftar_Anggota_Tim_dan_Peran.md

That artifact records **Syifani Adillah Salsabila** as **Security Engineer (SAST)** and separately labels another teammate as **Project Lead / Scrum Master**.

The portfolio owner states that she also served as **Ketua Kelompok / Group Lead** for team coordination. The recruiter-facing repository therefore presents the role as **Group Lead & Security Engineer (SAST)** while keeping the original role artifact linked here for transparency.

The distinction is intentional: the original role matrix is used as evidence of technical assignment, while the group-lead title describes team-coordination responsibility and is not used to claim individual authorship of all team output.

## Assigned issue evidence

### OJS initialization

An organization issue assigned to `syifaniads` documents the OJS initialization/setup task:

https://github.com/dso-1/Pertemuan-1-Kickoff-Case-1-Vulnerability-OJS/issues/8

The raw historical repository contains environment-specific setup details; the personal portfolio uses a sanitized setup summary in [`LAB_SETUP.md`](./LAB_SETUP.md).

### SAST / API / authentication analysis

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
| Broader DevSecOps project presentation | https://github.com/dso-1/project/commit/961df611d3c6fa2b708e93c054148c19379d5098 |

## Technical artifacts preserved in the personal portfolio

The portfolio includes a non-sensitive copy of the original team's PHP Semgrep rules:

[`../artifacts/semgrep/custom_rules.yaml`](../artifacts/semgrep/custom_rules.yaml)

The source artifact can be traced to the Meeting 3 SAST directory in the original organization repository.

## What the evidence supports

The linked organization history supports direct contribution across kickoff/setup, attack-surface documentation, SAST/DAST artifacts, risk-scoring work, final repository consolidation, and a presentation contribution in the broader DevSecOps project. The closed assigned issue provides especially clear evidence for API/admin review and authentication data-flow work.

Leadership responsibilities are represented separately from source-code authorship evidence. This keeps the portfolio honest about what GitHub proves directly versus what is stated as team-role context by the portfolio owner.

## Important sanitization note

Some historical organization artifacts contain lab-only infrastructure values and credentials in screenshots, text files, or historical commit metadata. Those values are not reproduced in this portfolio.

A reviewer who follows the original source history may therefore encounter material that is intentionally omitted here. This portfolio should be treated as the safer recruiter-facing version of the work.

## Evidence hierarchy used in this repository

When source materials disagree, the portfolio uses the following hierarchy:

1. detailed finding section of the final report for `VUL-001`–`VUL-015` names and CVSS values;
2. risk-register section for likelihood, impact, and business-priority values;
3. patch-verification appendix as evidence that re-testing occurred, but not as a reliable one-to-one finding-ID map;
4. original GitHub issues and commits for individual technical contribution proof;
5. portfolio-owner clarification for group-lead responsibility, kept distinct from direct authorship evidence.
