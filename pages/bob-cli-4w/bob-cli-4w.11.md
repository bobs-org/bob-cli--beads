# Bead: bob-cli-4w.11 — Live verification, install, and skill deployment on athena

[Bead Pages](../README.md) / [bob-cli-4w](README.md) / bob-cli-4w.11

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3s.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3s.linker.w0.md) · **Assignee:** `bob-cli-4w.11` · **Size:** small
**Created:** 2026-10-06 20:15:53 EDT · **Closed:** 2026-10-06 23:57:27 EDT
**Plan:** [202610/bob\_ref\_reference\_library.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_ref_reference_library.md)

## Description

verify: run the acceptance exercise and the counts, performance, alias, and dry-run scan checks against the real vault; install the new bob on athena; deploy the skill; and record bead hygiene and follow-ups.

## Notes

[2026-10-07T03:56:49Z · bob-cli-4w.11] verify numbers (athena, real vault ~/bob, release build e3e69df): ref/ has 595 notes, 0 skipped; library 594 (1 superseded: ref/ai/agent_ref/openai_harness_engineer.md -> ref/blogs/harness_engineering.md), finished 327 / started 92 / queued 154 / dropped 21 / unknown 0. show on all 594: annotations_status parsed 313 / absent 281, zero unparsed_region; marker_mirror_excluded on 114 notes; opaque_url on 2. perf: list -R all -A -f json 35ms; 30-query batch find 37ms (budget 250ms). doctor coverage ~424 zorg-era records vs research ~425 (vault drift). scan --dry-run: 116 notes would update = 114 mirror removals + 2 routine marker syncs; trial writing sync on harness_for_rsi copy removed the mirror block, no tombstone, second sync no-op.

[2026-10-07T03:56:53Z · bob-cli-4w.11] PROPOSED FOLLOW-UP: zorg reading-record migration as a separate Bryan-reviewed epic (research Phase 5; ~424 unindexed records counted by bob ref doctor)

[2026-10-07T03:56:57Z · bob-cli-4w.11] PROPOSED FOLLOW-UP: memory task proposing a decisions record that reference reading state is derived and the library verbs are read-only

[2026-10-07T03:57:04Z · bob-cli-4w.11] PROPOSED FOLLOW-UP: library-wide annotation search across ref notes (out of scope for bob-cli-4w)

[2026-10-07T03:57:08Z · bob-cli-4w.11] PROPOSED FOLLOW-UP: bare bob ref defaulting to list (out of scope for bob-cli-4w)

[2026-10-07T03:57:12Z · bob-cli-4w.11] PROPOSED FOLLOW-UP: durable ever-finished reading history beyond derived reading state (out of scope for bob-cli-4w)

[2026-10-07T03:57:16Z · bob-cli-4w.11] PROPOSED FOLLOW-UP: just all has 2 pre-existing lib-test failures on the untouched tree, both already tracked: every_value_arg_has_a_decision (ref create:audio) tracked by bob-cli-4j, and listen_filter_renders_card_and_encoded_play_link (pandoc ampersand escaping) tracked by bob-cli-4u. 1818 lib tests pass; all 54 ref_library + 89 aliases/help/doctor integration tests pass.

[2026-10-07T03:57:27Z · bob-cli-4w.11] Verify done on athena, release build of e3e69df, real vault read-only. Acceptance: finished paper incl. html/v1 URL variant, legacy review_lit_notes, queued chat note, title near-match (possible/90), intake-only URL capture (in_intake), not-in-library, Harness pair (in_library+finished+superseded also). Counts: 595 notes/594 indexed, show-all clean (0 unparsed_region, 114 mirror notes). Perf: list 35ms, 30-query find 37ms. Aliases byte-identical; doctor rows plausible (coverage ~424 vs ~425). Dry-run: 116 updates = 114 mirror removals + 2 routine syncs; trial sync proved tombstone-free removal. Installed via cargo install --locked; bob_ref skill deployed (sase skill init + chezmoi update, ~/.claude/skills/bob_ref/SKILL.md verified). just all: 2 pre-existing lib failures on untouched tree, tracked by bob-cli-4j/bob-cli-4u; ref_library (54) + aliases/help/doctor (89) integration tests all pass.

## Dependencies

- **Depends on:** [bob-cli-4w.10](bob-cli-4w.10.md) ✓ · ⧖ 2026-10-06
- **Depends on:** [bob-cli-4w.7](bob-cli-4w.7.md) ✓ · ⧖ 2026-10-06
- **Depends on:** [bob-cli-4w.8](bob-cli-4w.8.md) ✓ · ⧖ 2026-10-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-4w.11](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4w.11/README.md) | [bob-cli-4w.11](bob-cli-4w.11.md) | 0 |
