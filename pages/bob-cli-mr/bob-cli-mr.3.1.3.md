# Bead: bob-cli-mr.3.1.3 — Prove scan interleavings and document the new lock window

[Bead Pages](../README.md) / [bob-cli-mr.3.1](bob-cli-mr.3.1.md) / bob-cli-mr.3.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-mr.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mr.3.md) · **Assignee:** `bob-cli-mr.3.1.3` · **Size:** medium
**Created:** 2026-11-17 12:14:07 EST · **Closed:** 2026-11-17 15:55:35 EST
**Plan:** [202611/highlights\_scan\_lock\_window.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/highlights_scan_lock_window.md)

## Description

scan-proof: complete adversarial concurrency coverage, update lock and receipt contracts, and run the full code and documentation gates with clean-base attribution for unrelated failures.

## Notes

[2026-11-17T20:26:40Z · bob-cli-mr.3.1.3] PROPOSED FOLLOW-UP: just docs-check fails on docs/reference/json-outputs.md word budget (6058/6000) identically on clean HEAD (reproduced with our contract docs stashed); previously noted on bob-cli-ln.5 / bob-cli-lm. This phase did not add words to that page.

[2026-11-17T20:31:07Z · bob-cli-mr.3.1.3] PROPOSED FOLLOW-UP: mounted docs/reference/mac-capture/refs.md (bob-mac-capture) still says a writing scan rewrites last-scan.json; lock-free no-work and prelock failures leave the receipt untouched. Update that sibling page after this lock window lands.

[2026-11-17T20:31:35Z · bob-cli-mr.3.1.3] Verified before just check: cargo test --test cli highlights::scan (137 ok, including 18 scan_interleave), highlights::marker_write (6), highlights::overwrite_recovery (8), highlights::ingest (7); workspace clippy with just check gates exit 0. Handshake tests cover lock-free no-work under held locks, unlocked planning, lock_busy/scan_busy with no mutation, stale-input replan, two-scan intake, recovery-before-hook, prelock intake_collision (no receipt) vs post-lock intake_collision (receipt). just docs-check only fails json-outputs 6058/6000 on clean HEAD.

[2026-11-17T20:55:35Z · bob-cli-mr.3.1.3--1] Handshake-bounded scan interleave tests and lock/receipt docs landed. Inline sase tool run check (c1327b1097f4dd3056ca723d33370f55) exit 0 after the prepared just check (0b3ac4084e7592ab3a19dc20058d8de8) also passed. Host completion had missed Python stage names that this Rust check does not emit; recovered via inline verification + sase final submit. Follow-ups already on the bead: json-outputs.md word-budget on clean HEAD, and bob-mac-capture last-scan.json wording.

## Dependencies

- **Depends on:** [bob-cli-mr.3.1.2](bob-cli-mr.3.1.2.md) ✓ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-mr.3.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mr.3.1.3.md) | [bob-cli-mr.3.1.3](bob-cli-mr.3.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6c409ab`](https://github.com/bobs-org/bob-cli/commit/6c409ab287f79994ac5fc257c0d47f9fc4ed273c) | test(ref): prove narrow scan lock-window interleavings | [bob-cli-mr.3.1.3](bob-cli-mr.3.1.3.md) | 2026-11-17 15:56:23 EST |
