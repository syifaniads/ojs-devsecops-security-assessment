# Original Organization Artifact Inventory

This page records the broader set of repositories in the original `dso-1` organization that are relevant to this portfolio and its surrounding DevSecOps project. It exists so a reviewer can distinguish the **core OJS assessment** from **related engineering workstreams** built by the same group.

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

A direct `syifaniads` commit adds the multi-project CI/CD architecture presentation:

https://github.com/dso-1/project/commit/961df611d3c6fa2b708e93c054148c19379d5098

This portfolio does not claim that one commit proves sole authorship of the full application or deployment pipeline. Broader contribution is represented using the evidence model described below.

### `dso-1/kelompok1_website`

Repository: https://github.com/dso-1/kelompok1_website

This repository contains the group application source for **Go Reserve**, including:

- TanStack Start / TypeScript application code;
- Prisma/PostgreSQL database setup;
- authentication and role-specific dashboards;
- room and reservation management;
- testing/linting/tooling configuration.

A GitHub author filter does not show commits linked directly to `syifaniads` in this repository. However, the portfolio owner has clarified that some hands-on work was committed from a **shared or other team laptop**, where the local Git identity could belong to that device's existing configuration. Therefore the absence of `author:syifaniads` is **not treated as proof of non-contribution**.

Until a particular shared-device commit can be independently mapped to the portfolio owner, the repository is presented as collaborative group work rather than individually re-attributed source code.

### `dso-1/sast-llm`

Repository: https://github.com/dso-1/sast-llm

This is a separate hands-on security engineering project comparing **LLM-based SAST** with **Semgrep**. It includes:

- vulnerable Python and JavaScript samples;
- an LLM-based analyzer;
- custom Semgrep rules;
- a comparison/report generator;
- a master runner;
- a web/application component.

A GitHub author filter likewise does not expose the complete contribution picture for `syifaniads`. The repository history includes local/unlinked Git identities, which is consistent with work being committed from machines whose Git configuration was not tied to the individual contributor's GitHub account.

For credibility, this portfolio records the project as part of the team's wider security-engineering work unless a specific commit or artifact has stronger individual evidence.

## Organization infrastructure repository

`dso-1/.github` contains organization-level GitHub configuration and is not treated as a standalone portfolio project.

## Shared-device attribution caveat

Git records the configured `user.name` and `user.email` on the machine that creates a commit. On a shared laptop, this can produce a historical author identity that differs from the person who actually performed the work.

For that reason, this portfolio does not use `author:syifaniads` as a complete measure of contribution. It combines:

1. direct commits linked to `syifaniads`;
2. assigned GitHub issues/tasks;
3. report-level finding attribution;
4. documented role and artifact ownership;
5. portfolio-owner clarification for shared-device context;
6. team-level repository history.

At the same time, a commit under another identity is **not automatically relabeled** as Syifani's. A specific mapping should have an independent basis, such as a known shared-laptop identity, task record, artifact ownership, or other contemporaneous evidence.

## Why everything is not copied into this repository

This repository is intentionally **curated instead of mirrored**.

Raw repositories contain large scanner outputs, screenshots, PDFs, lab-specific addresses, credentials/session material, and application code whose authorship is distributed across the team. Copying everything into a personal portfolio would:

1. weaken attribution;
2. expose unnecessary lab-specific information;
3. make the OJS assessment harder to review;
4. blur the boundary between individual work and team output.

Therefore the personal portfolio keeps the security-assessment narrative, selected sanitized technical artifacts, contribution evidence, and links back to the original repositories where Git history remains preserved.

## Portfolio boundary

The repository you are reading represents:

- the portfolio owner's **group-lead / coordination role**;
- the documented **Security Engineer (SAST)** role;
- OJS lab setup/documentation contributions;
- API/authentication/SAST work supported by issues, report attribution, commits, and artifacts;
- a curated representation of the team's complete OJS assessment lifecycle;
- context for the wider Go Reserve, CI/CD, and LLM-vs-Semgrep workstreams.

The wider workstreams are documented in [`PROJECT_ECOSYSTEM.md`](./PROJECT_ECOSYSTEM.md). They can be promoted as separate portfolio case studies later, while this repository remains focused on the OJS/AppSec assessment.
