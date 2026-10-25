# Bead: bob-cli-an.6.6.6.5.6.5.5.6.2 — Mark the source manifest published after an explicit sase-listen publish

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6](bob-cli-an.6.6.6.5.6.5.5.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.2` · **Size:** small
**Created:** 2026-10-25 08:44:09 EDT · **Closed:** 2026-10-25 08:55:52 EDT
**Plan:** [202610/backlog\_batch9\_epipe\_listen\_publish\_refresh\_flakes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch9_epipe_listen_publish_refresh_flakes.md)

## Description

listen-explicit-publish: resolve bob-cli-c1 in sase-listen so an explicit publish in either feed role marks the originating library manifest published, with success, failure, and mark-failure tests.

## Notes

[2026-10-25T12:55:41Z · bob-cli-an.6.6.6.5.6.5.5.6.2] Baseline: explicit sase-listen publish delivered the episode but left the source library manifest published:false in both roles (sase-listen ba0613d; only receive_episode, flush_pending, and render auto-publish marked). Fix: publish_any in src/sase_listen/feedhost.py now flips the source manifest via mark_manifest_published after every successful publish in both roles (new _mark_published_or_raise helper); a mark OSError/ValueError raises SaseListenError (exit 1, human+JSON) with a --pending hint in the remote role (run_publish queues it, so publish --pending retries the mark) and a rerun hint locally; delivery failures still leave published:false with unchanged outbox behavior. Removed the now-redundant mark in pipeline.py render auto-publish so publish_any is the single owner. Tests: 7 new tests in tests/test_feedhost.py (publish_any success local+remote, delivery failure both roles, mark failure both roles, CLI success, CLI mark-failure JSON, CLI remote mark-failure queues for --pending). sase tool run check passes (lint+full suite). Limitation: a local render auto-publish mark failure now surfaces through the generic 'Auto-publish skipped' warning (message body states the episode was delivered); visible and repairable, wording prefix slightly off. Target task bob-cli-c1 left open for the lander to verify.

[2026-10-25T12:55:52Z · bob-cli-an.6.6.6.5.6.5.5.6.2] Verified: new tests failed before the fix (6 failed) and pass after; tests/test_feedhost.py, test_feed.py, test_cli.py (73 passed) and test_pipeline.py, test_buildinfo.py (72 passed) green; sase tool run check (lint+full suite) succeeded. Explicit publish now marks the source manifest published:true in both roles; delivery failure leaves it false; mark failure exits 1 with human+JSON error and a repair path (queued --pending retry remotely, rerun locally).

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.2/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.2](bob-cli-an.6.6.6.5.6.5.5.6.2.md) | 0 |
