# Bead: bob-cli-iz.2 — Start the create hook only after Templater finishes

[Bead Pages](../README.md) / [bob-cli-iz](README.md) / bob-cli-iz.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1aa](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1aa.md) · **Assignee:** `bob-cli-iz.2` · **Size:** small
**Created:** 2026-11-09 07:12:09 EST · **Closed:** 2026-11-09 07:29:02 EST
**Plan:** [202611/gcal\_sync\_race\_force\_and\_skip\_reasons.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_sync_race_force_and_skip_reasons.md)

## Description

ledger_tools_readiness: bob-plugins. Ledger Tools waits for a rendered, settled daily note before spawning `bob gcal sync` (and Gmail), calls `--format json`, accepts the `held` status, and surfaces waiting/held notices. See plan section "Phase ledger_tools_readiness".

## Notes

[2026-11-09T12:29:02Z · bob-cli-iz.2] Ledger-tools readiness done in bob-plugins: new 291a readiness fragment (pending-tag detector skipping fences/inline code, gcalEventsNoteReady, gcalEventsWaitForRenderedNote with 500ms settle, 60s bound, --format json spawn args, waiting/held once-per-day notices, held accepted by decoder); calendar hook spawns sync on timeout; Gmail hook keeps skip with 60s text; docs paragraph updated; 39/39 node tests pass, build:check and docs-check pass, deployed via bob plugins sync -F.

## Dependencies

- **Blocks:** [bob-cli-iz.4](bob-cli-iz.4.md) ◐ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-iz.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-iz.2/README.md) | [bob-cli-iz.2](bob-cli-iz.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-iz.2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-iz.2/README.md

<!-- sase:referenced-by:end -->
