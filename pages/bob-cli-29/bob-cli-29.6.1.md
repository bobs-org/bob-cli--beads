# Bead: bob-cli-29.6.1 — bob-cli close contract fixes, clippy cleanup, docs, and required tests

[Bead Pages](../README.md) / [bob-cli-29.6](bob-cli-29.6.md) / bob-cli-29.6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-29.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-29.land.md) · **Assignee:** `bob-cli-29.6.1` · **Size:** medium
**Created:** 2026-09-28 09:06:29 EDT · **Closed:** 2026-09-28 09:38:11 EDT
**Plan:** [202609/pomodoro\_close\_closeout.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/pomodoro_close_closeout.md)

## Description

close-contract-fixes: in bob-cli, fix five things. (1) A relative `-b` path double-joins the vault dir, so every task effect is skipped. (2) `raw` is wrong on link forms. (3) Non-carried rows report `tasks[].carried`. (4) Link-form diagnostics, the human header and locator, and link-form `placement` are wrong. (5) The JSON drops nulls and keeps a `#task` prefix on embedded rows. Also fix the 12 clippy warnings the epic introduced and the gaps in docs/capture.md, and add the integration and protocol tests the parent plan required.

## Notes

[2026-09-28T13:38:11Z · bob-cli-29.6.1] All 5 close-contract fixes landed with manual repro verification: relative -b applies task effects (incl. link+close both editing bob.md); raw is =x/=X on all forms; struck rows report carried:false; link placement is linked/inserted; explicit nulls emitted; #task stripped on embed/subtask rows; link diagnostics keep next-up/section/pre-image lines/own-spelling hints; human header names day file with single locator. 12 epic clippy warnings fixed (zero remain on epic lines; only pre-existing warnings + bob-cli-28 || true error left). docs/capture.md gained Contents entry, TAB worked example, and JSON field docs. tests/cli.rs fixture converted to TAB with byte-exact post-images and full pomodoro_close JSON; added relative-b, transitions, body-hint, bad-range, forced-flag, child-line, dry-run-identity, note-CRLF, and parse/complete/rewrite protocol tests plus nospace-tomato unit test. Verified: cargo fmt --check clean, cargo test fully green (1524+ tests), hand-ran worked example confirming JSON deltas. No epic-symbol leftovers. Note for 29.6.2: new additive pomodoro_close.day_relative key (day file, vault-relative) feeds the human header; Swift decoders should ignore or adopt it. Left uncommitted for land-agent review.

## Dependencies

- **Blocks:** [bob-cli-29.6.2](bob-cli-29.6.2.md) ◐ · ⧖ 2026-09-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-29.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-29.6.1/README.md) | [bob-cli-29.6.1](bob-cli-29.6.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ec31329`](https://github.com/bobs-org/bob-cli/commit/ec3132963f89f15aef1344f3bbef954793325c06) | fix(capture): close-contract fixes for =x Pomodoro close, clippy cleanup, docs, and required tests | [bob-cli-29.6.1](bob-cli-29.6.1.md) | 2026-09-28 09:40:15 EDT |
