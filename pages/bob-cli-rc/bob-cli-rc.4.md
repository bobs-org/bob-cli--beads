# Bead: bob-cli-rc.4 — Real-Obsidian acceptance, docs, and deploy

[Bead Pages](../README.md) / [bob-cli-rc](README.md) / bob-cli-rc.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1hg](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1hg.md) · **Assignee:** `bob-cli-rc.4` · **Size:** medium
**Created:** 2026-11-27 15:06:05 EST · **Closed:** 2026-11-27 17:28:47 EST
**Plan:** [202611/ctrl\_jk\_section\_map.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/ctrl_jk_section_map.md)

## Description

ship: prove the map end to end in real Obsidian over CDP (both key routes, lifecycle, dismissal, wrap, windowing, compact, unchanged note bytes), document it in the navigation plugin reference, and deploy with bob plugins sync.

## Notes

[2026-11-27T22:28:32Z · bob-cli-rc.4] PROPOSED FOLLOW-UP: test-snooze-model-vectors resnooze-history vector fails identically on the clean base (20/21 pass; stale woke-history row in daily postimage) — unrelated to the Section Map, needs triage into a task bead

[2026-11-27T22:28:47Z · bob-cli-rc.4] Ship done: real-Obsidian CDP run 23/23 PASS (routes incl. Vim exmap+nnoremap emulation, lifecycle incl. 2253ms linger, wrap, chip parity, 42-heading windowing 8+34, compact strip, margin, only-section, pinned peek, unchanged note hashes, zero console exceptions) with 7 reviewed screenshots; Section map docs subsection + show-section-map row + manifest sentence; 2.107.17 via gate (build, build:check, docs:gen, inventory:check, unit incl. new self-test wrapper) and bob plugins sync (vault at 2.107.17). Acceptance found and fixed 2 wiring bugs: same-dispatch dismissal (stamp guard + Holding reconcile) and body-level host mount (was clipped 17px by .workspace containing block). One pre-existing unrelated failure recorded as follow-up: test-snooze-model-vectors resnooze-history fails identically on clean base.

## Dependencies

- **Depends on:** [bob-cli-rc.3](bob-cli-rc.3.md) ✓ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-rc.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-rc.4/README.md) | [bob-cli-rc.4](bob-cli-rc.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@dca8452`](https://github.com/bobs-org/bob-plugins/commit/dca84529724c2fbbf8336a516e5e281fd1cfd286) | feat(navigation): prove the Section Map in real Obsidian and ship 2.107.17 | [bob-cli-rc.4](bob-cli-rc.4.md) | 2026-11-27 17:29:53 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-rc.4][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-rc.4/README.md

<!-- sase:referenced-by:end -->
