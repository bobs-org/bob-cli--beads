# Bead: bob-cli-fl.1 — bob-cli: \[off:: Nm\] ledger key, #offclock tag, and the off-clock vocabulary

[Bead Pages](../README.md) / [bob-cli-fl](README.md) / bob-cli-fl.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2z.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2z.linker.w0.md) · **Assignee:** `bob-cli-fl.1` · **Size:** medium
**Created:** 2026-11-01 21:46:35 EST · **Closed:** 2026-11-01 23:55:55 EST
**Plan:** [202611/off\_clock\_pomodoros.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/off_clock_pomodoros.md)

## Description

off-clock-ledger: replace SessionTracking with SessionClock, read and write [off:: Nm], accept #offclock/#off-clock/#untracked, rename every surface to off-clock, give off-clock homes real minutes, and land the glossary and record.

## Notes

[2026-11-02T04:40:55Z · bob-cli-fl.1--4] PROPOSED FOLLOW-UP: Remove the nine baseline Clippy blockers so clean just check can pass — this matches bob-cli-fe note #3: six needless_return findings in task_theme.rs already tracked by bob-cli-fh, plus three capture-language findings attributed to ccd1ada1; none are owned by the off-clock SessionClock changes.

[2026-11-02T04:55:55Z · bob-cli-fl.1--5] Implemented the off-clock ledger key, SessionClock naming, tag aliases, off-clock vocabulary and home minutes, with the authorized glossary and decision records. cargo fmt passed. The final just check reaches clippy and fails on the same nine clean-base errors: six task_theme.rs findings tracked by bob-cli-fh and three capture-language findings documented in bob-cli-fe note #3; no phase-owned SessionClock errors remain. Recorded the proposed follow-up citing bob-cli-fe and bob-cli-fh. epic-symbols reported no leftovers.

## Dependencies

- **Blocks:** [bob-cli-fl.2](bob-cli-fl.2.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-fl.3](bob-cli-fl.3.md) ◐ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-fl.4](bob-cli-fl.4.md) ✓ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fl.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fl.1.md) | [bob-cli-fl.1](bob-cli-fl.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8a9ec68`](https://github.com/bobs-org/bob-cli/commit/8a9ec685ed9c727a0d7338c9c7072b7e285c975e) | feat(off-clock): add off-clock Pomodoro ledger support | [bob-cli-fl.1](bob-cli-fl.1.md) | 2026-11-02 01:10:48 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fl.1--5][1] | Need the phase scope, design file, and prior notes before completing the assigned phase | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fl.1.md

<!-- sase:referenced-by:end -->
