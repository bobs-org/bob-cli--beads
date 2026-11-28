# Bead: bob-cli-q5.1.1.4 — Wake receipts, notification arbitration, and first tick step

[Bead Pages](../README.md) / [bob-cli-q5.1.1](bob-cli-q5.1.1.md) / bob-cli-q5.1.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.1.md) · **Assignee:** `bob-cli-q5.1.1.4` · **Size:** medium
**Created:** 2026-11-25 10:36:16 EST · **Closed:** 2026-11-25 17:21:51 EST
**Plan:** [202611/snooze\_wake\_engine.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snooze_wake_engine.md)

## Description

wake-delivery: add post-commit wake receipts, Darwin notification, snooze.notify config, live notifier-claim arbitration and truthful desktop fallback reporting. Register snooze first in tick with a five-minute cadence, readiness gate, two-minute ceiling and nonfailure deferred/skipped handling. Test receipt ordering and notification failures with fakes; update tick/config docs.

## Notes

[2026-11-25T22:21:37Z · bob-cli-q5.1.1.4] PROPOSED FOLLOW-UP: just check 3 lib + 18 CLI failures reproduce on clean HEAD 68dee6e1 (three_component_marker #\"REQUIREMENTS\" vs #requirements; task_drawers missing **REQUIREMENTS**; wispr_summary kicker; capture inbox_route/note_pull/project_note/offer, drawers_complete_after_id_hash, today_matches_unnamed_capture, task_status_hooks grouping) — already recorded on bob-cli-q4 / bob-cli-q5.1.1.1 / bob-cli-q5.1.1.2 / bob-cli-q4.9.1.1

[2026-11-25T22:21:44Z · bob-cli-q5.1.1.4] PROPOSED FOLLOW-UP: just docs-check word-budget overages remain on untouched pages (docs/reference/capture-syntax.md 6011/6000; generated mounted plugin pages bob-ledger-tools.md, bob-navigation-hotkeys.md 6068/6000, plugin-apis.md ~9279/8000) — already recorded on bob-cli-q5.1.1.3 / bob-cli-q4.9.1.1 / bob-cli-q4.11

[2026-11-25T22:21:51Z · bob-cli-q5.1.1.4] Wake delivery landed: post-commit last-wake.json (0600 atomic rename), Darwin org.bobs.bob.snooze.woken after readable receipt, snooze.notify auto|desktop|off with live notifier.json claim, truthful notified mac_capture|desktop|none, tick snooze first (5m/2m, gcal_gate, deferred wait, skipped ok). Verified: rustfmt; focused lib 12 (receipt/notify/config/adapter) pass; CLI snooze+tick 41 pass including invalid notify, live claim, notify off, dry-run leaves prior receipt, deferred/skipped tick. just check 3 lib + 18 CLI and docs-check capture-syntax/plugin budget overages reproduce on HEAD 68dee6e1; recorded as PROPOSED FOLLOW-UP citing bob-cli-q4 / bob-cli-q5.1.1.1 / bob-cli-q5.1.1.2 / bob-cli-q5.1.1.3 / bob-cli-q4.9.1.1. epic-symbols empty. Did not close parent bob-cli-q5.1.1 / bob-cli-q5.1 / bob-cli-q5.

## Dependencies

- **Depends on:** [bob-cli-q5.1.1.3](bob-cli-q5.1.1.3.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q5.1.1.5](bob-cli-q5.1.1.5.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.1.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.1.1.4/README.md) | [bob-cli-q5.1.1.4](bob-cli-q5.1.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9dd67c6`](https://github.com/bobs-org/bob-cli/commit/9dd67c6253060c6492a19a591971f67b25b476c7) | feat(snooze): deliver wake receipts, notices, and first tick step | [bob-cli-q5.1.1.4](bob-cli-q5.1.1.4.md) | 2026-11-25 17:23:07 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.1.1.4][1] | Need full notes, DECISIONS, and remaining work before close | 7 |
| read-by | [agent:bob-cli-q5.1.1.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.1.1.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.1.1.land.md

<!-- sase:referenced-by:end -->
