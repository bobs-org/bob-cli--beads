# Bead: bob-cli-aq.2 — Roll preview on review-walk landings and api.quickRoll

[Bead Pages](../README.md) / [bob-cli-aq](README.md) / bob-cli-aq.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.132](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.132.md) · **Assignee:** `bob-cli-aq.2` · **Size:** medium
**Created:** 2026-10-23 06:34:43 EDT · **Closed:** 2026-10-23 07:29:44 EDT
**Plan:** [202610/quick\_roll\_alt\_p.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/quick_roll_alt_p.md)

## Description

review-preview: extract one shared recommendation planner, format the concise roll preview, add it as the last line of `]s` landing toasts, and expose it as the additive nav `api.quickRoll` v1 namespace.

## Notes

[2026-10-23T11:29:33Z · bob-cli-aq.2] PROPOSED FOLLOW-UP: bob-plugins full suite still reports the six pre-existing failures verified identical without this phase work (stashed to 92d5809, same 6 fail): four unblocked-glyph cases tracked by bob-cli-6v, the decision-card Keep case by bob-cli-6w, and the forward-promotion conversion case by bob-cli-7i

[2026-10-23T11:29:44Z · bob-cli-aq.2] review-preview done in linked bob-plugins: shared planPriorityRollRecommendationAtLine planner (390 is a thin wrapper, parity-tested), planQuickRollPreview/quickRollPreviewForLine with the exact preview-table strings, landing toasts append the preview line at the ]s jump, answer-advance, and walk-return sites (PRE/POST skipped), additive nav api.quickRoll v1 (root version stays 3), new test-navigation-quick-roll-preview.cjs with 7 passing tests in the npm test list, docs/develop/plugin-apis.md + docs/bob-navigation-hotkeys.md + manifest updated and nav bumped to 2.52.0. Verified: npm run build, npm run validate, npm run docs:check, new+neighbor suites (119 pass), full suite 3450 pass with only the 6 pre-existing failures (verified identical stashed at 92d5809; tracked by bob-cli-6v/6w/7i), and bob plugins sync ran clean. No epic-symbol entries remain.

## Dependencies

- **Depends on:** [bob-cli-aq.1](bob-cli-aq.1.md) ✓ · ⧖ 2026-10-23
- **Blocks:** [bob-cli-aq.3](bob-cli-aq.3.md) ✓ · ⧖ 2026-10-23
- **Blocks:** [bob-cli-aq.4](bob-cli-aq.4.md) ✓ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-aq.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-aq.2/README.md) | [bob-cli-aq.2](bob-cli-aq.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-aq.2][1] | Need full bead including notes for phase work | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-aq.2/README.md

<!-- sase:referenced-by:end -->
