# Bead: bob-cli-rv.2 — Plugin Rotten and Schedule readers and recall bands accept stamps

[Bead Pages](../README.md) / [bob-cli-rv](README.md) / bob-cli-rv.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ho](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ho.md) · **Assignee:** `bob-cli-rv.2` · **Size:** medium
**Created:** 2026-11-28 08:22:27 EST · **Closed:** 2026-11-28 08:49:01 EST
**Plan:** [202611/task\_log\_datetime\_stamps.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_log_datetime_stamps.md)

## Description

plugin-readers: make the nav and ledger-tools Rotten Log parsers, the nav Schedule Log parser, and both plugins' recall-age precision accept stamped and legacy entries. Displays show the time. Deploy both plugins before any plugin writer stamps.

## Notes

[2026-11-28T13:49:01Z · bob-cli-rv.2] plugin-readers done: nav + ledger-tools Rotten/Schedule readers accept stamped and legacy entries with strict rejection of malformed stamps; recall bands use minute precision for every kind with HH:MM last_used; shared display helpers render the time. Verified: build, build:check, docs-check (exit 0), 257/257 tests pass across rotten-log, schedule-log, log-recall, log-history, freshness-mark (+surfaces), rotten-keep, roll-decay, decision-card suites; full unit suite 10467/10472 with the single cabinets-chrome failure reproducing identically on the clean tree (pre-existing, unrelated). Deployed -p bob-navigation-hotkeys and -p bob-ledger-tools; vault bundles contain the new parsers.

## Dependencies

- **Blocks:** [bob-cli-rv.4](bob-cli-rv.4.md) ◐ · ⧖ 2026-11-28
- **Blocks:** [bob-cli-rv.5](bob-cli-rv.5.md) ◐ · ⧖ 2026-11-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-rv.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-rv.2/README.md) | [bob-cli-rv.2](bob-cli-rv.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@d55ba76`](https://github.com/bobs-org/bob-plugins/commit/d55ba7601f39d3f6526a26ae42c59e6cbc306aa5) | feat(plugins): accept stamped Rotten and Schedule entries in readers and recall bands | [bob-cli-rv.2](bob-cli-rv.2.md) | 2026-11-28 08:49:58 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-rv.2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-rv.2/README.md

<!-- sase:referenced-by:end -->
