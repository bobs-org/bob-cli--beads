# Bead: bob-cli-fv.6 — Bullets on created and upgraded Event Tasks

[Bead Pages](../README.md) / [bob-cli-fv](README.md) / bob-cli-fv.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5o.linker.w0.md) · **Assignee:** `bob-cli-fv.6` · **Size:** medium
**Created:** 2026-11-02 09:28:51 EST · **Closed:** 2026-11-02 12:11:12 EST
**Plan:** [202611/gcal\_description\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_description_bullets.md)

## Description

birth-bullets: add the config keys, write the bullets with every created Event Task and Maybe→Yes upgrade, add the tri-state journal description record carried by every row record, match rows only on top-level lines, add ≡ N and description_lines, and document birth-time behavior.

## Notes

[2026-11-02T17:11:12Z · bob-cli-fv.6] birth-bullets landed: config keys description/description_lines (defaults bullets/8, setup errors naming the key), bullets on every created Event Task + Maybe->Yes upgrade in one insert_block with design-call-8 indentation, tri-state journal description record (Absent omitted, HandsOff null, Tracked hash+lines; malformed parses HandsOff), required PlannedRow/AdoptedRow.description with carry-forward, top-level-only row matching in plan + list, human dim = N + description_lines in sync/list JSON (never text). Verified: just check exit 0 (26 binaries ok), just docs-check green, BOB_GCAL_GOG sync -d scratch vault shows the motivating Swings!/And retainers! output; sase bead epic-symbols clean. No memory notes edited.

## Dependencies

- **Depends on:** [bob-cli-fv.4](bob-cli-fv.4.md) ✓ · ⧖ 2026-11-02
- **Depends on:** [bob-cli-fv.5](bob-cli-fv.5.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-fv.7](bob-cli-fv.7.md) ◐ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-fv.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fv.6/README.md) | [bob-cli-fv.6](bob-cli-fv.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`db4e8a8`](https://github.com/bobs-org/bob-cli/commit/db4e8a8aa3aeca27647ff0b36780190317fa895d) | feat(gcal): write event descriptions as Event Task bullets at birth | [bob-cli-fv.6](bob-cli-fv.6.md) | 2026-11-02 12:12:20 EST |
