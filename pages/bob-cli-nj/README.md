# Bead: bob-cli-nj — Log Recall: Ctrl+N/P phrase history for Schedule, Work, Rotten, and Cancel Log prompts

[Bead Pages](../README.md) / bob-cli-nj

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.f3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.f3.md) · **Assignee:** `bob-cli-nj.land`
**Created:** 2026-11-19 12:14:02 EST
**Plan:** [202611/log\_reason\_recall.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/log_reason_recall.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/log_reason_recall.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/log_reason_recall.md

<!-- sase:links:end -->

## Description

Every free-text prompt in Obsidian and Bob Mac Capture that writes a Schedule, Work, Rotten, or Cancel Log entry can reuse a reason typed earlier for any task in two keystrokes. Ctrl+N/P move through a visible "USED BEFORE" band that is filtered by the draft and ranked by recent and frequent use. The band fills the field, and Enter still writes exactly the text the field shows. The four histories are derived read-only from the vault by `bob logs list`, so they need no new store, have no cold start, and pick up note edits and deletions on their own.

## Notes

[2026-11-19T22:34:15Z · bob-cli-nh.4.1.land] DISCOVERED ISSUE: Landing bob-cli-nh.4.1 triaged identical PROPOSED FOLLOW-UP reports from bob-cli-nh.4.1.2 #1, .3 #1, and .4 #2. They reproduce four capture-completion failures on clean 749efc28 and ddf28f64 (three lib: drawers::bullet_starts_that_cannot_name_a_drawer_are_empty_successes, output::close_bullet_lines_suppress_wikilink_block_but_keep_note, output::close_items_and_suffixes_request_no_completion; one matching CLI complete_drawers case). Source/history review independently ties the changed WorkLog completion context to nj.6 ddf28f64; old empty-context assertions remain. Reconcile accepted Work Log behavior and these expectations without weakening suppression/candidate guarantees. No fresh full test run claimed by this lander. Task search across all statuses and last-week sweep found no matching task; this causally related active epic owns the failure, so no new task.

[2026-11-19T22:34:33Z · bob-cli-nh.4.1.land] DISCOVERED ISSUE: Docs follow-up proposed by bob-cli-nh.4.1.4 #1 duplicates ready bob-cli-jz (corroborated by this lander). Independent canonical count_words on Mac b6b7f6cf: capture-previews 6171/6000 and keyboard 6027/6000. nj.7 commit ddeab6c8 grows capture-previews from 6096 to 6171 (+75), confirmed from its parent and postimage; nj.7 note #2 acknowledges this. This epic owns integrating its added prose with the budget; jz retains inherited overages. No new task.

[2026-11-19T22:36:32Z · bob-cli-no.land] DISCOVERED ISSUE: bob-cli-no.3 note #3 reports task-status-cycler vault deployment protected as ws15 uncommitted build based on 795fad3, with bytes matching no landed commit; phase .3 deployed bob-ledger-tools but correctly left cycler alone. Active nj.4 owns cycler Log Recall work. Please reconcile/deploy that owned build through the normal guarded sync after landing; do not force over it. Attribution is the bank phase report, not a fresh deployment attempt by this lander; no new unrelated deployment task.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-nj.1](bob-cli-nj.1.md) | bob-cli: vault-derived log phrase catalog and \`bob logs list\` | ✓ closed | medium | 2026-11-19 | 1 | 1 |
| [bob-cli-nj.2](bob-cli-nj.2.md) | bob-plugins: recall store, model, band decorator, and the Work Log modals | ✓ closed | medium | 2026-11-19 | 1 | 1 |
| [bob-cli-nj.3](bob-cli-nj.3.md) | bob-plugins: Task Card picker log stages | ✓ closed | medium | 2026-11-19 | 1 | 1 |
| [bob-cli-nj.4](bob-cli-nj.4.md) | bob-plugins: Rotten keep prompts and the successor inline cancel reason | ✓ closed | medium | 2026-11-19 | 1 | 1 |
| [bob-cli-nj.5](bob-cli-nj.5.md) | bob-mac-capture: pull-in cancel reason recall | ✓ closed | medium | 2026-11-19 | 1 | 1 |
| [bob-cli-nj.6](bob-cli-nj.6.md) | bob-cli: Work Log phrase completion in capture-complete | ✓ closed | medium | 2026-11-19 | 1 | 1 |
| [bob-cli-nj.7](bob-cli-nj.7.md) | bob-mac-capture: inline Work Log recall in the completion popup | ✓ closed | medium | 2026-11-19 | 1 | 2 |
| [bob-cli-nj.8](bob-cli-nj.8.md) | Decision record, glossary term, and cross-repo docs sweep | ✓ closed | small | 2026-11-19 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-nj: Log Recall: Ctrl+N/P phrase history for Schedule, Work, Rotten, and Cancel Log prompts [in_progress]"]
    n1["bob-cli-nj.1: bob-cli: vault-derived log phrase catalog and `bob logs list` [closed]"]
    n2["bob-cli-nj.2: bob-plugins: recall store, model, band decorator, and the Work Log modals [closed]"]
    n3["bob-cli-nj.3: bob-plugins: Task Card picker log stages [closed]"]
    n4["bob-cli-nj.4: bob-plugins: Rotten keep prompts and the successor inline cancel reason [closed]"]
    n5["bob-cli-nj.5: bob-mac-capture: pull-in cancel reason recall [closed]"]
    n6["bob-cli-nj.6: bob-cli: Work Log phrase completion in capture-complete [closed]"]
    n7["bob-cli-nj.7: bob-mac-capture: inline Work Log recall in the completion popup [closed]"]
    n8["bob-cli-nj.8: Decision record, glossary term, and cross-repo docs sweep [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n0 --> n8
    n1 -.-> n2
    n1 -.-> n5
    n1 -.-> n6
    n2 -.-> n3
    n2 -.-> n4
    n3 -.-> n8
    n4 -.-> n8
    n5 -.-> n7
    n6 -.-> n7
    n7 -.-> n8
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-nj.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nj.1/README.md) | [bob-cli-nj.1](bob-cli-nj.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-nj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nj.2/README.md) | [bob-cli-nj.2](bob-cli-nj.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-nj.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nj.3/README.md) | [bob-cli-nj.3](bob-cli-nj.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-nj.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-nj.4.md) | [bob-cli-nj.4](bob-cli-nj.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-nj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nj.5/README.md) | [bob-cli-nj.5](bob-cli-nj.5.md) | 1 |
| [bbugyi200.apollo.bob-cli-nj.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nj.6/README.md) | [bob-cli-nj.6](bob-cli-nj.6.md) | 1 |
| [bbugyi200.apollo.bob-cli-nj.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-nj.7.md) | [bob-cli-nj.7](bob-cli-nj.7.md) | 0 |
| [bbugyi200.apollo.bob-cli-nj.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nj.8/README.md) | [bob-cli-nj.8](bob-cli-nj.8.md) | 1 |
| [bbugyi200.apollo.bob-cli-nj.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nj.land/README.md) | [bob-cli-nj](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`382963d`](https://github.com/bobs-org/bob-cli/commit/382963dbae5ee9a11c5492c1bf9ddb192abd3199) | feat(logs): add vault-derived phrase recall | [bob-cli-nj.1](bob-cli-nj.1.md) | 2026-11-19 14:30:15 EST |
| bob-mac-capture | [`bob-mac-capture@e58a9e2`](https://github.com/bobs-org/bob-mac-capture/commit/e58a9e27e6649b8498fb411a4a3aca87a2a3c60a) | feat(capture): pull-in cancel reason recall from vault log history | [bob-cli-nj.5](bob-cli-nj.5.md) | 2026-11-19 14:54:12 EST |
| bob-cli | [`ddf28f6`](https://github.com/bobs-org/bob-cli/commit/ddf28f64fbe831671b4c0dc438f2a9b85c7255b5) | feat(capture): add work log phrase completion | [bob-cli-nj.6](bob-cli-nj.6.md) | 2026-11-19 15:22:18 EST |
| bob-plugins | [`bob-plugins@795fad3`](https://github.com/bobs-org/bob-plugins/commit/795fad3d924de86eb3e3f5890ba4d467833d80bb) | feat(log-recall): add Work Log phrase recall to Obsidian prompts | [bob-cli-nj.2](bob-cli-nj.2.md) | 2026-11-19 15:33:44 EST |
| bob-mac-capture | [`bob-mac-capture@ddeab6c`](https://github.com/bobs-org/bob-mac-capture/commit/ddeab6c8d3e5e4400dabd569f678df5c62f2299f) | feat(capture): inline Work Log recall in the completion popup | [bob-cli-nj.7](bob-cli-nj.7.md) | 2026-11-19 15:49:25 EST |
| bob-mac-capture | [`bob-mac-capture@b6b7f6c`](https://github.com/bobs-org/bob-mac-capture/commit/b6b7f6cf23b70060c8fab0d4c088a80ed66e90e5) | fix(tests): pass work\_log response init arguments in order | [bob-cli-nj.7](bob-cli-nj.7.md) | 2026-11-19 15:57:38 EST |
| bob-plugins | [`bob-plugins@3968f0d`](https://github.com/bobs-org/bob-plugins/commit/3968f0d70e8d45a1c225a6bb111df3f1805a956e) | feat(log-recall): attach recall to Task Card picker log stages | [bob-cli-nj.3](bob-cli-nj.3.md) | 2026-11-19 16:01:14 EST |
| bob-plugins | [`bob-plugins@7eb0685`](https://github.com/bobs-org/bob-plugins/commit/7eb0685a30c13844d7dbf2546d1709e214ed3d75) | feat(plugins): add Rotten and Cancel log recall | [bob-cli-nj.4](bob-cli-nj.4.md) | 2026-11-19 20:09:35 EST |
| bob-plugins | [`bob-plugins@3d1f553`](https://github.com/bobs-org/bob-plugins/commit/3d1f553fc07a49faa0acfc07d9b4068380f41ba4) | docs(log-recall): cover plugin prompt surfaces | [bob-cli-nj.8](bob-cli-nj.8.md) | 2026-11-19 20:14:59 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nh.4.1.land][1] | Need the active Log Recall epic scope before attaching capture completion failures | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nh.4.1.land/README.md

<!-- sase:referenced-by:end -->
