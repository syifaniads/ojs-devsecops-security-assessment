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

## Broader DevSecOps project repositories

The organization contains additional engineering work beyond the five-stage OJS assessment:

| Repository | What it contains | Portfolio treatment |
|---|---|---|
| https://github.com/dso-1/project | Jenkins pipeline, Docker deployment flow, Python app, Go Reserve `app-web`, CI/CD architecture material | part of the broader team ecosystem; direct `syifaniads` presentation commit linked below |
| https://github.com/dso-1/kelompok1_website | Go Reserve room-reservation application using TanStack Start, TypeScript, Prisma and PostgreSQL | linked as collaborative application work |
| https://github.com/dso-1/sast-llm | LLM-based SAST vs Semgrep experiment, vulnerable samples, custom rules, comparison tooling | linked as collaborative security-tooling work |
| https://github.com/dso-1/.github | organization-level configuration | not treated as a standalone portfolio project |

See [`PROJECT_ECOSYSTEM.md`](./PROJECT_ECOSYSTEM.md) for the relationship among these workstreams and [`ORIGINAL_ARTIFACT_INVENTORY.md`](./ORIGINAL_ARTIFACT_INVENTORY.md) for the repository boundary.

## Final report source

The original team repository contains the final PDF report:

https://github.com/dso-1/Pertemuan-5-Finalisasi-Laporan-Rekomendasi-Mitigasi/blob/main/Laporan%20Vulnerability%20Assessment%20%E2%80%94%20OJS_Kelompok%201.pdf

The portfolio documentation in this repository is a curated interpretation of that report and the original project repositories. Where the source report is inconsistent, this repository states the limitation rather than presenting an invented correction.

## Role evidence and clarification

The original kickoff repository includes the team-role document:

https://github.com/dso-1/Pertemuan-1-Kickoff-Case-1-Vulnerability-OJS/blob/main/2_Daftar_Anggota_Tim_dan_Peran.md

That artifact records **Syifani Adillah Salsabila** as **Security Engineer (SAST)** and separately labels another teammate as **Project Lead / Scrum Master**.

The portfolio owner states that she also served as **Ketua Kelompok / Group Lead** for team coordination. The recruiter-facing repository therefore presents the role as **Group Lead & Security Engineer (SAST)** while keeping the original role artifact linked here for transparency.

## Assigned issue evidence

### OJS initialization

An organization issue assigned to `syifaniads` documents the OJS initialization/setup task:

https://github.com/dso-1/Pertemuan-1-Kickoff-Case-1-Vulnerability-OJS/issues/8

The raw historical repository contains environment-specific setup details; the personal portfolio uses a sanitized setup summary in [`LAB_SETUP.md`](./LAB_SETUP.md).

### SAST / API / authentication analysis

A closed task assigned to `syifaniads` documents work on REST API/admin entry points and authentication data flow:

https://github.com/dso-1/Pertemuan-2-Pemetaan-Attack-Surface-OJS/issues/4

The issue scope includes REST API endpoint documentation, admin-panel endpoint documentation, review of unauthenticated admin-route access, authentication data-flow analysis, and DFD output.

## Direct commit evidence

The following commits are directly linked to the `syifaniads` GitHub identity:

| Stage | Evidence |
|---|---|
| Kickoff / scope | https://github.com/dso-1/Pertemuan-1-Kickoff-Case-1-Vulnerability-OJS/commit/874ff7749d8f36d134772071b55c22ec78b2905c |
| Attack-surface documentation | https://github.com/dso-1/Pertemuan-2-Pemetaan-Attack-Surface-OJS/commit/8635923836fa62d0d87e0e3ec9db1930855bf73d |
| SAST/DAST artifacts | https://github.com/dso-1/Pertemuan-3-Scanning-OJS-SAST-DAST-NEW/commit/83d4b4b55876f58278b0d3aa9d4b697f1d784abf |
| DAST checklist finalization | https://github.com/dso-1/Pertemuan-3-Scanning-OJS-SAST-DAST-NEW/commit/4631c1c59b78b2a58409aa167f7fb8826e785840 |
| Risk-scoring repository | https://github.com/dso-1/Pertemuan-4-Analisis-OWASP-Risk-Scoring/commit/70b77bfcdbdef4ef1384f35670d4c52d3eaf8fab |
| Final repository cross-linking | https://github.com/dso-1/Pertemuan-5-Finalisasi-Laporan-Rekomendasi-Mitigasi/commit/6a1085e82060f8acf873e7d7ffea039888d8eff3 |
| Multi-project CI/CD architecture presentation | https://github.com/dso-1/project/commit/961df611d3c6fa2b708e93c054148c19379d5098 |

