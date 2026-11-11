# Bead: bob-cli-kj.4 — Configured-timezone created stamps

[Bead Pages](../README.md) / [bob-cli-kj](README.md) / bob-cli-kj.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bm](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bm.md) · **Assignee:** `bob-cli-kj.4` · **Size:** small
**Created:** 2026-11-11 17:20:03 EST · **Closed:** 2026-11-11 18:08:13 EST
**Plan:** [202611/impact\_ranked\_bead\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/impact_ranked_bead_fixes.md)

## Description

created-offset: pass the configured timezone into capture_project_note's shared timestamp helpers so created/captured stamps carry the right offset on UTC-clock hosts, with a TZ=Etc/UTC regression test (bead bob-cli-k8).

## Notes

[2026-11-11T23:08:04Z · bob-cli-kj.4] Verification: TZ=Etc/UTC simulated via pin_tz_utc0_for_test; 4 new regression tests fail on old code and pass on new (helper, render, notebooks plan, BOB_NOW offset). just check: fmt clean, clippy gate clean, lib 6650 passed, cli 3589 passed on rerun. One parallel flake in first cli run (complete_themes configured_shell, passes isolated/in-module/full-rerun; unrelated theme-completion text, no timestamp path). Backfilling already-written wrong stamps is out of scope per phase.

[2026-11-11T23:08:13Z · bob-cli-kj.4] Configured-timezone created stamps land: shared helpers take Option<Tz> (records delegates), threaded through ProjectNoteRenderInput/CreateRequest/capture planners, all production callers pass configured zone; RFC3339 BOB_NOW offset honored. Verified: 4 new tests fail pre-fix/pass post-fix; just check green (fmt, clippy, lib 6650, cli 3589; one unrelated parallel flake triaged green on rerun).

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kj.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kj.4/README.md) | [bob-cli-kj.4](bob-cli-kj.4.md) | 0 |
