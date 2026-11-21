# Bead: bob-cli-oj.5.1 — The group row at the bottom of property cards

[Bead Pages](../README.md) / [bob-cli-oj.5](bob-cli-oj.5.md) / bob-cli-oj.5.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-oj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.5.md) · **Assignee:** `bob-cli-oj.5.1.land`
**Created:** 2026-11-21 12:21:10 EST · **Closed:** 2026-11-21 17:09:11 EST
**Plan:** [202611/group\_rail.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/group_rail.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/group_rail.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:0810648fd519b42127cbe1ed | attached via sase artifact create --bead |
| related | file:explicit:2d421ffa815baa593e33d56d | attached via sase artifact create --bead |
| related | file:explicit:43eb9c4ca9480d51ed367145 | attached via sase artifact create --bead |
| related | file:explicit:52e2fe78b6593e1d06652c85 | attached via sase artifact create --bead |
| related | file:explicit:608eb22989c8cad86c532146 | attached via sase artifact create --bead |
| related | file:explicit:6d9a9dfc810fb1ef3a31ed2c | attached via sase artifact create --bead |
| related | file:explicit:9cf5815b4f609e0391edbda8 | attached via sase artifact create --bead |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/group_rail.md

<!-- sase:links:end -->

## Description

Day, week, and quarter cards and grouped record walk rails show a quiet group row (`« Q3 · W27 … week 8 of 14 ▮▮■▯ … 2027-Q1 · W01 »`) from the same resolver behind `[N` / `]N`; legacy dailies get a derived step row; every missing stop reads dashed `+` (creatable) or dotted and faint (ghost) across rail items, chips, and arms; the album card says `· walks by Section`; and a preview matrix plus the existing e2e suites prove it on athena.

## Notes

[2026-11-21T21:11:29Z · bob-cli-oj.5.1.land] LANDING TRIAGE (bob-cli-oj.5.1.land) of every PROPOSED FOLLOW-UP from the child phases:
- Timing flakes under the parallel full npm test (5.1.1 #1, 5.1.3 #1, 5.1.4 #4) were corroborated on the existing tasks: frees-marks:481 → +1 bob-cli-io; event-link-times:1069 → +1 bob-cli-km; dependencies-stage-performance:64 → +1 bob-cli-m1; keep-moving-marks:236 → +1 bob-cli-nw. Declined, no task filed: test-command-mode-sheet-sequence-dom.cjs:173 (one 30 s timeout under load, no named root cause, passes in isolation) and the gcal-events minute-rollover mismatch (one observation; the cited line drifted, so the node could not be pinned on the current tree). The phases still have them on record if they recur.
- The nav-hotkeys reference page at 6247/6000 words (5.1.1 #2) duplicates bob-cli-ob (trim/split bob-navigation-hotkeys.md) → +1 bob-cli-ob, noting it now fails docs:check.
- The stale intentionCardRailNavigate comment in 296d (5.1.2 #1) is caused by this epic, so it is epic work. o6's code phases are closed and 296d is free now; it goes into the landing tale.
- Intention-card e2e YAML excursion failing on the pre-epic base (5.1.4 #1) → new task bob-cli-ot (ci, related bob-cli-o6).
- record-card e2e race with the auto projects sync (5.1.4 #2) → new task bob-cli-ou (flake).
- record-walk e2e startup null-leaf crash (5.1.4 #3) → new task bob-cli-ov (flake).
- bob-cli-oj.5 note #1 (the skipped decisions:group-stops-are-derived memory record) is left to the outer bob-cli-oj land agent. The same follow-up is already on oj.1, oj.2, and oj.4, and memory_decision_group_stops=no forbids this epic from editing it.

[2026-11-21T22:09:11Z · bob-cli-oj.5.1.land] LANDED (bob-cli-oj.5.1.land). Verification:

PHASES: row-kit c4953d3 (Ledger Tools 1.150.0), calendar-rail 63e2f64 (1.151.0), record-rail 2aa877c (1.152.0), rail-proof cb70f82 (1.155.0); all four phase beads closed.

LANDING TALE (plan:202611/group_rail_declutter.md; Bryan's bob-cli-oj note #2): Ledger Tools 1.157.0, committed by the host finalizer as this turn's bob-plugins stitch on top of origin/master ae305a3 (merged before commit; main.js regenerated). Decisions: layout = slim, glyph = skip, footer = yes.
- Group arms show an inline Lucide skip-back / skip-forward SVG mark (span.bob-property-card-group-glyph[aria-hidden][data-icon]) and the group name only. No «/», no landing, no `·`. The landing stays in the tooltip, and the accessible name now names it in every state (creatable "activating creates <landing>", ghost "<landing> not in vault").
- The centre is the tick track only (bar above 21), with the hidden position label and a title (calendar `Day 6 of 7 in week W47`; record `Section 2 of 4: 🔮 Future Work · 2 of 3`). A one-member group has no centre and no track (the gap keeps the grid). This is Bryan's screenshot case.
- Arm states have no box: creatable is muted ink with a dashed underline under the name and `+`; ghost is faint ink with a dotted underline and `· not in vault`. Items and chips keep their boxes. Forced colors use CanvasText underlines and GrayText ghosts.
- Status-bar links footer: the same kit mark (shared propertyCardGroupMark, no duplicated geometry), and footer text has no «/». Context drops `1/1` (label only). `]n enters/wraps to X` moves to the tooltip while the same-direction group arm names X, and comes back if that arm is shed and it fits.
- Authored «/»/<< >> nav-line grammar and the `Two « links on nav lines — keep one` text are unchanged. Resolver, re-validation, activation, and narrow rules are unchanged.
- 296d intentionCardRailNavigate comment rewritten (derived step row from the same walkMode.links calendar stops), the epic-caused follow-up from 5.1.2.
- Docs: intention-card.md, record-card.md, and the bob-ledger-tools.md compass sentence; bob-navigation-hotkeys.md untouched.

GATES (merged tree): npm run build:check ok. Focused suites: group-row 15/15, intention group-rail 16/16, record-walk group-rail 12/12, album-header 42/42, preview-group-rail 3/3, walker-footer 55/55. Full npm test: 8423 pass, 0 fail, 4 skipped (perf 13/13). A pre-merge run hit event-link-times:1069 once (59.9 ms vs 25 ms; bob-cli-km) and it passed in isolation. docs:check fails only on bob-navigation-hotkeys.md 6307/6000 (bob-cli-ob), plus the plugin-apis.md develop warning (bob-cli-ob). bob-ledger-tools.md was 6033/6000 on 604c8a9 and was fixed upstream by ae305a3; this tale's edit is word-neutral.

PREVIEW: 16 fixtures × 8 = 128 renders, 0 failing. The new fixture record-screenshot-single-member mirrors the screenshot. Every image was inspected at full size; the merged-tree renders are byte-identical. Archive file:explicit:9cf5815b4f609e0391edbda8, inspection note file:explicit:0810648fd519b42127cbe1ed, contrast file:explicit:2d421ffa815baa593e33d56d. Worst cases: ghost 4.95:1 light / 5.2:1 dark (text, underline, mark); creatable 7.04 / 7.63; exists 6.64 / 6.92.

E2E (athena, /snap/bin/obsidian, xvfb-run -a, isolated scratch vaults, merged tree):
- intention-card 81/82: only yaml-done-returns failed (pre-epic, bob-cli-ot); the legacy daily proves the SVG marks and centre title. file:explicit:6d9a9dfc810fb1ef3a31ed2c
- record-card 180/180: file:explicit:52e2fe78b6593e1d06652c85
- record-walk passed: file:explicit:608eb22989c8cad86c532146
- walker-footer: weekGroups and dailyGroups pass, including the new skip-mark and no-«» checks. geometryStable fails identically on clean origin/master (same .bob-bracket-mode x per panel), already proposed as follow-up on bob-cli-oj.6 note #3 and left to the outer landing. file:explicit:43eb9c4ca9480d51ed367145

DEPLOY: bob plugins sync --repo <linked checkout> --no-pull -p bob-ledger-tools; bob plugins list --no-pull shows bob-ledger-tools 1.157.0 synced. Other plugins were not touched: block-id-prompt and task-status-cycler hold bob-cli_13's unlanded 726f9a5 deploy.

EPIC SYMBOLS: none for bob-cli-oj.5.1 or bob-cli-oj.5. `just symvision` does not exist in bob-cli (checked `just --list`).

FOLLOW-UP TRIAGE (recorded on note #1): corroborated bob-cli-io, bob-cli-km, bob-cli-m1, bob-cli-nw, bob-cli-ob; new bob-cli-ot, bob-cli-ou, bob-cli-ov; declined the command-mode sheet timeout and the gcal minute rollover; epic-caused 296d comment fixed in this tale; the decisions-web follow-up is left to the outer bob-cli-oj lander.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-oj.5.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.5.1.land.md) | [bob-cli-oj.5.1](bob-cli-oj.5.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@24ed171`](https://github.com/bobs-org/bob-plugins/commit/24ed1719709183364382e64a48153c01224fea1d) | feat(ledger-tools): declutter the group row and footer group arms with skip marks | [bob-cli-oj.5.1](bob-cli-oj.5.1.md) | 2026-11-21 17:11:32 EST |
| bob-cli--plans | [`bob-cli--plans@b8a4c00`](https://github.com/bobs-org/bob-cli--plans/commit/b8a4c00646dae5071489f1a2214c3f31a0edf796) | chore(plans): mark group\_rail done after landing bob-cli-oj.5.1 | [bob-cli-oj.5.1](bob-cli-oj.5.1.md) | 2026-11-21 17:12:20 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-oj.5.1.1][1] | Need the epic decisions and notes | 1 |
| read-by | [agent:bob-cli-oj.5.1.2][2] | Need the epic decisions and phases | 1 |
| read-by | [agent:bob-cli-oj.5.1.3][3] | Need epic decisions and context | 1 |
| read-by | [agent:bob-cli-oj.5.1.4][4] | Need epic decisions and notes | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.3/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.4/README.md

<!-- sase:referenced-by:end -->
