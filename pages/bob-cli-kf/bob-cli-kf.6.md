# Bead: bob-cli-kf.6 — Shell and migration script fixes

[Bead Pages](../README.md) / [bob-cli-kf](README.md) / bob-cli-kf.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bj](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bj.md) · **Assignee:** `bob-cli-kf.6` · **Size:** small
**Created:** 2026-11-11 13:33:44 EST · **Closed:** 2026-11-11 14:07:11 EST
**Plan:** [202611/security\_audit\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/security_audit_fixes.md)

## Description

script-small-fixes: honor bob_notify's --no-timeout escalation, make the tracker migration CRLF-safe and atomic with working duplicate-anchor detection, and settle the decision-gated partial-registry capture-targets behavior.

## Notes

[2026-11-11T19:07:11Z · bob-cli-kf.6] Verified bob_notify persist from the 10th overdue cycle onward (shell -ge 10 plus --no-timeout -> notify-send -t 0; Rust notify.rs parity with persist_notification/notify_send_args tests). Tracker apply is CRLF-safe and atomic (raw-newline read, splitlines, temp+os.replace); duplicate ^ref anchors keyed by block id; scripts/migrations/test_tracker_review_corrections.py 10/10. Partial album-registry walks drop all record capture targets (drop_all), matching completion; capture_targets unit tests pass including partial_registry_hides_every_record_capture_target. just lint green; no leftover --epic-symbol entries.

[2026-11-11T19:38:35Z · bob-cli-kf.6--1] Recovery: just check was red because sibling kf.3 put --literal-pathspecs on every git_command. git check-ignore rejects pathspec magic, and vault_task_loss git grep/ls-files/diff of *.md stopped matching. Scoped the flag to git_command_literal (commit_paths + vault_sync git_success_os). Re-verified the previously failing gkeep/plugins/highlights/vault_sync tests plus just lint.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kf.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kf.6.md) | [bob-cli-kf.6](bob-cli-kf.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4771047`](https://github.com/bobs-org/bob-cli/commit/4771047e8bcc12a59b9c1dd723d078b5ffbdab84) | fix(scripts): persist notify, harden tracker apply, restore git globs | [bob-cli-kf.6](bob-cli-kf.6.md) | 2026-11-11 15:10:57 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kf.6--2][1] | Need current phase status, notes, and whether work already landed | 1 |
| read-by | [agent:bob-cli-kf.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kf.6.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kf.land.md

<!-- sase:referenced-by:end -->
