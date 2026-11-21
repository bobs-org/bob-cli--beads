# Bead: bob-cli-oj.2 — Calendar group provider, legacy step fill-in, and the pre-adoption guard

[Bead Pages](../README.md) / [bob-cli-oj](README.md) / bob-cli-oj.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1es](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1es.md) · **Assignee:** `bob-cli-oj.2` · **Size:** medium
**Created:** 2026-11-21 07:41:35 EST · **Closed:** 2026-11-21 08:05:17 EST
**Plan:** [202611/bracket\_n\_group\_jumps.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bracket_n_group_jumps.md)

## Description

calendar-groups: in bob-ledger-tools, add the `api.navGroups` v1 provider for daily, week, and quarter group stops plus derived step stops for notes without a written nav link, classify every target as existing, creatable, or ghost, and make `periodNotes.ensureNote` refuse pre-adoption past years.

## Notes

[2026-11-21T13:03:44Z · bob-cli-oj.2] PROPOSED FOLLOW-UP: npm run docs:check fails on clean base: docs/reference/vault-format.md 6016/6000-word lint (bob-cli-oc). plugin-apis.md develop/ over-budget is a warning only (bob-cli-ob).

[2026-11-21T13:03:45Z · bob-cli-oj.2] PROPOSED FOLLOW-UP: bob-plugins npm test fails on clean master 9c4b401 at cycler v6 checklist jump parks the walk then lands on the pin (scripts/test-navigation-checklist-ctrl-enter.cjs:952 expected reviewLanding null, got the PRE row). Reproduced with and without this phase. Causal epic bob-cli-oe.8 (phase oe.8.3 still in_progress).

[2026-11-21T13:03:46Z · bob-cli-oj.2] PROPOSED FOLLOW-UP: skipped decisions:group-stops-are-derived — memory_decision_group_stops=no forbids editing decisions; land agent should add the record that group stops are derived on Bob notes and authored only on nav lines

[2026-11-21T13:05:05Z · bob-cli-oj.2] PROPOSED FOLLOW-UP: bob plugins sync (no -F) refused to overwrite vault bob-ledger-tools: vault is stamped from an uncommitted build in bob-cli_11 (b8b7baf, 2026-11-21T06:00:17Z). After that deploy lands, sync 1.149.0 from a committed tree; do not -F.

[2026-11-21T13:05:17Z · bob-cli-oj.2] api.navGroups v1 calendar group/step stops plus periodNotes v2 pre-adoption refusal in bob-ledger-tools 1.149.0. 27 nav-groups+period-notes tests pass (worked examples, W53/14-week Q4, 1970/2999, exists/creatable/ghost, cache, ensure). Full npm test: 1 failure is pre-existing cycler v6 park-the-walk on clean 9c4b401 (bob-cli-oe.8). docs:check fails on vault-format.md 6016/6000 (bob-cli-oc). epic-symbols clean. bob plugins sync refused without -F because vault ledger-tools is an uncommitted bob-cli_11 deploy.

## Dependencies

- **Blocks:** [bob-cli-oj.4](bob-cli-oj.4.md) ◐ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-oj.5](bob-cli-oj.5.md) ◐ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-oj.6](bob-cli-oj.6.md) ◐ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-oj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.2/README.md) | [bob-cli-oj.2](bob-cli-oj.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@168b665`](https://github.com/bobs-org/bob-plugins/commit/168b665d35c36ec1f28309c6abca21219f161c39) | feat(ledger-tools): add api.navGroups v1 calendar group stops | [bob-cli-oj.2](bob-cli-oj.2.md) | 2026-11-21 08:06:42 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-oj.2][1] | Need phase scope, notes, and remaining work before finishing calendar-groups | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.2/README.md

<!-- sase:referenced-by:end -->
