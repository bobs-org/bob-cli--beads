# Bead: bob-cli-n7.3 — Make the detached-grandchild pipe-drain tests deterministic and portable

[Bead Pages](../README.md) / [bob-cli-n7](README.md) / bob-cli-n7.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-n5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-n5.land.md) · **Assignee:** `bob-cli-n7.3` · **Size:** medium
**Created:** 2026-11-18 01:55:52 EST · **Closed:** 2026-11-18 10:22:18 EST
**Plan:** [202611/backlog\_triage\_t4.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/backlog_triage_t4.md)

## Description

pipe-drain: Resolve bob-cli-kl so both subprocess_runner pipe-drain tests pass deterministically on Linux under full-suite load and on macOS, which has no setsid(1).

## Notes

[2026-11-18T14:24:21Z · bob-cli-n7.3] PROPOSED FOLLOW-UP: cargo fmt --all -- --check fails on tests/cli/albums_create.rs:1149 (unrelated to pipe-drain; file untouched by this phase). Baseline evidence: identical fmt diff with change stashed (clean-base exit 1) and with change applied (exit 1); diff of the two fmt logs is empty. Needs a fmt-only pass or a tracking bead.

[2026-11-18T14:24:30Z · bob-cli-n7.3] Interim Linux verification (2026-11-18): replaced both setsid(1) fixtures in src/native/subprocess_runner.rs with a python3 setsid(2)+sentinel fixture (BOB_PIPE_DRAIN_READY, leader waits max 3s, Drop guard SIGKILLs holder). Focused: 6/6 pass, 5 consecutive runs at ~2.11s each (<4s). Full lib suite under parallel load: 7357 passed, 0 failed, pair green within it. Full clippy gate (just-lint flags): exit 0. No stray holders (ps clean). Portability proof without setsid binary on PATH: NO_SETSID_CONFIRMED, new fixture exit 0 with sentinel written; old fixture fails (setsid: not found). python3 already a test dep (fake_clip/fake_gog). just check is red only on the pre-existing fmt item above. Starting macos-ci-check under sase monitor; kl + phase close on green.

[2026-11-18T14:27:14Z · bob-cli-n7.3] macOS gate underway: monitor 5kc7bx (scripts/dev/macos-ci-check) staged and running; no output yet at ~2m (normal: push + run discovery). Beads bob-cli-kl and bob-cli-n7.3 stay open until the macOS verdict lands; the monitor follow-up closes on green or records failing nodes on red.

[2026-11-18T15:21:56Z · bob-cli-n7.3--1] macOS gate BLOCKED by pre-existing lint failure, not by the pipe-drain pair (run https://github.com/bobs-org/bob-cli/actions/runs/44324801726, snapshot SHA 3d9fd5b includes this phase fix). lint job 134873117837 FAILED solely in `just fmt`: cargo fmt --all -- --check reports one diff, tests/cli/albums_create.rs:1149 (`assert!` H1-less join, needs single-line `.all(...)`). Re-verified this turn: identical single-file fmt diff with fix applied AND on clean base (stashed), and src/native/subprocess_runner.rs is fmt-clean; git status shows only that file modified. Consequence: test (macos-latest) job got Lint-macOS-only-targets=ok then Run-tests=cancelled, archive-move=skipped - no macOS verdict on the pair. Linux CI on the same snapshot SHA passed: test (ubuntu-latest) job 134873117938 SUCCESS, both pair tests ok (`run_bounds_pipe_drain_when_detached_grandchild_holds_output`, `raw_run_...`). Re-running the gate now would fail identically on fmt, so no re-run. kl stays OPEN: close requires a green macOS result which this run could not produce.

[2026-11-18T15:22:06Z · bob-cli-n7.3--1] PROPOSED FOLLOW-UP: fmt-only pass on tests/cli/albums_create.rs:1149 (cargo fmt joins the two-line `.all(...)` closure into one line). Pre-existing on clean base, untouched by this phase, but it reds the whole CI workflow including the macOS gate (run 44324801726 lint job 134873117837). No tracking bead exists yet. After the fmt fix lands, re-run scripts/dev/macos-ci-check to obtain the macOS verdict on the pipe-drain pair, then close bob-cli-kl.

[2026-11-18T15:22:18Z · bob-cli-n7.3--1] Pipe-drain fixture ported (src/native/subprocess_runner.rs only): python3 setsid(2)+sentinel instead of setsid(1); leader waits for detach; Drop guard reaps holder. Verified: focused 6/6 x5 runs ~2.11s (<4s bound); full lib suite 7357 passed/0 failed under load; clippy exit 0; my file fmt-clean; no-setsid-on-PATH shell proof passes. CI on snapshot SHA: ubuntu job green with both pair tests ok. macOS verdict blocked: workflow red solely on pre-existing fmt nit tests/cli/albums_create.rs:1149 (byte-identical on clean base, recorded as PROPOSED FOLLOW-UP); macOS Run-tests step cancelled before running. bob-cli-kl left open pending macOS re-run after fmt fix.

## Dependencies

- **Depends on:** [bob-cli-n7.2](bob-cli-n7.2.md) ✓ · ⧖ 2026-11-18
- **Blocks:** [bob-cli-n7.4](bob-cli-n7.4.md) ◐ · ⧖ 2026-11-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-n7.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-n7.3.md) | [bob-cli-n7.3](bob-cli-n7.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f0857be`](https://github.com/bobs-org/bob-cli/commit/f0857be8a6d084b9e9548919b27178c1b3bb2511) | fix(subprocess): make detached-grandchild pipe-drain tests deterministic and portable | [bob-cli-n7.3](bob-cli-n7.3.md) | 2026-11-18 10:24:41 EST |
