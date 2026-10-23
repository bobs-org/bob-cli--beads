# Bead: bob-cli-as.2 — bob-cli managed-log registry, agenda JSON, and note snapshots

[Bead Pages](../README.md) / [bob-cli-as](README.md) / bob-cli-as.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.55.linker.w2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.55.linker.w2.md) · **Assignee:** `bob-cli-as.2` · **Size:** medium
**Created:** 2026-10-23 08:24:12 EDT · **Closed:** 2026-10-23 08:49:48 EDT
**Plan:** [202610/rotten\_log.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/rotten_log.md)

## Description

registry: add ManagedTaskLogKind::Rotten with the 🥀 marker grammar, fix the Schedule Log inserter that files entries under any managed log, emit log "rotten" in capture-pomodoros agenda JSON, render KEPT rows in note snapshots, and document the registry row and MC vectors.

## Notes

[2026-10-23T12:49:48Z · bob-cli-as.2] Registry landed: ManagedTaskLogKind::Rotten with 🥀 grammar (optional VS16, emoji-less, legacy case) + assembly vectors; Schedule inserter now Schedule-only with Work-only/Rotten-only regression tests; agenda log rotten JSON + test; snapshots condense KEPT (newest +N older), full KEPT on include-closed, rotten_logs counter plumbed through view/transclusion/human logs line; docs §2.4 row + MC18-21 + vault-format grammar + capture.md; verified cargo fmt --check, clippy gate, cargo test 3173+1940 pass, just docs-check 447 pass; epic-symbols clean

## Dependencies

- **Depends on:** [bob-cli-as.1](bob-cli-as.1.md) ✓ · ⧖ 2026-10-23
- **Blocks:** [bob-cli-as.8](bob-cli-as.8.md) ✓ · ⧖ 2026-10-23
- **Blocks:** [bob-cli-as.9](bob-cli-as.9.md) ✓ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-as.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-as.2/README.md) | [bob-cli-as.2](bob-cli-as.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5eed7df`](https://github.com/bobs-org/bob-cli/commit/5eed7df96a7ce1ca2d07d13c9859e434c34a73ec) | feat(managed-log): register Rotten Log kind with agenda and snapshot support | [bob-cli-as.2](bob-cli-as.2.md) | 2026-10-23 08:50:36 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-as.2][1] | Need full description plus notes to check remaining work | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-as.2/README.md

<!-- sase:referenced-by:end -->
