# Bead: bob-cli-hc.4 — bob-plugins clock mirror and vector copies

[Bead Pages](../README.md) / [bob-cli-hc](README.md) / bob-cli-hc.4

**Status:** ○ open · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3c.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3c.linker.w0.md) · **Assignee:** `bob-cli-hc.4` · **Size:** medium
**Created:** 2026-11-05 10:03:54 EST
**Plan:** [202611/offclock\_types.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/offclock_types.md)

## Description

plugin-mirror: in the bob-plugins linked repo, teach bob-ledger-tools' `taskEffectiveClockResolution` the same `offclock_types` rules with a type helper that also handles closed tasks, copy the shared vectors byte for byte into both plugin fixture directories, make the test harnesses honor `config`, update plugin docs, rebuild, test, and run `bob plugins sync`.

## Notes

[2026-11-05T16:52:26Z · bob-cli-hc.4] PROPOSED FOLLOW-UP: Re-stamp the running Pomodoro clock when Obsidian block-id-prompt naming changes its name or type — that path has no clock writer today.

## Dependencies

- **Depends on:** [bob-cli-hc.1](bob-cli-hc.1.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hc.6](bob-cli-hc.6.md) ◐ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hc.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hc.4.md) | [bob-cli-hc.4](bob-cli-hc.4.md) | 0 |
