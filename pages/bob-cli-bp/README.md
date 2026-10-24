# Bead: bob-cli-bp — Day strip — a compact daily-stats receipt at the bottom of Bob daily notes

[Bead Pages](../README.md) / bob-cli-bp

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2f.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2f.linker.w1.md) · **Assignee:** `bob-cli-bp.land`
**Created:** 2026-10-24 16:30:44 EDT · **Closed:** 2026-10-24 19:11:26 EDT
**Plan:** [202610/daily\_note\_day\_strip.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/daily_note_day_strip.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/daily_note_day_strip.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/daily_note_day_strip.md

<!-- sase:links:end -->

## Description

Every canonical daily note (`YYYY/YYYYMMDD.md`) ends with a quiet, beautiful Day strip of that day's own facts (Worked, Reviewed, Done, Created, Review closed, and the area time mix). It is painted from cache in the first frame, re-runs `bob stats` only while it is on screen and the data has changed and aged, and is never written into the note.

## Notes

[2026-10-24T22:31:23Z · bryanbugyi34@gmail.com] Today's daily file is failing to open in Obsidian right now. See the 🔒 20261024\_182631.png screenshot for context. The epic lander agent should make sure this is fixed before closing this epic.

[2026-10-24T23:11:09Z · bob-cli-bp.land] FOLLOW-UP TRIAGE (land): (1) bob-cli-bp.1 note #1 inbox_route.rs test compile error — declined, already fixed on master by 3bc7e45e (commit_capture_batch(&mut batch, &vault)); just check green. (2) Skipped decision_record (bp.2 #1, bp.3 #1, bp.4 #1, bp.5 #1, bp.6 #1) — created memory task bob-cli-bs (decisions/day-strip-shows-the-days-facts.md), ready for Bryan's triage since the 'no' was an unreviewed planner default. (3) Skipped glossary_term (bp.2 #2, bp.3 #1, bp.4 #2, bp.5 #2, bp.6 #2) — created memory task bob-cli-bt (glossary/day-strip.md), linked related to bob-cli-bs. (4) Stage-ranker 16 ms perf flake (bp.2 #3, bp.3 #2-#3, bp.4 #3, bp.5 #4) — duplicate of bob-cli-3w; +1 recorded. Also: closed bob-cli-bm (same fetch-service bugs) as superseded by bob-cli-bp.2, and +1'd bob-cli-a6 (Obsidian startup smoke check) with this epic's Failed-to-open crash as impact evidence.

[2026-10-24T23:11:26Z · bob-cli-bp.land] Verified all 6 phases against plan:202610/daily_note_day_strip.md and their commits (bob-cli 0fc6ebfa, 41afa14b; bob-plugins 6ce2e17, 38b6b1b, 5f1df8b, af1e691). DECISIONS honored: no Reading view mount shipped (only the bob-day-stats fence renders there); no decisions/glossary memory edits. EPIC NOTE #1 FIXED (Today's daily note 'Failed to open'): root cause in 239-plugin-day-strip-mount.js — the StateField value is {path, day, decorations} but was provided via EditorView.decorations.from(field) without a getter, so CodeMirror's decorations facet got a plain object and EditorView construction threw 'Cannot read properties of undefined (reading isEmpty)' for EVERY Markdown editor (unit tests stub CodeMirror, so 3,647 tests passed). Fix: from(field, v => v.decorations || Decoration.none). Also fixed a plan deviation: the field read+YAML-parsed ~/.config/bob/config.yml on every doc-changing transaction; it now uses a cached stats.day_strip value refreshed at setup, by the 60 s poll, and before each strip re-check cycle. Tightened mount tests (getter asserted; zero config reads per transaction; re-check config refresh). Verified with a jsdom harness on real CodeMirror state+view: pre-fix main.js fails to open daily, past-day, source-mode, and non-daily notes; fixed build opens all, mounts the strip after the last line only for Live Preview daily notes, keeps it last after typing/appending, and reuses its DOM. bob-ledger-tools bumped to 1.67.1; npm test 3648/3648, validate 7/7, docs:check pass; deployed to apollo vault via bob plugins sync --repo <checkout> --no-pull. Mac was offline: run 'bob plugins sync' on the Mac after the bob-plugins commit lands, then reload Obsidian. bob-cli: added the planned daily_point display-rule unit test (provisional 0 -> not yet, complete 0 -> missed, provisional 1 -> met, null -> –); documented plugin-only stats.day_strip in docs/stats.md Defaults; just check and just docs-check pass. INTEGRATION: post-start commits (relation labels, pomodoro-themes, capture ||, listen, docs) don't touch stats; bob-cli config already ignores unknown stats keys; closed bob-cli-bm (same fetch-service bugs) as superseded by bp.2. Follow-ups: bob-cli-bs and bob-cli-bt (memory, from skipped decisions), +1 bob-cli-3w (perf flake), +1 bob-cli-a6 (startup smoke check), inbox_route follow-up declined as already fixed. epic-symbols: none.

## Attachments

- 🔒 20261024\_182631.png · image/png · 2854×1686 · 145.222 KiB (private attachment)

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-bp.1](bob-cli-bp.1.md) | bob stats reads "not yet" for an unmet provisional boolean | ✓ closed | small | 2026-10-24 | 1 | 1 |
| [bob-cli-bp.2](bob-cli-bp.2.md) | Stats fetch service fixes for the Stats page and the strip | ✓ closed | medium | 2026-10-24 | 1 | 1 |
| [bob-cli-bp.3](bob-cli-bp.3.md) | Day strip model, painter, styles, and preview matrix | ✓ closed | medium | 2026-10-24 | 1 | 1 |
| [bob-cli-bp.4](bob-cli-bp.4.md) | Day strip data selection, refresh policy, fence, and Stats hand-off | ✓ closed | medium | 2026-10-24 | 1 | 1 |
| [bob-cli-bp.5](bob-cli-bp.5.md) | Virtual Live Preview mount, controls, and plugin docs | ✓ closed | medium | 2026-10-24 | 1 | 1 |
| [bob-cli-bp.6](bob-cli-bp.6.md) | Day strip contract in bob-cli docs and memory | ✓ closed | small | 2026-10-24 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-bp: Day strip — a compact daily-stats receipt at the bottom of Bob daily notes [closed]"]
    n1["bob-cli-bp.1: bob stats reads \"not yet\" for an unmet provisional boolean [closed]"]
    n2["bob-cli-bp.2: Stats fetch service fixes for the Stats page and the strip [closed]"]
    n3["bob-cli-bp.3: Day strip model, painter, styles, and preview matrix [closed]"]
    n4["bob-cli-bp.4: Day strip data selection, refresh policy, fence, and Stats hand-off [closed]"]
    n5["bob-cli-bp.5: Virtual Live Preview mount, controls, and plugin docs [closed]"]
    n6["bob-cli-bp.6: Day strip contract in bob-cli docs and memory [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n1 -.-> n6
    n2 -.-> n3
    n2 -.-> n4
    n3 -.-> n4
    n4 -.-> n5
    n5 -.-> n6
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bp.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bp.1/README.md) | [bob-cli-bp.1](bob-cli-bp.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-bp.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bp.2/README.md) | [bob-cli-bp.2](bob-cli-bp.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-bp.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-bp.3.md) | [bob-cli-bp.3](bob-cli-bp.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-bp.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bp.4/README.md) | [bob-cli-bp.4](bob-cli-bp.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-bp.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-bp.5.md) | [bob-cli-bp.5](bob-cli-bp.5.md) | 1 |
| [bbugyi200.apollo.bob-cli-bp.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bp.6/README.md) | [bob-cli-bp.6](bob-cli-bp.6.md) | 1 |
| [bbugyi200.apollo.bob-cli-bp.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bp.land/README.md) | [bob-cli-bp](README.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0fc6ebf`](https://github.com/bobs-org/bob-cli/commit/0fc6ebfaccaca03e00dab4f0ee6552db2c92834c) | fix(stats): mark unmet provisional booleans not yet | [bob-cli-bp.1](bob-cli-bp.1.md) | 2026-10-24 16:51:15 EDT |
| bob-plugins | [`bob-plugins@6ce2e17`](https://github.com/bobs-org/bob-plugins/commit/6ce2e17b63f645295a5f5c0e20d47bbff2418d85) | feat(ledger-tools): per-key FIFO fetch queue with stats cache, peek and grouping | [bob-cli-bp.2](bob-cli-bp.2.md) | 2026-10-24 16:57:37 EDT |
| bob-plugins | [`bob-plugins@38b6b1b`](https://github.com/bobs-org/bob-plugins/commit/38b6b1b91aeebdfd4fa51ea85441803a36038183) | feat(stats): add Day strip model, painter, and preview matrix | [bob-cli-bp.3](bob-cli-bp.3.md) | 2026-10-24 17:36:52 EDT |
| bob-plugins | [`bob-plugins@5f1df8b`](https://github.com/bobs-org/bob-plugins/commit/5f1df8b57e307052b2e4edc5dd437b912e813d5d) | feat(ledger-tools): day strip data selection, refresh policy, fence, and Stats hand-off | [bob-cli-bp.4](bob-cli-bp.4.md) | 2026-10-24 17:57:57 EDT |
| bob-plugins | [`bob-plugins@af1e691`](https://github.com/bobs-org/bob-plugins/commit/af1e691a33b90373e8652cbb4680a72f3b1b8628) | feat(bob-ledger-tools): mount Day strip in Live Preview | [bob-cli-bp.5](bob-cli-bp.5.md) | 2026-10-24 18:22:23 EDT |
| bob-cli | [`41afa14`](https://github.com/bobs-org/bob-cli/commit/41afa14b74ac7fc6bc4b05cd80366acbc3f08511) | docs(stats): document the shipped Day strip contract | [bob-cli-bp.6](bob-cli-bp.6.md) | 2026-10-24 18:32:20 EDT |
| bob-cli | [`cf68d60`](https://github.com/bobs-org/bob-cli/commit/cf68d608998b758ef46d4d16d27a6a13d09939cb) | test(stats): pin the not-yet display rule and note plugin-only day\_strip | [bob-cli-bp](README.md) | 2026-10-24 19:12:40 EDT |
| bob-plugins | [`bob-plugins@631c5d4`](https://github.com/bobs-org/bob-plugins/commit/631c5d4c8e6324cfd6fd0ebb73b1ef571f307c34) | fix(bob-ledger-tools): stop the Day strip mount from breaking every editor | [bob-cli-bp](README.md) | 2026-10-24 19:13:35 EDT |
| bob-cli--plans | [`bob-cli--plans@9e5e7b5`](https://github.com/bobs-org/bob-cli--plans/commit/9e5e7b59d7aa8d0dc94a26df539c04f39757fec9) | chore(plans): mark daily\_note\_day\_strip done | [bob-cli-bp](README.md) | 2026-10-24 19:14:06 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-bp.2][1] | epic context | 1 |
| read-by | [agent:bob-cli-bp.4][2] | Need epic context for strip-hosts phase | 1 |
| read-by | [agent:bob-cli-bp.6][3] | epic context | 1 |
| read-by | [agent:bob-cli-bp.land][4] | Need the parent link | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bp.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bp.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bp.6/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bp.land/README.md

<!-- sase:referenced-by:end -->
