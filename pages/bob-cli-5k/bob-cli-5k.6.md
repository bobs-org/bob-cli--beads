# Bead: bob-cli-5k.6 — Refuse bare plugin syncs from a different bob-plugins checkout

[Bead Pages](../README.md) / [bob-cli-5k](README.md) / bob-cli-5k.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0y2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0y2.md) · **Assignee:** `bob-cli-5k.6` · **Size:** small
**Created:** 2026-10-07 14:38:42 EDT · **Closed:** 2026-10-07 16:08:08 EDT
**Plan:** [202610/close\_top\_ten\_impact\_beads.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/close_top_ten_impact_beads.md)

## Description

plugins-sync-guard: make `bob plugins sync` without `--repo` abort before any pull or copy when run from inside a bob-plugins checkout other than the resolved repo, test it, document the rule in bob-cli and bob-plugins AGENTS.md, and close bob-cli-59.

## Notes

[2026-10-07T20:07:50Z · bob-cli-5k.6] PROPOSED FOLLOW-UP: scrub DISPLAY/WAYLAND_DISPLAY in CLI test harness — capture_url_with_markers_or_flags_stays_a_task fails under stale SSH-forwarded DISPLAY (xclip cannot open display), reproducing identically on the clean base tree; named in epic plan check-gate section 5.2

[2026-10-07T20:08:08Z · bob-cli-5k.6] Implemented foreign-checkout guard for bare bob plugins sync (src/native/plugins/guard.rs + cli.rs): refuses exit 2 before pull/copy when cwd is inside a different bob-plugins checkout, incl. dry-run and json mode. 4 new CLI tests pass (foreign refused/origin+marker, resolved allowed, unrelated allowed, explicit --repo allowed); lib 1896 green; cli 1163/1164 with the only failure the pre-existing DISPLAY/xclip env test, reproduced on clean base and recorded as PROPOSED FOLLOW-UP. Closed bob-cli-59. Docs: docs/plugins.md + bob-plugins AGENTS.md@856afc9. No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-5k.3](bob-cli-5k.3.md) ✓ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5k.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5k.6/README.md) | [bob-cli-5k.6](bob-cli-5k.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bb66952`](https://github.com/bobs-org/bob-cli/commit/bb669522e38f2bf5652125225d1b24e1d83987d8) | feat(plugins): refuse bare sync from a foreign bob-plugins checkout | [bob-cli-5k.6](bob-cli-5k.6.md) | 2026-10-07 16:09:02 EDT |
