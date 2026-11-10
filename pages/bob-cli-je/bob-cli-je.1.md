# Bead: bob-cli-je.1 — Merge engine copies source notes instead of cutting them

[Bead Pages](../README.md) / [bob-cli-je](README.md) / bob-cli-je.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1an](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1an.md) · **Assignee:** `bob-cli-je.1` · **Size:** medium
**Created:** 2026-11-09 18:00:12 EST · **Closed:** 2026-11-09 18:43:20 EST
**Plan:** [202611/merge\_copies\_source\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/merge_copies_source_notes.md)

## Description

engine: stop cutting source bodies, strip identity from copies, keep in-copy links on S's originals, update wording, docs, memory, and tests.

## Notes

[2026-11-09T23:43:20Z · bob-cli-je.1] Merge engine copies source notes: T gets a title bullet plus an identity-stripped copy; S keeps its original notes as a cancelled tombstone with 🪢 LINKS: merged into [[T]]; inbound links stay on S. just fmt, just lint, just test, and just docs-check passed. Scratch-vault bob task merge -d/-o printed '1 note copied', left S's ^detail in place, stripped it from T's copy, and left referrer links on inbox.md. JSON field names moved_lines/moved_notes unchanged. glossary:task-merge and glossary:task-relation updated. No leftover --epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-je.2](bob-cli-je.2.md) ✓ · ⧖ 2026-11-09
- **Blocks:** [bob-cli-je.3](bob-cli-je.3.md) ◐ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-je.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-je.1/README.md) | [bob-cli-je.1](bob-cli-je.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`076fdc4`](https://github.com/bobs-org/bob-cli/commit/076fdc484ff3920a40b5b16bae3dfe518cbdea92) | feat(task-merge)!: copy merged source notes instead of moving them | [bob-cli-je.1](bob-cli-je.1.md) | 2026-11-09 18:44:20 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-je.1][1] | Need notes from earlier agents for remaining work | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-je.1/README.md

<!-- sase:referenced-by:end -->
