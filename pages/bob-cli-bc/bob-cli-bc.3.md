# Bead: bob-cli-bc.3 — Hide, unhide, and color writers plus the vault journal rollout

[Bead Pages](../README.md) / [bob-cli-bc](README.md) / bob-cli-bc.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2c.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2c.linker.w1.md) · **Assignee:** `bob-cli-bc.3` · **Size:** medium
**Created:** 2026-10-24 07:52:22 EDT · **Closed:** 2026-10-24 09:40:47 EDT
**Plan:** [202610/pomodoro\_themes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_themes.md)

## Description

prefs: add the journal writers, collision hints, the vault allowlist and union-merge rollout, and the one-time pin seeding.

## Notes

[2026-10-24T13:22:20Z · bob-cli-bc.3] Seeded pins from live bob themes list -f json (3 theme_hue_collision hints, then empty after): SASE aqua (undo: bob themes color SASE auto), RESEARCH aqua (undo: bob themes color RESEARCH auto), DECKS violet (undo: bob themes color DECKS auto). Vault allowlist 6a3ba8ae (.gitignore !/.bob/themes/*.jsonl + .gitattributes merge=union; git check-ignore last match negated; git check-attr merge: union) then journal 8775297e (.bob/themes/apollo.jsonl). Both landed via vault-sync as vault(apollo) commits.

[2026-10-24T13:40:12Z · bob-cli-bc.3] PROPOSED FOLLOW-UP: capture::related::draft_related_stays_under_the_debug_perf_gate exceeds 500ms under load — reproduces on clean base (667ms isolated after compile, 775ms in cargo test --test cli); prefs tree isolated 3/3 at 330-400ms after cooldown

[2026-10-24T13:40:47Z · bob-cli-bc.3] Shipped hide/unhide/color writers (bob_sync.lock ≤3s, JSON refusals unknown_theme/invalid_hue/unchanged/lock_busy), collision hints on bob themes list, similar vectors, and vault journal allowlist. Live git check-ignore last match !/.bob/themes/*.jsonl; git check-attr merge: union. Vault 6a3ba8ae allowlist, 8775297e apollo.jsonl. Seeded pins: SASE aqua, RESEARCH aqua, DECKS violet (undo: bob themes color NAME auto). Hints empty after pins. Two-host fold, concurrent hides, lock_busy, help, completion, docs-check, clippy unused-gate, cargo test --lib pomodoro_themes all green. just check's only failure is capture::related::draft_related_stays_under_the_debug_perf_gate, which reproduces on the clean base tree. No leftover --epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-bc.10](bob-cli-bc.10.md) ◐ · ⧖ 2026-10-24
- **Depends on:** [bob-cli-bc.2](bob-cli-bc.2.md) ✓ · ⧖ 2026-10-24
- **Blocks:** [bob-cli-bc.6](bob-cli-bc.6.md) ✓ · ⧖ 2026-10-24
- **Blocks:** [bob-cli-bc.7](bob-cli-bc.7.md) ◐ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bc.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bc.3/README.md) | [bob-cli-bc.3](bob-cli-bc.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f6f7909`](https://github.com/bobs-org/bob-cli/commit/f6f79099a6ca7a5c9f94b30c7e5280825a6331b8) | feat(themes): add hide, unhide, and color journal writers | [bob-cli-bc.3](bob-cli-bc.3.md) | 2026-10-24 09:41:48 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-bc.3][1] | Need the phase scope and design file | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bc.3/README.md

<!-- sase:referenced-by:end -->
