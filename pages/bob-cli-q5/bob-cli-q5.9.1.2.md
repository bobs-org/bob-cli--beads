# Bead: bob-cli-q5.9.1.2 — Fix the q5-owned bob-cli contract and doc drift

[Bead Pages](../README.md) / [bob-cli-q5.9.1](bob-cli-q5.9.1.md) / bob-cli-q5.9.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1hl](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1hl.md) · **Assignee:** `bob-cli-q5.9.1.2` · **Size:** small
**Created:** 2026-11-27 20:55:07 EST · **Closed:** 2026-11-27 21:45:04 EST
**Plan:** [202611/finish\_snoozed\_tasks\_unattended.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_snoozed_tasks_unattended.md)

## Description

bob-fixes: give deferred snooze reports their documented envelope, describe relative-time rounding as implemented, and correct the stale capture grammar revision claims.

## Notes

[2026-11-28T02:44:55Z · bob-cli-q5.9.1.2] bob-fixes done (uncommitted working tree for land agent): q5-note-1 rounding reworded to delta rule with 12:03 examples in docs/snooze.md, docs/capture.md, src/native/snooze/when.rs; q5-note-2 grammar drift fixed in docs/reference/compatibility.md (32->34 plus Grammar 33/34 sentences) and docs/capture.md history paragraph (Grammar 33 sentence); q5-note-3 slim deferred envelope replaced with per-verb deferred_add/deferred_drop reports (wake path already carried full envelope). No memory notes edited. PROPOSED FOLLOW-UP: ref_library timing test extra_pass_and_additive_id_resolution_agree_on_the_fixture failed once under full parallel load (extra 685ms vs additive 28ms) then passed alone in 0.06s and in the earlier full run; consider a flake bead if it recurs.

[2026-11-28T02:45:04Z · bob-cli-q5.9.1.2] Verified: 7/7 snooze cli unit tests pass (incl. new per-verb deferred-shape tests for add/drop/wake); fmt+clippy clean; full workspace suite green (4304 cli integration + 8294 lib; one ref_library timing flake passed alone in 0.06s); docs-check passes. Real patched binary produced deferred add/drop/wake JSON with correct per-verb envelopes and untouched vault; real deferred wake JSON decodes ok:true via bob-plugins snoozeWakeDecodeReport (read-only node check); Mac SnoozeWakeAddResponse/CaptureSnoozeWakeResponse decode the new shapes (nested task/target, defaulted plan, .deferred status). No linked-repo doc changes needed (no snooze rounding claims found in bob-plugins/bob-mac-capture). Changes left uncommitted for the land agent.

## Dependencies

- **Blocks:** [bob-cli-q5.9.1.8](bob-cli-q5.9.1.8.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-q5.9.1.9](bob-cli-q5.9.1.9.md) ◐ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.9.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.9.1.2/README.md) | [bob-cli-q5.9.1.2](bob-cli-q5.9.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`684811a`](https://github.com/bobs-org/bob-cli/commit/684811a90676b601f8c90e83fab9facc60d3ca1b) | fix(snooze): per-verb deferred envelopes, rounding wording, grammar drift docs | [bob-cli-q5.9.1.2](bob-cli-q5.9.1.2.md) | 2026-11-27 21:45:57 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.9.1.2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.9.1.2/README.md

<!-- sase:referenced-by:end -->
