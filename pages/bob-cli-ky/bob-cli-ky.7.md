# Bead: bob-cli-ky.7 — Docs, memory, and deploy

[Bead Pages](../README.md) / [bob-cli-ky](README.md) / bob-cli-ky.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bu](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bu.md) · **Assignee:** `bob-cli-ky.7` · **Size:** medium
**Created:** 2026-11-12 12:30:15 EST · **Closed:** 2026-11-12 15:52:50 EST
**Plan:** [202611/walker\_footers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/walker_footers.md)

## Description

ship: update bob-plugins and bob-cli docs that say the review footer is persistent, publish the Walker Footer glossary strand and the two strand amendments per the accepted memory decisions, optionally record the decision record, and deploy with bob plugins sync.

## Notes

[2026-11-12T20:51:26Z · bob-cli-ky.7] PROPOSED FOLLOW-UP: docs-check offline lychee reports one broken link (gcal-notes page -> reference/mac-capture/event-notes); reproduces identically on the clean tree, unrelated to walker-footer docs

[2026-11-12T20:52:50Z · bob-cli-ky.7] Ship done: ledger/nav plugin docs rewritten for the walker footer (gated s panel, Review clear, ]] next, lane/links panels, attention dot, walkMode v3 + doorbell) within reference word budgets; bob-cli freshness.md + run-morning-review.md updated; published glossary:walker-footer and amended morning-gtd-review-footer + task-freshness per accepted memory decisions (no decision record per mem_decision_record=no); bob-docs lint green, build:check + validate green, lychee failure is pre-existing on clean tree (recorded as PROPOSED FOLLOW-UP); vault deployed via clean-sync recipe, ledger-tools 1.113.0 verified byte-identical

## Dependencies

- **Depends on:** [bob-cli-ky.6](bob-cli-ky.6.md) ✓ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ky.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ky.7/README.md) | [bob-cli-ky.7](bob-cli-ky.7.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`70f69c2`](https://github.com/bobs-org/bob-cli/commit/70f69c2304ee2c7d1765ea0397962ee306253362) | docs(memory): publish walker-footer glossary and ship docs for bracket-walk footers | [bob-cli-ky.7](bob-cli-ky.7.md) | 2026-11-12 15:55:28 EST |
| bob-plugins | [`bob-plugins@444b8a8`](https://github.com/bobs-org/bob-plugins/commit/444b8a866775746a3e5b3f735ef6a579ee13ab52) | docs(plugins): document walker footer, walkMode API, and review attention dot | [bob-cli-ky.7](bob-cli-ky.7.md) | 2026-11-12 15:56:13 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ky.7][1] | Need the phase scope and design file | 2 |
| read-by | [agent:bob-cli-ky.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ky.7/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ky.land.md

<!-- sase:referenced-by:end -->
