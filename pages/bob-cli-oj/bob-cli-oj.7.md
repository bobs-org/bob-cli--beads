# Bead: bob-cli-oj.7 — Album adoption, real-Obsidian proof, and final deploy

[Bead Pages](../README.md) / [bob-cli-oj](README.md) / bob-cli-oj.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1es](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1es.md) · **Assignee:** `bob-cli-oj.7` · **Size:** medium
**Created:** 2026-11-21 07:41:35 EST · **Closed:** 2026-11-21 18:50:40 EST
**Plan:** [202611/bracket\_n\_group\_jumps.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bracket_n_group_jumps.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:1d4596dfd90d9c6ce4174d6a | attached via sase artifact create --bead |
| related | file:explicit:34b0fba4a734a8724a96bbac | attached via sase artifact create --bead |
| related | file:explicit:7d6cde4d840b2c47a9276a59 | attached via sase artifact create --bead |
| related | file:explicit:ee698e8f342e2740746c0830 | attached via sase artifact create --bead |
| related | file:explicit:fde96ae50f55a1ea41d67ab8 | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

adopt-and-prove: verify every host runs plugins and a bob that support grouped walks, set `walk_by` on the zettel, subscriptions, and eat albums (plus movies and podcasts if accepted), sync them, add a real-Obsidian group-jump e2e, run the existing walk, footer, card, and title-block e2e suites, and deploy the final tree.

## Notes

[2026-11-21T23:50:03Z · bob-cli-oj.7] PROPOSED FOLLOW-UP: adopt walk_by once apollo runs bob with record_walk_groups_v1 — apollo was unreachable all session (tailscale ping and SSH via apollo and apollo-do time out); no release tag carries walk_by (e11f2a0c is after v0.5.0), so its bob is unknown. When apollo answers, confirm `bob albums list -f json` reports record_walk_groups_v1, then `bob albums update` subscriptions and eat to walk_by: status and `bob albums sync` (dry-run, review, apply). athena and mac pass; evidence file:explicit:1d4596dfd90d9c6ce4174d6a.

[2026-11-21T23:50:08Z · bob-cli-oj.7] PROPOSED FOLLOW-UP: skipped memory change per decision memory_decision_group_stops=no — decisions-web record that group stops are derived on Bob notes and authored only as «/» links on link-only nav lines (same proposal as oj.1, oj.2, oj.4, oj.5, oj.6).

[2026-11-21T23:50:13Z · bob-cli-oj.7] PROPOSED FOLLOW-UP: walker-footer e2e geometryStable still fails identically (.bob-bracket-mode x = 819/956/1085/968 for s/w/n/b at 1400x900); all group, panel, dot, ink, and bank checks pass. Pre-existing per bob-cli-oj.6 note #3 and reproduced on clean fc806cf by bob-cli-oj.5.1.land; no task bead yet.

[2026-11-21T23:50:28Z · bob-cli-oj.7] adopt-and-prove done. HOST GATE: athena and mac run bob 0.5.0 with record_walk_groups_v1 and nav/ledger supporting grouped walks; apollo unverifiable (unreachable), so per plan subscriptions/eat were NOT adopted (follow-up above). sase_blog_zettel already has walk_by: section, set by Bryan from the Mac (vault 52c909faa); live `bob albums sync -d` shows 0 walk lines to change. walk_more_albums=no, so movies/podcasts untouched. No live-vault writes this phase. E2E: new scripts/obsidian-group-jump-e2e.cjs (offline wrapper in npm test) passes 41/41 on athena under xvfb with real bob (periods ensure, albums sync, records update via logging shim) and Templater: W30/W47/Q4/Saturday/legacy daily [N ]N, derived legacy [n ]n, year notice, authored «/» << >> and Markdown links, << never hijacks [n, prose » ignored, creatable 2027-W01 via bob periods ensure and Monday via the daily template, pre-adoption ghosts byte-identical vault with no ensure call, ]} refuses to create, grouped album ]n across sections, ]N heads, ↺ wrap, Record Card section edit rewrote exactly 5 walk lines with one writer call and no albums sync, rail and footer clicks run the group command, real <C-o> returns. SUITES: record-walk 18/18, record-card 180/180, title-block 65/65, intention-card 81/82 (yaml-done-returns = bob-cli-ot), walker-footer all but geometryStable (pre-existing, follow-up above); preview matrix 128 renders 0 failing. GATES: bob-plugins build:check, docs inventory pass; npm test 8492/8497 with 1 fail = frees-marks 25ms budget (bob-cli-io; passes 3/3 alone), perf lane 13/13; docs:check lint passes, fails only bob-cli test_contracts.py 55!=54 (tracked on bob-cli-on, reproduces on clean bob-cli 6b9139a6); plugin-apis.md warning = bob-cli-ob. bob-cli just check passes; just docs-check fails only the same test_contracts.py. DEPLOY: bob plugins sync from clean e5cb895 (stash): ledger-tools 1.157.0, nav 2.102.0, chips synced and byte-equal to origin/master; block-id-prompt and task-status-cycler stay protected by the abandoned 726f9a5 stamp (already tracked in bob-cli-on.10.1.2 note), not forced. Artifacts: host gate file:explicit:1d4596dfd90d9c6ce4174d6a, group-jump e2e file:explicit:fde96ae50f55a1ea41d67ab8, suite reports file:explicit:ee698e8f342e2740746c0830, preview matrix file:explicit:34b0fba4a734a8724a96bbac, gate logs file:explicit:7d6cde4d840b2c47a9276a59. Glossary strands left for bob-cli-oj.8.

[2026-11-21T23:50:40Z · bob-cli-oj.7] Verified: new real-Obsidian group-jump e2e 41/41 on athena (artifact file:explicit:fde96ae50f55a1ea41d67ab8); record-walk 18/18, record-card 180/180, title-block 65/65, intention-card 81/82 (bob-cli-ot), walker-footer only pre-existing geometryStable; preview matrix 128/0 failing; bob-cli just check green; npm test and docs-check red only on tracked items (bob-cli-io flake, bob-cli-on contract tests); ledger 1.157.0 and nav 2.102.0 deployed clean at origin/master e5cb895. Host gate recorded: apollo unreachable, so subscriptions/eat not adopted (follow-up); zettel already adopted by Bryan and synced.

## Dependencies

- **Depends on:** [bob-cli-oj.5](bob-cli-oj.5.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-oj.6](bob-cli-oj.6.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-oj.8](bob-cli-oj.8.md) ◐ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-oj.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.7/README.md) | [bob-cli-oj.7](bob-cli-oj.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@235c7db`](https://github.com/bobs-org/bob-plugins/commit/235c7db27ea06bea003db3822d908e08ce2f2c04) | test(nav): add the real-Obsidian \[N / \]N group-jump walkthrough | [bob-cli-oj.7](bob-cli-oj.7.md) | 2026-11-21 18:51:25 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-oj.6][1] | Need sibling phase statuses so I do not redo landed work or collide with group-rail | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.6/README.md

<!-- sase:referenced-by:end -->
