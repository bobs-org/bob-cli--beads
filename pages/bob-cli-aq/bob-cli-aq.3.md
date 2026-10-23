# Bead: bob-cli-aq.3 — Roll preview in the review footer

[Bead Pages](../README.md) / [bob-cli-aq](README.md) / bob-cli-aq.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.132](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.132.md) · **Assignee:** `bob-cli-aq.3` · **Size:** small
**Created:** 2026-10-23 06:34:43 EDT · **Closed:** 2026-10-23 07:41:16 EDT
**Plan:** [202610/quick\_roll\_alt\_p.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/quick_roll_alt_p.md)

## Description

footer-preview: bob-ledger-tools shows the compact preview in the footer's hint slot and the full sentence in its tooltip while the cursor is on a review row.

## Notes

[2026-10-23T11:41:07Z · bob-cli-aq.3] PROPOSED FOLLOW-UP: full npm test shows 6 failures that reproduce identically on the clean base tree (verified via git stash): unblocked-glyph x4 (tracked by bob-cli-6v), Keep counts once and saturates at 999 (tracked by bob-cli-6w), forward conversion carries a Depends-On line (noted on bob-cli-am.6/bob-cli-a2.3). Footer-preview suite itself is 25/25 green.

[2026-10-23T11:41:16Z · bob-cli-aq.3] Footer preview done and verified in bob-plugins: updateFreshnessStatusBar calls nav api.quickRoll v1 preview({lines, line, tier}) only on queue rows (v1+ gate, try/catch, footer never throws); freshnessFooterView puts compact in the hint slot and detail in the tooltip next to actionHint; aria and paint key pick it up with no extra changes; without nav or on PRE/POST the footer is byte-identical. Tests: 6 new tests in test-ledger-tools-freshness-footer.cjs, 25/25 pass. Docs sentence + manifest description added, ledger-tools bumped 1.63.3 to 1.64.0, docs:gen/build/validate/docs:check green, bob plugins sync deployed. Full npm test: 3456/3462 pass; the 6 failures reproduce identically on the clean base tree and are already tracked (bob-cli-6v, bob-cli-6w, am.6/a2.3 notes).

## Dependencies

- **Depends on:** [bob-cli-aq.2](bob-cli-aq.2.md) ✓ · ⧖ 2026-10-23
- **Blocks:** [bob-cli-aq.4](bob-cli-aq.4.md) ✓ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-aq.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-aq.3/README.md) | [bob-cli-aq.3](bob-cli-aq.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@060395d`](https://github.com/bobs-org/bob-plugins/commit/060395d72fca04391411c33ad8ec2f607234f97e) | feat(ledger-tools): show Alt+P roll preview in the review footer | [bob-cli-aq.3](bob-cli-aq.3.md) | 2026-10-23 07:42:13 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-aq.3][1] | need full | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-aq.3/README.md

<!-- sase:referenced-by:end -->