The CI/CD presentation commit adds `Multi_Project_CI_CD_Architecture.pptx.pdf` to the broader DevSecOps repository.

## Shared-device Git history

The portfolio owner has clarified that some hands-on work was committed from a **shared / other team laptop**. On such machines, Git can record the laptop's existing local `user.name` / `user.email` rather than the actual person performing the work.

This has two consequences:

1. `author:syifaniads` can **undercount** the portfolio owner's contribution;
2. a commit recorded under another local identity cannot safely be reassigned to the portfolio owner from Git metadata alone.

The original organization history contains commits with local/unlinked Git identities as well as normal GitHub-linked identities. This repository therefore does not treat the author filter as the sole evidence source.

### Attribution method used here

For individual contribution claims, evidence is ranked as follows:

1. **direct GitHub identity** — commit linked to `syifaniads`;
2. **assigned issue/task** — organization issue explicitly assigned to `syifaniads`;
3. **report attribution** — final report names Syifani for a specific finding/output;
4. **documented responsibility / artifact ownership** — artifact aligns with an assigned role or deliverable;
5. **portfolio-owner clarification** — useful context for shared-device history, but not sufficient by itself to rewrite another person's commit attribution;
6. **team-level repository evidence** — demonstrates the broader project scope without implying solo authorship.

This approach is intentionally conservative. It protects the credibility of the portfolio while acknowledging that shared-device Git configuration makes the raw author graph incomplete.

## Technical artifacts preserved in the personal portfolio

The portfolio includes small non-sensitive examples from the original project:

- [`../artifacts/semgrep/custom_rules.yaml`](../artifacts/semgrep/custom_rules.yaml) — PHP Semgrep rules from the SAST workstream;
- [`../artifacts/ci-cd/Jenkinsfile.example`](../artifacts/ci-cd/Jenkinsfile.example) — sanitized representation of the Jenkins Docker deployment workflow.

Infrastructure addresses, usernames, credential IDs, runtime secrets, and environment-specific paths are replaced with placeholders.

## What the evidence supports

The organization history and project artifacts support direct technical contribution across kickoff/setup, attack-surface documentation, SAST/DAST artifacts, risk scoring, final repository consolidation, and CI/CD architecture presentation work. Assigned issues provide especially clear evidence for OJS initialization and API/admin/authentication analysis.

The wider organization also demonstrates exposure to application development, containerized deployment, Jenkins CI/CD, and SAST-tool experimentation. Those broader repositories are presented as **collaborative project context** unless a specific individual contribution has independent evidence.

## Important sanitization note

Some historical organization artifacts contain lab-only infrastructure values and credentials in screenshots, text files, or historical commit metadata. Those values are not reproduced in this portfolio.

A reviewer who follows the original source history may therefore encounter material that is intentionally omitted here. This portfolio should be treated as the safer recruiter-facing version of the work.

## Evidence hierarchy for inconsistent technical records

When source materials disagree on technical finding data, the portfolio uses the following hierarchy:

1. detailed finding section of the final report for `VUL-001`–`VUL-015` names and CVSS values;
2. risk-register section for likelihood, impact, and business-priority values;
3. patch-verification appendix as evidence that re-testing occurred, but not as a reliable one-to-one finding-ID map;
4. original GitHub issues and commits for individual technical contribution proof;
5. portfolio-owner clarification for leadership/shared-device context, kept distinct from direct authorship evidence.
