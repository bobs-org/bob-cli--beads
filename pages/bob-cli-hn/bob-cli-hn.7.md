# Bead: bob-cli-hn.7 — Verdicts on the Obsidian project-promotion card

[Bead Pages](../README.md) / [bob-cli-hn](README.md) / bob-cli-hn.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.191](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.191/README.md) · **Assignee:** `bob-cli-hn.7` · **Size:** small
**Created:** 2026-11-05 18:41:47 EST · **Closed:** 2026-11-06 10:23:56 EST
**Plan:** [202611/successor\_card\_verdicts.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/successor_card_verdicts.md)

## Description

promotion: expose the cycler's describe/apply offer-close functions as cycler api v5 and wire them into nav's project-promotion successor card. The task-merge card stays pull-in-only.

## Notes

[2026-11-06T15:23:47Z · bob-cli-hn.7] PROPOSED FOLLOW-UP: docs-check test_readme_table_matches_original_contract_index_snapshot fails identically on clean master f075147 (pinned SHA fedc20a… vs actual 96a429d5… for docs/README.md contract table); unrelated to promotion, needs pin regeneration or README revert

[2026-11-06T15:23:56Z · bob-cli-hn.7] Cycler api v5 (describe/applyOfferCloses) + promotion card verdict wiring done; full npm suite 5657/5657 green, build/docs-inventory green, plugins synced to vault; docs-check README snapshot failure is pre-existing on clean master (recorded as follow-up)

## Dependencies

- **Depends on:** [bob-cli-hn.6](bob-cli-hn.6.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hn.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.7/README.md) | [bob-cli-hn.7](bob-cli-hn.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@f7ae51e`](https://github.com/bobs-org/bob-plugins/commit/f7ae51e90d0a28fd58dd2aa789cc3c3cf8636136) | feat(promotion): wire successor verdicts into the project-promotion card via cycler api v5 | [bob-cli-hn.7](bob-cli-hn.7.md) | 2026-11-06 10:24:57 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:195--code][1] | Confirm the promotion phase is unblocked after the cycler phase closed | 1 |
| read-by | [agent:bob-cli-hn.7][2] | Check phase notes and remaining work before planning | 2 |
| read-by | [agent:bob-cli-hn.land][3] | Need the child scope and notes | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.195.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.7/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hn.land.md

<!-- sase:referenced-by:end -->
