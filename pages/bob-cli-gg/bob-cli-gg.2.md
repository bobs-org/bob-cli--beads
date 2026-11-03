# Bead: bob-cli-gg.2 — The pill in bob-ledger-tools (bob-plugins)

[Bead Pages](../README.md) / [bob-cli-gg](README.md) / bob-cli-gg.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.ca](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.ca.md) · **Assignee:** `bob-cli-gg.2` · **Size:** medium
**Created:** 2026-11-03 10:19:38 EST · **Closed:** 2026-11-03 11:21:37 EST
**Plan:** [202611/event\_link\_times.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/event_link_times.md)

## Description

pill: fix the shared Event pill clock bug, then implement the contract in bob-ledger-tools (pure core, Live Preview widget, Reading sweep, gates, liveness, tests, docs, build, sync).

## Notes

[2026-11-03T15:39:37Z · 17b--code] COORDINATION NOTE (from a planning agent; not remaining work and not an earlier attempt at this phase): Read the CROSS-EPIC COORDINATION note on epic bob-cli-gg (items 1–7) before committing; it extends this plan's coordination section. gf's workers do not know about gg, so if gg commits second, gg owns the merge. Use the renamed `--bob-off-clock-icon` if gf has landed. Rely on gf's source-text freshness fix instead of adding another.

[2026-11-03T16:20:50Z · bob-cli-gg.2] PENDING SYNC: bob plugins sync refused by the deploy guard — the vault bob-ledger-tools was deployed from an uncommitted build in workspace bob-cli_10 (gf off-clock-link-chips commit 23d401b, not on master). Per the CROSS-EPIC COORDINATION note item 4, did not use -F. Rebase onto a bob-plugins master containing gf before syncing.

[2026-11-03T16:21:04Z · bob-cli-gg.2] PROPOSED FOLLOW-UP: bob-plugins npm run docs:check fails on docs/reference/glossary.md generated drift (run just docs-gen) identically on the clean master tree 175aced — pre-existing, unrelated to this phase.

[2026-11-03T16:21:37Z · bob-cli-gg.2] Pill implemented in bob-ledger-tools: shared clock fix (ES1-ES10), pure core 291d, Live Preview 291e, Reading 291f, gates, CSS, docs, manifest 1.96.0. Verified: new suite 22/22, neighbors (gcal/frees/unblocked/progress/ledger-type/task-link x3/meet/clock) green, full npm test 5267/5272 with only the 5 pre-existing baseline failures, build:check/validate green, docs:gen done. Sync pending (deploy guard: vault holds bob-cli_10 gf uncommitted build; no -F per coord note). docs:check glossary drift pre-exists on clean master.

## Dependencies

- **Depends on:** [bob-cli-gg.1](bob-cli-gg.1.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-gg.3](bob-cli-gg.3.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-gg.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gg.2/README.md) | [bob-cli-gg.2](bob-cli-gg.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@8ce2feb`](https://github.com/bobs-org/bob-plugins/commit/8ce2febc8632dc91926f271e3a0033da2f2b9ea2) | feat(ledger-tools): event link time pills with gcal now-on-timeline fix | [bob-cli-gg.2](bob-cli-gg.2.md) | 2026-11-03 11:42:36 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gg.2][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gg.2/README.md

<!-- sase:referenced-by:end -->
