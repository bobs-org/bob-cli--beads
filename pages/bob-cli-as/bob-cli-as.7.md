# Bead: bob-cli-as.7 — Freshness mark tooltip shows the logged keeps

[Bead Pages](../README.md) / [bob-cli-as](README.md) / bob-cli-as.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.55.linker.w2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.55.linker.w2.md) · **Assignee:** `bob-cli-as.7` · **Size:** small
**Created:** 2026-10-23 08:24:13 EDT · **Closed:** 2026-10-23 11:03:31 EDT
**Plan:** [202610/rotten\_log.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/rotten_log.md)

## Description

mark-tooltip: add a "🥀 N keeps logged · last <date> — <reason>" line to the bob-ledger-tools freshness mark tooltip in source-note views, never in Tasks query rows.

## Notes

[2026-10-23T15:03:31Z · bob-cli-as.7] Added Rotten Log count/date/reason to bob-ledger-tools freshness mark tooltips in Live Preview and rendered source notes, excluding Tasks query rows. Verified with npm run build, bob plugins sync --repo for the linked checkout, and git diff --check.

## Dependencies

- **Depends on:** [bob-cli-as.6](bob-cli-as.6.md) ✓ · ⧖ 2026-10-23
- **Blocks:** [bob-cli-as.9](bob-cli-as.9.md) ✓ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-as.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-as.7/README.md) | [bob-cli-as.7](bob-cli-as.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@f5557ec`](https://github.com/bobs-org/bob-plugins/commit/f5557ecc4b0a1fd4e2bed05d049d6cabbc7ee089) | feat(freshness): show rotten keeps in mark tooltips | [bob-cli-as.7](bob-cli-as.7.md) | 2026-10-23 11:04:07 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-as.7][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-as.7/README.md

<!-- sase:referenced-by:end -->
