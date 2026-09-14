# Original Organization Artifact Inventory

This page records the broader set of repositories I found in the original `dso-1` organization that are relevant to this portfolio and its surrounding DevSecOps coursework. It exists so a reviewer can distinguish the **core OJS assessment** from **related engineering projects** built by the same group.

## Core OJS security-assessment repositories

These five repositories form the primary assessment lifecycle represented by this portfolio:

| Stage | Original repository | Main purpose |
|---|---|---|
| 1 | [`dso-1/Pertemuan-1-Kickoff-Case-1-Vulnerability-OJS`](https://github.com/dso-1/Pertemuan-1-Kickoff-Case-1-Vulnerability-OJS) | Scope, Rules of Engagement, team roles, OJS lab initialization |
| 2 | [`dso-1/Pertemuan-2-Pemetaan-Attack-Surface-OJS`](https://github.com/dso-1/Pertemuan-2-Pemetaan-Attack-Surface-OJS) | Attack-surface mapping, critical assets, STRIDE threat modeling, DFDs |
| 3 | [`dso-1/Pertemuan-3-Scanning-OJS-SAST-DAST-NEW`](https://github.com/dso-1/Pertemuan-3-Scanning-OJS-SAST-DAST-NEW) | SAST, DAST, manual review, scanner outputs, custom Semgrep rules |
| 4 | [`dso-1/Pertemuan-4-Analisis-OWASP-Risk-Scoring`](https://github.com/dso-1/Pertemuan-4-Analisis-OWASP-Risk-Scoring) | OWASP mapping, CVSS calculation, risk register, risk matrix |
| 5 | [`dso-1/Pertemuan-5-Finalisasi-Laporan-Rekomendasi-Mitigasi`](https://github.com/dso-1/Pertemuan-5-Finalisasi-Laporan-Rekomendasi-Mitigasi) | Final report, mitigation recommendations, consolidated risk register, PoC/demo references |

## Related group engineering repositories

The organization also contains additional repositories that are **not part of the five-stage OJS assessment chain**, but are relevant to the broader DevSecOps project work completed by the group.

### `dso-1/project`

Repository: https://github.com/dso-1/project

This repository contains a broader DevSecOps engineering project with:

- a `Jenkinsfile` implementing container build, image transfer, VM deployment, database migration/seed, and post-deployment verification;
- a small Python application under `app/`;
- a larger `app-web/` application;
- Docker / Compose material;
- a multi-project CI/CD architecture presentation.

The `app-web/` application is documented as **Go Reserve**, a room-reservation platform using TanStack Start, Prisma, PostgreSQL, TypeScript, Tailwind CSS, and related tooling.

My GitHub account has a commit in this repository for the project presentation. This portfolio does **not** claim that I individually authored the complete application or CI/CD pipeline.

### `dso-1/kelompok1_website`

Repository: https://github.com/dso-1/kelompok1_website

This repository contains the group website/application source for **Go Reserve**, including:

- TanStack Start / TypeScript application code;
- Prisma/PostgreSQL database setup;
- authentication and role-specific dashboards;
- room and reservation management;
- testing/linting/tooling configuration.

No commits authored by `syifaniads` were found through GitHub's author filter in this repository, so it is referenced as **team output**, not as my individual source-code contribution.

### `dso-1/sast-llm`

Repository: https://github.com/dso-1/sast-llm

This is a separate hands-on security engineering project comparing **LLM-based SAST** with **Semgrep**. It includes:

- vulnerable Python and JavaScript samples;
- an LLM-based analyzer;
- custom Semgrep rules;
- a comparison/report generator;
- a master runner;
- an application/web component.

No commits authored by `syifaniads` were found through GitHub's author filter in this repository, so this repository is presented as **related team/course work**, not as an individually authored project.

## Organization infrastructure repository

`dso-1/.github` contains organization-level GitHub configuration and is not treated as a standalone portfolio project.

## Why everything is not copied into this repository

This repository is intentionally **curated instead of mirrored**.

Raw repositories contain large scanner outputs, screenshots, PDFs, lab-specific addresses, credentials/session material, and application code whose authorship is distributed across the team. Copying everything into a personal portfolio would:

1. weaken attribution;
2. expose unnecessary lab-specific information;
3. make the OJS assessment harder to review;
4. blur the boundary between my work and team output.

Therefore the personal portfolio keeps the security-assessment narrative, selected sanitized technical artifacts, contribution evidence, and links back to the original repositories where Git history remains authoritative.

## Portfolio boundary

The repository you are reading represents:

- my **group-lead / coordination role** as stated in this portfolio;
- my documented **Security Engineer (SAST)** role;
- OJS lab setup/documentation contributions that can be traced to my GitHub account;
- directly attributable API/authentication/SAST work;
- a curated representation of the team's complete OJS assessment lifecycle.

The related Go Reserve / CI/CD and LLM-vs-Semgrep projects are kept as references here because they demonstrate the broader scope of the group's DevSecOps work, but they should be treated as **separate portfolio case studies** if promoted as projects in their own right.
