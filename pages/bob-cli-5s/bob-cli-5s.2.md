# Bead: bob-cli-5s.2 — Hotkey registry and CI render artifacts in Bob Mac Capture

[Bead Pages](../README.md) / [bob-cli-5s](README.md) / bob-cli-5s.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.5z](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.5z.md) · **Assignee:** `bob-cli-5s.2` · **Size:** small
**Created:** 2026-10-08 19:32:40 EDT
**Plan:** [202610/bob\_refs\_panel.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_refs_panel.md)

## Description

mac-groundwork: replace the single-key HotKeyManager with a HotKeyRegistry that routes by EventHotKeyID, keep Capture's hotkey working through it, add a shared PNG render helper for design tests, and make CI render and upload design fixtures as an artifact.

## Notes

[2026-10-08T23:53:27Z · bob-cli-5s.2] PROPOSED FOLLOW-UP: Add a decision record extending the thin-client rule to Bob Refs (opening never mutates the vault) — skipped per epic auto-decision refs_decision_memory=no; land agent to triage into a task bead.

## Dependencies

- **Blocks:** [bob-cli-5s.6](bob-cli-5s.6.md) ◐ · ⧖ 2026-10-08
- **Blocks:** [bob-cli-5s.7](bob-cli-5s.7.md) ◐ · ⧖ 2026-10-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5s.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.2/README.md) | [bob-cli-5s.2](bob-cli-5s.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5s.2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.2/README.md

<!-- sase:referenced-by:end -->
