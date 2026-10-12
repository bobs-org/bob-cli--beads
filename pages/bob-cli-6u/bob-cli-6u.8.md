# Bead: bob-cli-6u.8 — Capture & on ^prj blocks residents; project graph edges and promotion guards

[Bead Pages](../README.md) / [bob-cli-6u](README.md) / bob-cli-6u.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.70](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.70.md) · **Assignee:** `bob-cli-6u.8` · **Size:** medium
**Created:** 2026-10-12 10:26:02 EDT · **Closed:** 2026-10-12 11:57:36 EDT
**Plan:** [202610/prj\_line\_project\_blocking.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_project_blocking.md)

## Description

cli-capture-deps: & with a ^prj dependent refuses same-note targets and blocks, tags, and unlinks residents; implicit resident edges in cycle checks; plan_promotions never raises ^prj.

## Notes

[2026-10-12T15:57:26Z · bob-cli-6u.8] PROPOSED FOLLOW-UP: capture::r#ref percent-listen CLI failures reproduce on clean base, tracked by bob-cli-6m — no new bead needed

[2026-10-12T15:57:36Z · bob-cli-6u.8] Implemented cli-capture-deps: & on ^prj refuses same-note targets, blocks/tags/unlinks residents in one write with commitment transfer; DependencyGraph adds implicit resident edges + never_raise guards; plan_promotions walks through ^prj; & consuming newly-Blocked dependents. Verified: 3 new unit + 5 new CLI tests pass (PDG7, PDB9, §13.5/13.6 vectors); lib 2398 + CLI 1371 green; only failures are the 2 known capture::r#ref percent-listen tests that fail identically on clean base (bob-cli-6m). Docs updated in docs/capture.md.

## Dependencies

- **Depends on:** [bob-cli-6u.2](bob-cli-6u.2.md) ✓ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6u.9](bob-cli-6u.9.md) ✓ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.8/README.md) | [bob-cli-6u.8](bob-cli-6u.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`66c4ddb`](https://github.com/bobs-org/bob-cli/commit/66c4ddbd9f19927eb13fe8d4be78986cb315970f) | feat(capture): block residents on & writes to ^prj with graph and promotion guards | [bob-cli-6u.8](bob-cli-6u.8.md) | 2026-10-12 11:59:33 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:72][1] | Assess 6u phase state and deps for conflict analysis with 6t | 1 |
| read-by | [agent:bob-cli-6u.8][2] | Need the phase scope and design file | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.72/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.8/README.md

<!-- sase:referenced-by:end -->
