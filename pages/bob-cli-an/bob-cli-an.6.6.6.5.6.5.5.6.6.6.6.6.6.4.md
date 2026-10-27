# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.4 — Retire the R8 legacy-child dependency readers

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.4` · **Size:** medium
**Created:** 2026-10-26 12:58:46 EDT · **Closed:** 2026-10-26 13:57:33 EDT
**Plan:** [202610/backlog\_batch14\_ledger\_integrity\_mac\_ci\_and\_cleanup.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch14_ledger_integrity_mac_ci_and_cleanup.md)

## Description

retire-legacy-dep-readers: resolve bob-cli-3o by re-verifying zero live legacy children, then removing the R8 readers from bob-cli and bob-navigation-hotkeys with their docs and test vectors.

## Notes

[2026-10-26T17:57:09Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.4] PROPOSED FOLLOW-UP: Resolve the pre-existing BOB_TEST_FIXTURE_PDF docs lint failure — just docs-check still fails on the unchanged highlights source/configuration contract; the same finding was recorded in bob-cli-ce.9 and bob-cli-c9.6.

[2026-10-26T17:57:33Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.4] Retired the R8 legacy-child readers in bob-cli and bob-navigation-hotkeys; updated contract docs, fixtures, and vectors, while preserving legacy_dependency_children=0 in JSON for this release. Verified local dry-run reports zero legacy children, and the Mac hook log had 940 matching zero-child runs. Passed cargo fmt --check, diff checks, 154 task_status_hooks tests, 940 capture tests, and 161 focused plugin tests; npm build/build:check and just docs-gen passed, then bob plugins sync deployed the built bundle. just docs-check remains blocked by the pre-existing BOB_TEST_FIXTURE_PDF lint finding on unchanged source/config, recorded as a proposed follow-up. epic-symbols reported none.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.4/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.4.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0f76d55`](https://github.com/bobs-org/bob-cli/commit/0f76d558b108754eec3db75b0837ae70380be550) | feat(task-deps): retire legacy child dependency readers | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.4.md) | 2026-10-26 13:58:36 EDT |
| bob-plugins | [`bob-plugins@241ca2d`](https://github.com/bobs-org/bob-plugins/commit/241ca2d818eb8381d0c672c877f0415b0b1546f6) | feat(navigation): read dependencies from managed lines only | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.4.md) | 2026-10-26 13:59:59 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.4][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.4--f][2] | Inspect the accidental note target using its exact typed identifier | 2 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land][3] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.4.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land.md

<!-- sase:referenced-by:end -->
