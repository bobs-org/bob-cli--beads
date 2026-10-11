# Bead: bob-cli-6l — Daily Stats — derived daily metrics, a review journal, bob stats, and an Obsidian Stats page

[Bead Pages](../README.md) / bob-cli-6l

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.0u.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.0u.linker.w0/README.md) · **Assignee:** `bob-cli-6l.land`
**Created:** 2026-10-11 07:01:05 EDT · **Closed:** 2026-10-11 17:56:11 EDT
**Plan:** [202610/daily\_stats.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/daily_stats.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/daily_stats.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/daily_stats.md

<!-- sase:links:end -->

## Description

Bryan can open Stats (Obsidian) or run `bob stats` (terminal) during the weekly prune, understand how the last weeks went in about a minute, trust where every number came from, and add a new daily metric with a few lines of config — with no daily logging habit and no data written that the vault already keeps.

## Notes

[2026-10-11T15:27:10Z · bob-cli-6l.2.1.land] DISCOVERED ISSUE (from bob-cli-6l.2.1 landing review): docs/stats.md records ~2.4 s for stats compute on the live vault, but that came from a debug test build. Release-mode re-measurement by the bob-cli-6l.2.1 land agent (BOB_STATS_REAL_VAULT_PARITY=1 BOB_NOW='2026-10-11 12:00:00' cargo test --release --lib real_vault_parity_is_opt_in, master f9324da, apollo, ~/bob) gives 365-378 ms for the full read plus a 7-day five-metric report — still ~25% over the <=300 ms rollout target. The bob-cli-6l.2.1 remediation tale corrects the doc number; meeting or re-budgeting the target remains rollout (bob-cli-6l.6) / CLI (bob-cli-6l.3) acceptance as the engine plan assigned.

[2026-10-11T21:32:24Z · bob-cli-6l.land] LANDING TRIAGE (bob-cli-6l.land, bob-cli master f11ca41, bob-plugins fa7db2f): PROPOSED FOLLOW-UP outcomes — (1) percent-listen CLI failures (6l.2.1.1 #1, .2.1.3 #1, .2.1.5 #1, .2.1.6 #1, 6l.3 #1, 6l.5.1.1 #1, 6l.5.1.4 #3, 6l.6 #6): reproduced in this lander's just check (1364 passed, 2 failed) -> +1 on existing bob-cli-6m. (2) clean-base bob-plugins npm failures (6l.1 #1, 6l.4 #1, 6l.5.1.2 #1/#2, 6l.5.1.3 #1, 6l.5.1.4 #2): already routed by bob-cli-6l.5.1.land — successor/unblocked-glyph date-pinned fixtures as DISCOVERED ISSUE on active epic bob-cli-5w, picker-clock +1 bob-cli-5r, stage-ranker +1 bob-cli-3w; not re-reproduced here, so no further +1. (3) installed bob predates bob stats (6l.4 #2): resolved by this lander's just install of f11ca41 on apollo; the Mac's bob (built 14:50 EDT) already serves bob stats -f json ok; declined as a task. (4) perf 340–370 ms vs <=300 ms (epic note #1, 6l.3 #2, 6l.6 #4): docs/stats.md#performance records the re-budget, which satisfies the plan's record-the-number acceptance -> new feature task bob-cli-6n (large). (5) snapshot kind (6l.6 #1) -> new feature task bob-cli-6o (large). (6) POST-closeout summary toast (6l.6 #2) -> new feature task bob-cli-6p (medium). (7) four-week revisit (6l.6 #3) -> new feature task bob-cli-6q (small), snoozed until 2026-11-09.

[2026-10-11T21:34:31Z · bob-cli-6l.land] LANDING REVIEW (bob-cli-6l.land): engine/CLI/page verified (just check fails only bob-cli-6m's two percent-listen tests; live bob stats 0.34 s after just install of f11ca41 on apollo; ref part present; STATS chip present; no memory edits; no epic-symbols; no non-epic commits in bob-cli or bob-plugins since 1023e6c/f4a2fe3). Remaining epic work found in the 6l.1 journal writer (bob-plugins f4a2fe3) vs plan Writer duties: Task Card answers always journal 'card' (no done/drop/defer/sequence after-line mapping), host keeps case/dots (Mac would write Kellys-MBP, plan says kellys-mbp) and api.stats.host() missing, plugin hard-coded @2.x and nav manifest never bumped (still 2.18.0), and the nav failure path re-Notices every 15 s (missing api.stats or persistent failure) with no burst/recovery/missing-API-once/500-cap policy and validation rejects pinning the queue head. No journal data exists yet (only walk on 10-11 predated the writer; Mac has journal-capable plugins), so fixing now needs no migration. Planned as lander-authored remediation tale that ends with this epic's closeout.

[2026-10-11T21:56:11Z · bob-cli-6l.land] Verified phases 6l.1-6l.6 and nested epics 6l.2.1 (6 phases) and 6l.5.1 (4 phases) closed with every child note addressed; reviewed the epic's 13 bob-cli commits (1023e6c..f11ca41) and bob-plugins f4a2fe3/db91d68/f3bc5e2/2e7f3b0/fa7db2f. DECISIONS honored: ref_in_done=yes (done/created/dropped include #ref/^ref as the ref kind part; live bob stats show done parts task/ref/prj), stats_chip=yes (label-only STATS chip in dash.md Browse row and docs/dashboard.md), memory_stats_record=no and memory_journal_term=no (no sase/memory changes). Integration: no non-epic commits landed in bob-cli or bob-plugins after the epic began. Live vault: bob stats installed on apollo (0.34 s, json ok); Mac bob serves bob stats; the Mac has journal-capable plugins and no journal lines exist yet because the only walk predated the writer. Landing tale fixed the writer contract: Card after-line outcomes, plan host naming plus api.stats.host(), plugin@manifest version, one-Notice-per-burst/recovery/missing-API/500-cap policy, R20-R24 and host vectors, docs; navigation 2.19.0, ledger-tools 1.48.0 synced to apollo's vault. just check: cargo test --lib 2360 passed; the only remaining just-check failures are the two bob-cli-6m percent-listen tests. Follow-ups per landing triage note: +1 bob-cli-6m; new bob-cli-6n (perf), 6o (snapshot kind), 6p (closeout toast), 6q (four-week revisit, snoozed to 2026-11-09); npm clean-base failures already routed to 5w/5r/3w. justfile has no symvision recipe.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-6l.1](bob-cli-6l.1.md) | Start the clock — the review journal writer | ✓ closed | medium | 2026-10-11 | 1 | 2 |
| [bob-cli-6l.2](bob-cli-6l.2.md) | The stats engine in bob-cli | ✓ closed | large | 2026-10-11 | 1 | 0 |
| [bob-cli-6l.3](bob-cli-6l.3.md) | The bob stats command | ✓ closed | medium | 2026-10-11 | 1 | 1 |
| [bob-cli-6l.4](bob-cli-6l.4.md) | Obsidian Stats page — data path, tiles, and table | ✓ closed | medium | 2026-10-11 | 1 | 2 |
| [bob-cli-6l.5](bob-cli-6l.5.md) | Obsidian Stats page — focus chart, context panels, and interaction | ✓ closed | large | 2026-10-11 | 1 | 0 |
| [bob-cli-6l.6](bob-cli-6l.6.md) | Rollout — real-vault verification, docs, and memory | ✓ closed | small | 2026-10-11 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-6l: Daily Stats — derived daily metrics, a review journal, bob stats, and an Obsidian Stats page [closed]"]
    n1["bob-cli-6l.1: Start the clock — the review journal writer [closed]"]
    n2["bob-cli-6l.2: The stats engine in bob-cli [closed]"]
    n3["bob-cli-6l.2.1: Daily Stats engine for bob-cli-6l.2 [closed]"]
    n4["bob-cli-6l.2.1.1: Define the stats model and configurable metric registry [closed]"]
    n5["bob-cli-6l.2.1.2: Build the single-pass vault and journal index [closed]"]
    n6["bob-cli-6l.2.1.3: Implement ranges, grouping, summaries, and display strings [closed]"]
    n7["bob-cli-6l.2.1.4: Evaluate Pomodoro, task, checklist, and field metrics [closed]"]
    n8["bob-cli-6l.2.1.5: Evaluate review answers and formulas [closed]"]
    n9["bob-cli-6l.2.1.6: Assemble compute, prove the schema, and document the engine [closed]"]
    n10["bob-cli-6l.3: The bob stats command [closed]"]
    n11["bob-cli-6l.4: Obsidian Stats page — data path, tiles, and table [closed]"]
    n12["bob-cli-6l.5: Obsidian Stats page — focus chart, context panels, and interaction [closed]"]
    n13["bob-cli-6l.5.1: Complete Daily Stats charts, context panels, and interaction [closed]"]
    n14["bob-cli-6l.5.1.1: Supply chart and calendar presentation data [closed]"]
    n15["bob-cli-6l.5.1.2: Build the focus chart and accessible interactions [closed]"]
    n16["bob-cli-6l.5.1.3: Render metric-family context panels [closed]"]
    n17["bob-cli-6l.5.1.4: Verify the real renderer in light and dark [closed]"]
    n18["bob-cli-6l.6: Rollout — real-vault verification, docs, and memory [closed]"]
    n0 --> n1
    n0 --> n2
    n2 --> n3
    n3 --> n4
    n3 --> n5
    n3 --> n6
    n3 --> n7
    n3 --> n8
    n3 --> n9
    n0 --> n10
    n0 --> n11
    n0 --> n12
    n12 --> n13
    n13 --> n14
    n13 --> n15
    n13 --> n16
    n13 --> n17
    n0 --> n18
    n1 -.-> n2
    n2 -.-> n10
    n4 -.-> n5
    n4 -.-> n6
    n5 -.-> n7
    n6 -.-> n9
    n7 -.-> n8
    n8 -.-> n9
    n10 -.-> n11
    n11 -.-> n12
    n12 -.-> n18
    n14 -.-> n15
    n15 -.-> n16
    n16 -.-> n17
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6l.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.1/README.md) | [bob-cli-6l.1](bob-cli-6l.1.md) | 2 |
| [bbugyi200.apollo.bob-cli-6l.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6l.2.md) | [bob-cli-6l.2](bob-cli-6l.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-6l.2.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.2.1.1/README.md) | [bob-cli-6l.2.1.1](bob-cli-6l.2.1.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-6l.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6l.2.1.2.md) | [bob-cli-6l.2.1.2](bob-cli-6l.2.1.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-6l.2.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.2.1.3/README.md) | [bob-cli-6l.2.1.3](bob-cli-6l.2.1.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-6l.2.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6l.2.1.4.md) | [bob-cli-6l.2.1.4](bob-cli-6l.2.1.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-6l.2.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.2.1.5/README.md) | [bob-cli-6l.2.1.5](bob-cli-6l.2.1.5.md) | 1 |
| [bbugyi200.apollo.bob-cli-6l.2.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.2.1.6/README.md) | [bob-cli-6l.2.1.6](bob-cli-6l.2.1.6.md) | 1 |
| [bbugyi200.apollo.bob-cli-6l.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6l.2.1.land.md) | [bob-cli-6l.2.1](bob-cli-6l.2.1.md) | 2 |
| [bbugyi200.apollo.bob-cli-6l.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.3/README.md) | [bob-cli-6l.3](bob-cli-6l.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-6l.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.4/README.md) | [bob-cli-6l.4](bob-cli-6l.4.md) | 2 |
| [bbugyi200.apollo.bob-cli-6l.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6l.5.md) | [bob-cli-6l.5](bob-cli-6l.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-6l.5.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.5.1.1/README.md) | [bob-cli-6l.5.1.1](bob-cli-6l.5.1.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-6l.5.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.5.1.2/README.md) | [bob-cli-6l.5.1.2](bob-cli-6l.5.1.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-6l.5.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.5.1.3/README.md) | [bob-cli-6l.5.1.3](bob-cli-6l.5.1.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-6l.5.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6l.5.1.4.md) | [bob-cli-6l.5.1.4](bob-cli-6l.5.1.4.md) | 2 |
| [bbugyi200.apollo.bob-cli-6l.5.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.5.1.land/README.md) | [bob-cli-6l.5.1](bob-cli-6l.5.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-6l.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6l.6.md) | [bob-cli-6l.6](bob-cli-6l.6.md) | 1 |
| [bbugyi200.apollo.bob-cli-6l.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6l.land.md) | [bob-cli-6l](README.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1023e6c`](https://github.com/bobs-org/bob-cli/commit/1023e6cb14cfbf68d8a1ef43cf288e855d6ab6f7) | feat(stats): add review answer journal contract | [bob-cli-6l.1](bob-cli-6l.1.md) | 2026-10-11 07:21:27 EDT |
| bob-plugins | [`bob-plugins@f4a2fe3`](https://github.com/bobs-org/bob-plugins/commit/f4a2fe345748b71b37b3b955f999671f8ea2d288) | feat(stats): journal review answers per host | [bob-cli-6l.1](bob-cli-6l.1.md) | 2026-10-11 07:22:37 EDT |
| bob-cli | [`d513f01`](https://github.com/bobs-org/bob-cli/commit/d513f013bb713434f631f488c00bd531487b1a36) | feat(stats): define engine types, isolated config, and metric registry | [bob-cli-6l.2.1.1](bob-cli-6l.2.1.1.md) | 2026-10-11 08:29:03 EDT |
| bob-cli | [`e27fe70`](https://github.com/bobs-org/bob-cli/commit/e27fe7020e80c1856899cc757f4b0c1e0675076d) | feat(stats): build single-pass vault and journal index | [bob-cli-6l.2.1.2](bob-cli-6l.2.1.2.md) | 2026-10-11 08:58:30 EDT |
| bob-cli | [`7f14f5f`](https://github.com/bobs-org/bob-cli/commit/7f14f5fd47d80227adc7c376d1523e2933e881af) | feat(stats): implement range and series reporting | [bob-cli-6l.2.1.3](bob-cli-6l.2.1.3.md) | 2026-10-11 09:08:21 EDT |
| bob-cli | [`346d4bf`](https://github.com/bobs-org/bob-cli/commit/346d4bf3fe438bccb75c1953be9ac544e06d4d18) | feat(stats): evaluate vault-derived metrics | [bob-cli-6l.2.1.4](bob-cli-6l.2.1.4.md) | 2026-10-11 09:28:02 EDT |
| bob-cli | [`0d014c0`](https://github.com/bobs-org/bob-cli/commit/0d014c0299c25a5f13ca2947a155f0af8562e1c7) | feat(stats): evaluate review answers and checked formulas | [bob-cli-6l.2.1.5](bob-cli-6l.2.1.5.md) | 2026-10-11 09:48:07 EDT |
| bob-cli | [`f9324da`](https://github.com/bobs-org/bob-cli/commit/f9324da87f989be6388c4db3650f9bfc15c6f48e) | feat(stats): assemble compute, prove the schema, and document the engine | [bob-cli-6l.2.1.6](bob-cli-6l.2.1.6.md) | 2026-10-11 11:03:23 EDT |
| bob-cli | [`625e973`](https://github.com/bobs-org/bob-cli/commit/625e973c43de2bd51b33f562af6e3cc50c90b6db) | fix(stats): land Daily Stats engine correctness for bob-cli-6l.2.1 | [bob-cli-6l.2.1](bob-cli-6l.2.1.md) | 2026-10-11 12:52:17 EDT |
| bob-cli--plans | [`bob-cli--plans@6a0a600`](https://github.com/bobs-org/bob-cli--plans/commit/6a0a6005a454b53689f8de1d64aace8f858cf968) | docs(plans): mark Daily Stats engine epic and landing-fixes done | [bob-cli-6l.2.1](bob-cli-6l.2.1.md) | 2026-10-11 12:53:31 EDT |
| bob-cli | [`9be32d9`](https://github.com/bobs-org/bob-cli/commit/9be32d97e56a552d0ef1dc19f3b8eff94ce43638) | feat(stats): add the bob stats CLI (overview, show, metrics) | [bob-cli-6l.3](bob-cli-6l.3.md) | 2026-10-11 13:48:19 EDT |
| bob-cli | [`f74f3ad`](https://github.com/bobs-org/bob-cli/commit/f74f3ad305e5ecee85eef35312af918d60c6070b) | feat(stats): document the Stats child page and Browse chip | [bob-cli-6l.4](bob-cli-6l.4.md) | 2026-10-11 14:05:58 EDT |
| bob-plugins | [`bob-plugins@db91d68`](https://github.com/bobs-org/bob-plugins/commit/db91d68a8d003689835001695d7c816303f8bcb6) | feat(stats): add the Stats page data path, tiles, and table block | [bob-cli-6l.4](bob-cli-6l.4.md) | 2026-10-11 14:07:01 EDT |
| bob-cli | [`ab314c0`](https://github.com/bobs-org/bob-cli/commit/ab314c061da8da06ed1d821c2afa03979c30cb4c) | feat(stats): add schema-1 chart, daily\_points, checklist, and chore metadata | [bob-cli-6l.5.1.1](bob-cli-6l.5.1.1.md) | 2026-10-11 14:45:40 EDT |
| bob-plugins | [`bob-plugins@f3bc5e2`](https://github.com/bobs-org/bob-plugins/commit/f3bc5e27fc9699ebef58cb044525abbbea0fe4eb) | feat(bob-ledger-tools): add accessible stats charts | [bob-cli-6l.5.1.2](bob-cli-6l.5.1.2.md) | 2026-10-11 15:08:27 EDT |
| bob-plugins | [`bob-plugins@2e7f3b0`](https://github.com/bobs-org/bob-plugins/commit/2e7f3b0ff365ad5696dc4ee0d61cfd11b84c8a8b) | feat(bob-ledger-tools): render Stats metric-family context panels | [bob-cli-6l.5.1.3](bob-cli-6l.5.1.3.md) | 2026-10-11 15:23:57 EDT |
| bob-cli | [`efc5593`](https://github.com/bobs-org/bob-cli/commit/efc55932f7b055437d270d5fea37f7186ce5fd73) | docs(stats): document charts and preview workflow | [bob-cli-6l.5.1.4](bob-cli-6l.5.1.4.md) | 2026-10-11 16:21:19 EDT |
| bob-plugins | [`bob-plugins@fa7db2f`](https://github.com/bobs-org/bob-plugins/commit/fa7db2fe74ec800417df11268d1c45828a3775e2) | feat(stats): add renderer preview fixtures | [bob-cli-6l.5.1.4](bob-cli-6l.5.1.4.md) | 2026-10-11 16:22:26 EDT |
| bob-cli--plans | [`bob-cli--plans@745c113`](https://github.com/bobs-org/bob-cli--plans/commit/745c1136250cadddf7a21e58adae8bb47c346943) | docs(plans): mark the Stats charts epic plan done | [bob-cli-6l.5.1](bob-cli-6l.5.1.md) | 2026-10-11 16:45:41 EDT |
| bob-cli | [`f11ca41`](https://github.com/bobs-org/bob-cli/commit/f11ca415b6fefc329b776be081ee36fd041bcb1d) | docs(stats): cross-link CLI, Stats page, and review journal | [bob-cli-6l.6](bob-cli-6l.6.md) | 2026-10-11 17:13:06 EDT |
| bob-cli | [`a55a22e`](https://github.com/bobs-org/bob-cli/commit/a55a22e83b0361ea90795dc22f1148b4f9152066) | feat(stats): land review-journal writer vectors R20–R24 | [bob-cli-6l](README.md) | 2026-10-11 17:58:06 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-6l.3][1] | Need parent epic plan and remaining phases | 1 |
| read-by | [agent:bob-cli-6l.4][2] | Need epic scope for phase 6l.4 | 1 |
| read-by | [agent:bob-cli-6l.5.1.land][3] | Need close status, parent notes, and whether the containing epic stayed open | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6l.5.1.land/README.md

<!-- sase:referenced-by:end -->
