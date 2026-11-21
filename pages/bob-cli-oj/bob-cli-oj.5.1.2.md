# Bead: bob-cli-oj.5.1.2 — Day, week, and quarter cards adopt the group row and the derived step row

[Bead Pages](../README.md) / [bob-cli-oj.5.1](bob-cli-oj.5.1.md) / bob-cli-oj.5.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-oj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.5.md) · **Assignee:** `bob-cli-oj.5.1.2` · **Size:** medium
**Created:** 2026-11-21 12:21:10 EST · **Closed:** 2026-11-21 13:14:40 EST
**Plan:** [202611/group\_rail.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/group_rail.md)

## Description

calendar-rail: compute one nav answer per card from walkMode.links v7 (fallback api.navGroups), render the group row and the legacy derived step row, classify every rail item and chip as exists/creatable/ghost, repaint on vault create/delete/rename and midnight, run the group commands with re-validation, test it, update docs/intention-card.md, then build, test, bump, commit, and sync.

## Notes

[2026-11-21T18:14:24Z · bob-cli-oj.5.1.2] PROPOSED FOLLOW-UP: Refresh the stale intentionCardRailNavigate comment in bob-plugins 296d — it still says the rail exists only for a recognized nav line, but calendar-rail (Ledger Tools 1.151.0) now also renders a derived step row from walkMode.links calendar stops; 296d was off-limits to this phase (o6 coordination), so the comment-only fix belongs to whoever next owns 296d.

[2026-11-21T18:14:40Z · bob-cli-oj.5.1.2] calendar-rail landed in bob-plugins Ledger Tools 1.151.0 (base origin/master c4953d3; commit via this turn's finalizer). New 296ca (BobLedgerToolsIntentionCardGroupRailMixin, registered after the intention-card mixin, exports via new 375a): one nav answer per card from walkMode.links v7 (else navGroupsResolve; parent from navGroups step.parent) reduced to model.navRail; group row on day/week/quarter cards only (years, all_time, conflicted roles keep today's rail); derived step row when there is no written rail and every step stop is calendar-sourced (navGroups fallback also refuses when the body has a prev/next or single-arrow link); exists/creatable/ghost on written items and chips (calendar path or getFirstLinkpathDest; pre-adoption ghost only for past targets, avoiding per-chip vault scans); labels, tooltips, aria names, and center text per the contract; ghost items/arms only Notice; creatable period parent/chips via periodNotesEnsureForPath (refusals surfaced); group arms re-validate against the pane text, refuse with 'The group stop changed — try again' plus a repaint, else run open-prev/next-group-link in the card's leaf (modified click on exists opens like a link; no-Nav fallback opens exists and explains creatable); vault create/delete/rename listeners (after layout) repaint for calendar paths; navRail in the model signature. 296b/296c small edits; 296d untouched. Verified: new scripts/test-ledger-tools-intention-card-group-rail.cjs 16/16 (registered in test:unit) covering all contract worked examples, year/all_time, legacy derived row (both routes), authored step links, conflict, ghost no-op, ensure path, leaf-targeted step and group commands, re-validation mismatch, no-Nav fallback, vault and midnight repaint; all existing intention-card/property-card/nav-groups tests unchanged and green; npm run build:check green; full npm test 8209 pass, 0 fail; npm run docs:check fails only on base budget errors (nav-hotkeys reference 6247/6000 recorded on bob-cli-oj.5.1.1, vault-format 6037/6000 = bob-cli-oc; plugin-apis warning = bob-cli-ob) with intention-card.md clean; docs/intention-card.md Docked rail updated. bob plugins sync deployed Ledger Tools 1.151.0 (bob plugins list --no-pull: synced); it refused block-id-prompt and task-status-cycler because bob-cli_13 deployed them from unlanded 726f9a5 — untouched by this phase, not forced.

## Dependencies

- **Depends on:** [bob-cli-oj.5.1.1](bob-cli-oj.5.1.1.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-oj.5.1.4](bob-cli-oj.5.1.4.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-oj.5.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.2/README.md) | [bob-cli-oj.5.1.2](bob-cli-oj.5.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@63e2f64`](https://github.com/bobs-org/bob-plugins/commit/63e2f6418a4f6135b59884ed888b67ccd9c14d68) | feat(ledger-tools): day, week, and quarter cards adopt the group row | [bob-cli-oj.5.1.2](bob-cli-oj.5.1.2.md) | 2026-11-21 13:15:37 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-oj.5.1.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.2/README.md

<!-- sase:referenced-by:end -->
