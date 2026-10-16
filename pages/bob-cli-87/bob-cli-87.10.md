# Bead: bob-cli-87.10 — Obsidian command to snapshot the open note

[Bead Pages](../README.md) / [bob-cli-87](README.md) / bob-cli-87.10

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.10l](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.10l.md) · **Assignee:** `bob-cli-87.10` · **Size:** medium
**Created:** 2026-10-16 07:13:19 EDT · **Closed:** 2026-10-16 15:56:56 EDT
**Plan:** [202610/note\_snapshots.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/note_snapshots.md)

## Description

plugin-command: gated on obsidian_command. Add a desktop-only bob-plugins command that runs bob ref create on the active note, with a -C variant, progress and result notices, then deploys with bob plugins sync.

## Notes

[2026-10-16T19:56:31Z · bob-cli-87.10] PROPOSED FOLLOW-UP: Full bob-plugins npm test has six failures reproduced identically on the clean base: four unblocked-glyph cases (bob-cli-6v), Keep counts once (bob-cli-6w), and forward/reverse conversion (bob-cli-7i); unrelated to this phase.

[2026-10-16T19:56:56Z · bob-cli-87.10] Implemented and deployed both Snapshot note to Highlights commands. Verified active-Markdown gating, the -C variant, resolved bob path and vault environment, progress/result/error notices, and off-desktop refusal; targeted tests passed 5/5 and npm run validate passed. Full npm test had 6 failures reproduced identically on the clean base and tracked by bob-cli-6v, bob-cli-6w, and bob-cli-7i; recorded the proposed follow-up. epic-symbols reported none.

## Dependencies

- **Blocks:** [bob-cli-87.12](bob-cli-87.12.md) ◐ · ⧖ 2026-10-16
- **Depends on:** [bob-cli-87.5](bob-cli-87.5.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-87.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-87.10/README.md) | [bob-cli-87.10](bob-cli-87.10.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-87.10][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-87.10/README.md

<!-- sase:referenced-by:end -->
