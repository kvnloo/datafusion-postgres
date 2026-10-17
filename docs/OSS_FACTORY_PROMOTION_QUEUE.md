<!-- oss-factory:v1
{"id":"20261017-lane23-postgres-promotion-state","kind":"state","project":"datafusion-postgres-doss","from":"chatgpt","to":["factory"],"status":"blocked","dedupe_key":"promotion-queue:Doss-com/datafusion-postgres","civ":{"city_id":"oss:datafusion-postgres-doss"},"goal_lock":{"objective":"Recover, independently validate and promote the existing user-named PostgreSQL TLS/security fix, preserving contributor credit and the runtime failure contract; do not invent a replacement feature","targets":["Doss-com/datafusion-postgres:master@47bdf5e4b7b929a85bc48b2a107e0bd7edf8262c","kvnloo/datafusion-postgres:master@47bdf5e4b7b929a85bc48b2a107e0bd7edf8262c"],"controls":["datafusion-contrib/datafusion-postgres:master@94f7f4c4d8ca7a6ba2cea3f83420802827d11852"],"fixture":"Original saved TLS patch, regression fixture and expected failure contract: NOT RECOVERED","environment":"Linux ARM64 phone inside Omalauncher/PRoot","proof":"Execute the original candidate and baseline against its actual supported PostgreSQL/TLS failure path before any readiness claim"},"execution_proof":{"tested":[],"runtime":"NOT RUN: original candidate unavailable","result_status":"NOT RUN"}}
-->

# PostgreSQL promotion queue — Lane 23

Audit: 2026-10-17. This is the repository-local queue because Issues are disabled. No existing issue, PR, branch queue or queue file was found in either Doss-com/datafusion-postgres or kvnloo/datafusion-postgres. This coordination-only branch is not a TLS product patch and must not be represented as one. Routing remains provisional under [registry PR 190](https://github.com/kvnloo/oss-factory/pull/190); no default branch was merged.

## Bounded human decision

Kevin's active Lane 23 handoff explicitly requests qualification and promotion of finished work in the named DOSS repositories, including the existing DataFusion PostgreSQL TLS/security fix, and repair of existing upstream PR feedback/CI. Scope: independently verified, nonduplicate work; preserve original authorship; no speculative features, public security disclosure, or default-branch merges. This receipt records that existing conversational approval, not a new worker-created approval. Current factory HITL policy retires Linear; missing Linear credentials are not a blocker.

## Routing and exact source identities

- Canonical named project: [Doss-com/datafusion-postgres](https://github.com/Doss-com/datafusion-postgres), `master` at `47bdf5e4b7b929a85bc48b2a107e0bd7edf8262c`.
- Writable coordination fork: [kvnloo/datafusion-postgres](https://github.com/kvnloo/datafusion-postgres), parent Doss-com/datafusion-postgres, same `master` SHA.
- Original source: [datafusion-contrib/datafusion-postgres](https://github.com/datafusion-contrib/datafusion-postgres), `master` at `94f7f4c4d8ca7a6ba2cea3f83420802827d11852`.
- The DOSS default is an ancestor of original upstream, with zero fork-only and 115 upstream-only commits. This is not 115 unpublished fixes.
- Do not silently retarget a DOSS-specific patch to datafusion-contrib. First recover its original base/intent and establish whether the change belongs in Doss-com, original upstream, or is already covered.

## Ready

None verified ready. No implementation commit was authored or promoted during this audit.

## Existing upstream review

The authenticated REST sweep of all PR states in both datafusion-contrib repositories found no PR authored by kvnloo or headed from kvnloo/Doss-com. Both named Doss forks have no PRs in any state. The kvnloo PostgreSQL fork had no PRs before this coordination record. Therefore no factory-owned live origin PR review, inline thread or CI repair was found to perform in this project. Other contributors' PRs retain their ownership.

## Needs proof — original TLS/security candidate

**HOLD / MISSING_SOURCE.** The exact missing prerequisite is the original saved TLS patch/commit/branch, or access to its writable checkout plus changed files and regression fixture. Also missing: original head/base, patch author/coauthor attribution, original actual failure receipt and expected error/exit behavior. No public candidate identifier or private artifact path was recoverable from accessible fork branches, PRs, repository files, historical factory index 64 and its matching comments, factory issue search, or local archive prompt history.

Do not infer the requested patch from nearby TLS code, write a different TLS feature, or claim source inspection reproduces the user's runtime failure. Preserve the original runtime failure contract when the artifact becomes available.

### Requirement, policy and evidence boundaries

- Current upstream README documents TLS certificate/key options and an encrypted connection workflow. That establishes a supported TLS path, **not** the specific missing candidate's requirement or behavior.
- [Upstream issue 119](https://github.com/datafusion-contrib/datafusion-postgres/issues/119) is closed: its original reporter identified a local root-CA configuration issue. It is not evidence for a new TLS implementation bug and must not be repackaged as this candidate.
- Upstream's [security policy page](https://github.com/datafusion-contrib/datafusion-postgres/security/policy) states no SECURITY.md is configured. Current source trees contain no CONTRIBUTING/AGENTS/AI-contribution policy; this absence is not permission to disclose sensitive details. License is Apache-2.0. Recheck applicable policies and private disclosure route before publishing any security-sensitive candidate.
- Existing integration test source and certificate fixtures are not fresh encrypted-client execution evidence. No existing test count is adopted as this candidate's validation.
- Execution status: **NOT RUN**. No Cargo build, test, linter, formatter, PostgreSQL client connection, RED/GREEN run, or remote CI run was launched for an unavailable patch. Do not spend a heavyweight build on an unrelated control and present it as candidate validation.

## Held or superseded branch work

Nine DOSS branch heads were inventoried. Besides stale dependency branches, named branches are upstream-owned work: `avoid_query_string` (`09ca1e17a1e83a826a8fe6536ad4fa91c93c9595`, Martin Garton), `improve_pg_catalog_type_mapping` (`626d70450ce545dd427f90aa7f87497853e7612d`, Martin Garton), `fix/pg-arrow-catalog2` (`acce715c7d9e0073c5ac3c367b7d2ec0e097b49f`, Ning Sun), `datafusion-50` (`f5c039cfaea5a931ef7def48811e2974824f4ec5`, Ning Sun), and `refactor/pg-catalog-record-batch-access-0.9` (`3d1b7c7d5b82dd49bafc2803259365e633f654fa`, Ning Sun). Those exact heads also exist on original upstream branches; do not create competing PRs.

DOSS `test/datagrip` at `869331f9c02c911bbd58e8b06145456e3277d73c` is an older carrier for Ning Sun's existing [upstream PR 166](https://github.com/datafusion-contrib/datafusion-postgres/pull/166), whose current head is `6055b840b6a45648a374d02582b605667a75ef02`. Disposition **OWNER_COVERED**; no duplicate promotion and no claim of current runtime acceptance.

The only commits reachable from DOSS branches but not any fetched upstream branch are the two stale Arrow 58 dependency heads and two old Datagrip carrier commits. No finished unpublished factory implementation was found.

## Landed

No new merge outcome claimed for this repository. No upstream or downstream default branch was merged.

## Next smallest action

Recover the original artifact and its author/credit, original exact head/base and failure contract. Then inspect disclosure requirements, dedupe current upstream work, finish the actual patch, and execute focused native candidate/baseline plus a real supported TLS/client path on an equipped host. Record exact tested SHA, command, failure/exit outcome and limits here before promotion. The blocker is missing source/provenance and runtime evidence, not Linear authorization.
