# Bead: bob-cli-34.5 — bob-cli docs, config guard test, and chezmoi config for roll decay

[Bead Pages](../README.md) / [bob-cli-34](README.md) / bob-cli-34.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0um](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0um.md) · **Assignee:** `bob-cli-34.5` · **Size:** small
**Created:** 2026-09-30 23:56:48 EDT · **Closed:** 2026-10-01 01:36:32 EDT
**Plan:** [202609/priority\_roll\_decay.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/priority_roll_decay.md)

## Description

decay-docs: add the bob-cli docs/projects.md section, the reason-table rows, and notes in randomize.md and freshness.md. Also adds a Rust test that keeps `decay`/`rolls` keys parseable, and a commented `decay` block in the chezmoi-managed config.

## Notes

[2026-10-01T05:36:11Z · bob-cli-34.5] PROPOSED FOLLOW-UP: flaky capture_pomodoros test missing_note_and_missing_section_are_warning_successes failed once in full just test run then passed on rerun and in isolation

[2026-10-01T05:36:32Z · bob-cli-34.5] decay-docs done: projects.md Recommended roll section + decay reason row + cancel mention; randomize.md transparency sentence; freshness.md Surfaces update; new ignores_decay_and_rolls_keys test passes; chezmoi commented decay block committed (0f310930) and validated VALID decay={enabled,rolls:1} via plugin helpers; just all passes (ALL CHECKS PASSED)

## Dependencies

- **Depends on:** [bob-cli-34.4](bob-cli-34.4.md) ✓ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-34.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-34.5/README.md) | [bob-cli-34.5](bob-cli-34.5.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| chezmoi | [`chezmoi@0f31093`](https://github.com/bbugyi200/dotfiles/commit/0f31093073d6fb98e1164fa6d2cdeec365f831b4) | docs: document priority roll decay defaults in bob config | [bob-cli-34.5](bob-cli-34.5.md) | 2026-10-01 01:32:22 EDT |
| bob-cli | [`849e9fe`](https://github.com/bobs-org/bob-cli/commit/849e9fee9dc44d16483e988919dc69ab87bf2ddc) | docs: recommended roll and priority decay docs with config guard test | [bob-cli-34.5](bob-cli-34.5.md) | 2026-10-01 01:39:45 EDT |
