# Bead: bob-cli-7e.4 — bob-ledger-tools BLOCKS chips with the 🔑 last-blocker badge

[Bead Pages](../README.md) / [bob-cli-7e](README.md) / bob-cli-7e.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4d.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4d.linker.w0.md) · **Assignee:** `bob-cli-7e.4` · **Size:** medium
**Created:** 2026-10-13 11:09:49 EDT · **Closed:** 2026-10-13 12:18:07 EDT
**Plan:** [202610/prerequisite\_blocks\_lines.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prerequisite_blocks_lines.md)

## Description

chips: render BLOCKS lines in Live Preview and Reading view from a live reverse index of the Tasks memo, with the 🔑 badge, `frees N` summaries, past-tense frozen rows, and stale-entry styling; guard the plan-budget link counter; deploy on this host.

## Notes

[2026-10-13T16:17:56Z · bob-cli-7e.4--1] PROPOSED FOLLOW-UP: npm test has six failures that also reproduce identically on clean base 0d69a20: four scripts/test-ledger-tools-unblocked-glyph.cjs cases (already tracked by bob-cli-6v), scripts/test-navigation-decision-card-handlers.cjs::Keep counts once and saturates at 999 without reset (bob-cli-6w), and scripts/test-task-status-cycler-successor-wiring.cjs::Pomodoro-line close appends the successor to the created continuation. BLOCKS changes add six passing tests.

[2026-10-13T16:18:07Z · bob-cli-7e.4--1] Verified bob-ledger-tools BLOCKS chips: npm run validate passed all 6 manifests; npm test added 6 passing BLOCKS tests and its 6 failures reproduced identically on clean base 0d69a20 (tracked failures noted on bob-cli-6v and bob-cli-6w); synced the local bob-ledger-tools build and restored the three unrelated plugins; added the approved glossary sentence, ran memory init and memory init --check; epic-symbols reported none.

## Dependencies

- **Depends on:** [bob-cli-7e.1](bob-cli-7e.1.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-7e.5](bob-cli-7e.5.md) ✓ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-7e.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-7e.4.md) | [bob-cli-7e.4](bob-cli-7e.4.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f287417`](https://github.com/bobs-org/bob-cli/commit/f287417934042f349541dc70fcb8e87e9deb4da7) | docs(memory): document task dependency BLOCKS mirrors | [bob-cli-7e.4](bob-cli-7e.4.md) | 2026-10-13 12:19:15 EDT |
| bob-plugins | [`bob-plugins@4fad819`](https://github.com/bobs-org/bob-plugins/commit/4fad8196862783513ce66aaff1dc44c150f75d5d) | feat(ledger-tools): render BLOCKS dependency chips | [bob-cli-7e.4](bob-cli-7e.4.md) | 2026-10-13 12:26:12 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7e.4--1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-7e.4.md

<!-- sase:referenced-by:end -->
