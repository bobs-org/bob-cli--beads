# Bead: bob-cli-a0.5.1.3 — Deploy repository templates and operator commands

[Bead Pages](../README.md) / [bob-cli-a0.5.1](bob-cli-a0.5.1.md) / bob-cli-a0.5.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.5.md) · **Assignee:** `bob-cli-a0.5.1.3` · **Size:** medium
**Created:** 2026-10-19 23:18:35 EDT · **Closed:** 2026-10-20 00:32:05 EDT
**Plan:** [202610/docs\_gated\_publication.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/docs_gated_publication.md)

## Description

host-controls: implement thin caller templates, idempotent preview/apply host bootstrap, publish dispatch/watch and status commands, just recipes, and the operator runbook without launching the live site yet.

## Notes

[2026-10-20T04:32:05Z · bob-cli-a0.5.1.3] Implemented thin host caller (tools/docs/host/publish.yml on 17 * * * * plus dispatch, calling docs-publish.yml@master with matching force/drill/pinned inputs), host README, bob-docs host-bootstrap/publish/status, and just docs-host-bootstrap/docs-publish/docs-status. Preview makes no mutations; apply is idempotent and preserves published.json and unrelated files byte-for-byte; dispatch watches the correlated run; status reports missing first site vs auth failure. Verified: 348 passed 2 skipped (docs suite) and just docs-check exit 0. Did not run the live bootstrap. No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-a0.5.1.2](bob-cli-a0.5.1.2.md) ✓ · ⧖ 2026-10-19
- **Blocks:** [bob-cli-a0.5.1.4](bob-cli-a0.5.1.4.md) ◐ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.5.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.5.1.3/README.md) | [bob-cli-a0.5.1.3](bob-cli-a0.5.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d5c318a`](https://github.com/bobs-org/bob-cli/commit/d5c318a97e103042b6067a1bf63d142e46c4ac7e) | feat(docs): add host templates and operator publish commands | [bob-cli-a0.5.1.3](bob-cli-a0.5.1.3.md) | 2026-10-20 00:33:27 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a0.5.1.3][1] | Need notes, DECISIONS, remaining work, and design path for host-controls phase | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.5.1.3/README.md

<!-- sase:referenced-by:end -->
