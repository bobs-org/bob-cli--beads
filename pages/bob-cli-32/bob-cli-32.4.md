# Bead: bob-cli-32.4 — Install bob, verify bullet drafts with dry runs, and hand Bryan the Mac steps

[Bead Pages](../README.md) / [bob-cli-32](README.md) / bob-cli-32.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0uj](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0uj.md) · **Assignee:** `bob-cli-32.4` · **Size:** small
**Created:** 2026-09-30 21:31:28 EDT · **Closed:** 2026-09-30 23:20:46 EDT
**Plan:** [202609/close\_work\_log\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/close_work_log_bullets.md)

## Description

rollout: reinstall bob on this host and, best effort, on the MacBook. Verify
bullet drafts against the live vault with `capture-parse` and `--dry-run` only,
never closing a real session. Give Bryan the checklist for installing the Mac
app.

## Notes

[2026-10-01T03:19:49Z · bob-cli-32.4] PROPOSED FOLLOW-UP: 5 tests in native::capture_pomodoro_close::linked_task_tests fail on the clean tree (close_plan_preserves_crlf, day_file_can_also_be_a_task_note, selection_in_progress_and_complete, typed_entry_lands_in_task_work_log, worked_example_updates_tasks) — task lines gain unexpected [fresh:: DATE] stamps, likely interference from the bob-cli-31.4 freshness landing; unrelated to the bullet rollout, no code changed in this phase

[2026-10-01T03:19:54Z · bob-cli-32.4] Mac install checklist for Bryan (MacBook unreachable from this host — bbmacbook did not resolve, best-effort remote install skipped): 1) pull bob-cli and run cargo install --path . --locked; 2) confirm bob capture-parse -- '=x2,3' with bullet draft parses; 3) in Bob Mac Capture, pull latest, rebuild, verify close card shows typed entries with details and the =x hint reads =x Ctrl-J 1 wrote the tests; 4) dry-run one bullet close with --dry-run before any real =x close

[2026-10-01T03:20:46Z · bob-cli-32.4] Reinstalled bob (cargo install --path . --locked, bob 0.1.0). Verified read-only: capture-parse accepts =x2,3 + bullet - 2 foo bar baz (log entry), detail bullets nest (+1 detail), '- 1 fixed 3 bugs' keeps literal 3, placeholder '- ' ignored, dangling '- 1' is incomplete; capture --dry-run on bullet draft fails only with no-running-Pomodoro (grammar accepted, daily file untouched) and retired tail --dry-run yields the bullet-hint error. MacBook unreachable (bbmacbook unresolvable); Mac install checklist left as bead note. 5 linked_task_tests fail identically on the clean tree ([fresh::] stamp interference, likely bob-cli-31.4) — filed as PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-32.2](bob-cli-32.2.md) ✓ · ⧖ 2026-09-30
- **Depends on:** [bob-cli-32.3](bob-cli-32.3.md) ✓ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-32.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-32.4/README.md) | [bob-cli-32.4](bob-cli-32.4.md) | 0 |
