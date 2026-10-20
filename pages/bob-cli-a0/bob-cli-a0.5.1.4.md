# Bead: bob-cli-a0.5.1.4 — Weekly fallback build and external link checks

[Bead Pages](../README.md) / [bob-cli-a0.5.1](bob-cli-a0.5.1.md) / bob-cli-a0.5.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.5.md) · **Assignee:** `bob-cli-a0.5.1.4` · **Size:** medium
**Created:** 2026-10-19 23:18:36 EDT · **Closed:** 2026-10-20 00:56:13 EDT
**Plan:** [202610/docs\_gated\_publication.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/docs_gated_publication.md)

## Description

weekly-checks: add the workflow_call-only weekly Material build and online lychee check, its separate issue lifecycle and caller, and validate the complete workflow set and production build path.

## Notes

[2026-10-20T04:56:13Z · bob-cli-a0.5.1.4] Weekly checks landed: docs-weekly reusable (workflow_call only, docs-weekly group) + host weekly caller (41 6 * * 1 + dispatch); links --online with bounded retries/timeouts keeping root/remap/fragments and no broad excludes; isolated docs-weekly issue reusing publish-report; host syncs both callers and status lists both issues. Verified: pytest 381 passed 2 skipped, just docs-check passed, just docs-build-material passed, offline links OK (0 errors), online links correctly fails with 5 concrete externals for launch triage (adobe.com 403; bob-mac-capture#readme and bob-plugins#readme missing fragments). epic-symbols clean.

## Dependencies

- **Depends on:** [bob-cli-a0.5.1.3](bob-cli-a0.5.1.3.md) ✓ · ⧖ 2026-10-19
- **Blocks:** [bob-cli-a0.5.1.5](bob-cli-a0.5.1.5.md) ✓ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.5.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.5.1.4/README.md) | [bob-cli-a0.5.1.4](bob-cli-a0.5.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`dadf073`](https://github.com/bobs-org/bob-cli/commit/dadf073491d7ad11a3b3e91e4134aafeb3a05857) | feat(docs): add weekly fallback build and online external link checks | [bob-cli-a0.5.1.4](bob-cli-a0.5.1.4.md) | 2026-10-20 00:57:28 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a0.5.1.4][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.5.1.4/README.md

<!-- sase:referenced-by:end -->
