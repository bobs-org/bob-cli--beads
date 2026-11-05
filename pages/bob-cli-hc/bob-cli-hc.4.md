# Bead: bob-cli-hc.4 — bob-plugins clock mirror and vector copies

[Bead Pages](../README.md) / [bob-cli-hc](README.md) / bob-cli-hc.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3c.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3c.linker.w0.md) · **Assignee:** `bob-cli-hc.4` · **Size:** medium
**Created:** 2026-11-05 10:03:54 EST · **Closed:** 2026-11-05 12:21:54 EST
**Plan:** [202611/offclock\_types.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/offclock_types.md)

## Description

plugin-mirror: in the bob-plugins linked repo, teach bob-ledger-tools' `taskEffectiveClockResolution` the same `offclock_types` rules with a type helper that also handles closed tasks, copy the shared vectors byte for byte into both plugin fixture directories, make the test harnesses honor `config`, update plugin docs, rebuild, test, and run `bob plugins sync`.

## Notes

[2026-11-05T16:52:26Z · bob-cli-hc.4] PROPOSED FOLLOW-UP: Re-stamp the running Pomodoro clock when Obsidian block-id-prompt naming changes its name or type — that path has no clock writer today.

[2026-11-05T17:21:54Z · bob-cli-hc.4--4] Verified plugin npm test: 5,563 passed, 0 failed, 1 skipped; bob plugins sync --repo succeeded; both plugin vectors are byte-identical to the bob-cli fixture; epic-symbol check has no entries.

## Dependencies

- **Depends on:** [bob-cli-hc.1](bob-cli-hc.1.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hc.6](bob-cli-hc.6.md) ◐ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hc.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hc.4.md) | [bob-cli-hc.4](bob-cli-hc.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@d751cf3`](https://github.com/bobs-org/bob-plugins/commit/d751cf37adb92a6f2bc8858d576a2f749f5be162) | feat(plugins): mirror offclock type resolution | [bob-cli-hc.4](bob-cli-hc.4.md) | 2026-11-05 12:23:55 EST |
