# Bead: bob-cli-hn.4 — Obsidian successor picker verdict UI (api.successors v4)

[Bead Pages](../README.md) / [bob-cli-hn](README.md) / bob-cli-hn.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.191](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.191/README.md) · **Assignee:** `bob-cli-hn.4` · **Size:** medium
**Created:** 2026-11-05 18:41:47 EST · **Closed:** 2026-11-05 19:20:29 EST
**Plan:** [202611/successor\_card\_verdicts.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/successor_card_verdicts.md)

## Description

nav-card: add per-row verdict state, keys, the inline cancel reason, the visuals, footer, two-step Esc, and hover buttons to SuccessorOfferPickerModal, and bump api.successors to v4 with the {picks, closes} result.

## Notes

[2026-11-06T00:20:08Z · bob-cli-hn.4] PROPOSED FOLLOW-UP: docs:check lint has 4 pre-existing BOB_GMAIL_* env errors (profile.rs:90-93) that reproduce identically on the clean base tree; unrelated to nav-card verdict UI

[2026-11-06T00:20:17Z · bob-cli-hn.4] PROPOSED FOLLOW-UP: full npm test shows 3 pre-existing failures on clean base (theme menu vectors x2, ledger-tools vector byte-identity) plus 1 flaky perf timing (wikilink-index 13ms vs 12ms budget); all unrelated to api.successors v4

[2026-11-06T00:20:29Z · bob-cli-hn.4] nav-card verdict UI shipped: api.successors v4 with {picks, closes}, per-row Done/Cancel staging, inline reason, two-step Esc, hover buttons, status/footer/aria; 206a close passthrough, 206c/206d new fragments, 712 exports, CSS, docs, 15 new verdict tests; 41 existing successor tests still green (56/56 focused); full suite 5586/5590 with only pre-existing/flaky failures noted; docs:check shows only the 4 pre-existing GMAIL lint errors; bob plugins sync deployed

## Dependencies

- **Depends on:** [bob-cli-hn.1](bob-cli-hn.1.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hn.5](bob-cli-hn.5.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hn.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.4/README.md) | [bob-cli-hn.4](bob-cli-hn.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@8a16ebe`](https://github.com/bobs-org/bob-plugins/commit/8a16ebeab6e4e2e1069527575cdd5a97352e3bc1) | feat(nav-hotkeys): successor picker verdict UI (api.successors v4) | [bob-cli-hn.4](bob-cli-hn.4.md) | 2026-11-05 19:21:44 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hn.4][1] | Need the phase scope and design file | 2 |
| read-by | [agent:bob-cli-hn.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hn.land.md

<!-- sase:referenced-by:end -->
