# Bead: bob-cli-87.2 — Snapshot view model and Obsidian layer

[Bead Pages](../README.md) / [bob-cli-87](README.md) / bob-cli-87.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.10l](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.10l.md) · **Assignee:** `bob-cli-87.2` · **Size:** large
**Created:** 2026-10-16 07:13:18 EDT · **Closed:** 2026-10-16 11:28:28 EDT
**Plan:** [202610/note\_snapshots.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/note_snapshots.md)

## Description

view-core: build the note_snapshot module. It classifies vault notes, resolves notes and attachments with Obsidian semantics, rewrites Obsidian syntax into the view model, and serializes the projected-Markdown contract with synthetic golden tests.

## Notes

[2026-10-16T15:28:51Z · bob-cli-87.2.1.land--1] View-core requirements are complete: source classification and cached reads, Obsidian URI compatibility, protected syntax and raw task-source fidelity, emitted/namespaced anchors, one-level transclusion and guards, and the serializer/profile shared contract are covered by the completed child phases and landing repairs. Focused snapshot and audio URI tests passed earlier this session. Monitored just check passed 51 tests and retained only the two clean-base capture-templates metadata and native-path-count failures, matching file:explicit:28b089609636028ae170391f; they remain assigned to bob-cli-8b. git diff --check is clean, both epic-symbols checks are empty, just symvision is unavailable, and the latest bc27d52 commit has no view-core drift. Outer epic bob-cli-87 remains open for its land agent.

## Dependencies

- **Blocks:** [bob-cli-87.3](bob-cli-87.3.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-87.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.2.md) | [bob-cli-87.2](bob-cli-87.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-87.2.1.3][1] | need outer epic DECISIONS | 1 |
| read-by | [agent:bob-cli-87.2.1.land--1][2] | Verify the enclosing phase lifecycle after closing its child epic | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-87.2.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-87.2.1.land.md

<!-- sase:referenced-by:end -->
