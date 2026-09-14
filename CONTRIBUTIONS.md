# My Contribution

This assessment was completed by **Kelompok 1**, a seven-person DevSecOps team. I served as **Group Lead (Ketua Kelompok)** while also working technically as a **Security Engineer (SAST)**.

The original kickoff role matrix explicitly records my technical role as **Security Engineer (SAST)**. It separately lists another teammate as **Project Lead / Scrum Master**. I therefore use **Ketua Kelompok / Group Lead** in this portfolio to describe my coordination responsibility, while keeping the original matrix linked so the distinction is visible to reviewers.

## Leadership responsibilities

As group lead, I helped keep the project organized across multiple stages and repositories. My coordination work included:

- aligning weekly deliverables with the assessment lifecycle;
- coordinating work across SAST, DAST, documentation, risk analysis, application work, and final reporting;
- reviewing progress and helping resolve gaps between artifacts;
- keeping outputs consistent enough to be consolidated into the final assessment package;
- helping ensure that findings, evidence, risk treatment, mitigation material, and supporting engineering work were carried forward between stages.

This was a collaborative project, so leadership here means **coordination and delivery ownership**, not individual authorship of every finding or artifact.

## Technical responsibilities I can substantiate

My technical work covered the following areas:

- OJS lab initialization / setup documentation;
- static source-code review using **Semgrep** and manual inspection;
- REST API and admin-panel attack-surface analysis;
- authentication data-flow analysis;
- documentation of selected findings and technical risk;
- contributions to SAST/DAST documentation and checklist completion;
- contributions to the final risk/reporting repository;
- participation in the broader DevSecOps project ecosystem, including CI/CD architecture material and supporting group engineering work.

## OJS lab setup evidence

The original kickoff repository contains an **`[INIT] OJS Init`** issue assigned to `syifaniads`:

- https://github.com/dso-1/Pertemuan-1-Kickoff-Case-1-Vulnerability-OJS/issues/8

My account also authored setup/documentation commits in that repository. The historical repository contains lab credentials and infrastructure values, so this portfolio does not reproduce those values. See [`docs/LAB_SETUP.md`](./docs/LAB_SETUP.md) for the sanitized setup story.

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

## Direct GitHub commit evidence

Selected commits authored under the `syifaniads` GitHub identity:

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
- Broader DevSecOps project — CI/CD architecture presentation contribution:  
  https://github.com/dso-1/project/commit/961df611d3c6fa2b708e93c054148c19379d5098

The last commit adds the multi-project CI/CD architecture presentation to the broader `dso-1/project` repository.

## Shared-laptop / legacy Git identity caveat

Some of my hands-on work was committed from a **shared or other team laptop**. The local Git configuration on that device was not always my GitHub identity, so the historical author field can point to the laptop owner's local Git name or another account even when I performed the work.

This means `author:syifaniads` is **not a complete contribution counter**.

For recruiter-facing attribution, I use the following evidence hierarchy:

1. commits directly linked to `syifaniads`;
2. issues/tasks assigned to me;
3. report-level finding attribution;
4. artifacts and deliverables tied to my documented responsibilities;
5. team-level repositories for work that was collaborative or whose historical Git identity is ambiguous.

I do **not** relabel a specific commit recorded under another person's identity as mine unless there is a separate basis for that mapping. This avoids creating a false Git history while still explaining why the direct GitHub author filter under-represents my work.

## Broader DevSecOps engineering work

The organization contains additional work beyond the five OJS assessment repositories:

- [`dso-1/project`](https://github.com/dso-1/project) — Jenkins/Docker deployment flow, application code, and multi-project CI/CD architecture material;
- [`dso-1/kelompok1_website`](https://github.com/dso-1/kelompok1_website) — the **Go Reserve** room-reservation application;
- [`dso-1/sast-llm`](https://github.com/dso-1/sast-llm) — an **LLM-vs-Semgrep SAST** comparison project.

Because some contributions were produced from shared devices and these repositories were collaborative, I present them as part of the **group project ecosystem** unless a specific artifact has direct individual evidence.

See [`docs/PROJECT_ECOSYSTEM.md`](./docs/PROJECT_ECOSYSTEM.md), [`docs/SOURCE_EVIDENCE.md`](./docs/SOURCE_EVIDENCE.md), and [`docs/ORIGINAL_ARTIFACT_INVENTORY.md`](./docs/ORIGINAL_ARTIFACT_INVENTORY.md) for the complete boundary.

## Curated artifacts in this portfolio

Two small examples are preserved locally for recruiter review:

- [`artifacts/semgrep/custom_rules.yaml`](./artifacts/semgrep/custom_rules.yaml) — non-sensitive Semgrep rules from the SAST workstream;
- [`artifacts/ci-cd/Jenkinsfile.example`](./artifacts/ci-cd/Jenkinsfile.example) — sanitized representation of the team's Jenkins container-deployment pipeline.

These examples are included to demonstrate the technical shape of the work without copying secrets, raw lab data, or the complete group source tree.

## Team attribution

This portfolio distinguishes between:

- **team output** — collaborative findings, scans, reports, application code, security tooling, CI/CD material, and mitigation artifacts;
- **my leadership contribution** — coordination, continuity between stages, and delivery oversight;
- **my technical contribution** — directly attributable setup, SAST/API/authentication-analysis work, documentation, selected findings, and other work supported by task/artifact evidence;
- **shared-device history** — historical commits whose author metadata alone cannot reliably establish the individual contributor.

That separation is intentional so a reviewer can evaluate both leadership and hands-on security work without treating every team artifact as individually authored or, conversely, assuming that every unlinked commit means I did not contribute.

## What I would improve in a production assessment

If repeating the engagement in a professional environment, I would strengthen the evidence chain by assigning stable ownership and finding IDs from discovery through remediation, storing sanitized raw tool output with hashes, separating scanner observations from manually validated vulnerabilities, and tracking each mitigation through explicit retest results. I would also require per-developer Git identities or signed commits on shared machines so individual contribution history remains verifiable.
