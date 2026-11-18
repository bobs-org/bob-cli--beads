# Bead: bob-cli-mw — Daily Headline: one line a day, shown wherever the week looks at its days

[Bead Pages](../README.md) / bob-cli-mw

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1dq](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1dq.md) · **Assignee:** `bob-cli-mw.land`
**Created:** 2026-11-17 17:23:39 EST
**Plan:** [202611/daily\_headline.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/daily_headline.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/daily_headline.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/daily_headline.md

<!-- sase:links:end -->

## Description

Every daily note can carry one Bryan-written `**Headline:**` line naming the result that would make the day count. bob reads it (and never writes it) and serves it to the week note's Days table and strip, the weekly brief, the terminal, and the top of the Bob Mac Capture idle agenda. A concise POST checklist row in gtd_daily.md prompts it each morning.

## Notes

[2026-11-17T23:53:54Z · bob-cli-mw.land] FOLLOW-UP TRIAGE (before repair tale): Reviewed all notes on mw.1-.4 and collected exactly two PROPOSED FOLLOW-UP entries, both from mw.1. #1 json-outputs word budget declined as already resolved: later commit 3914ab50 trims the page; canonical bob_docs.markdown.count_words on current 225a6fb is 5256/6000 with both headline contracts retained. No task or reopened report. #2 records tidy catalog/completion/canonical-path omissions routed as DISCOVERED ISSUE to active causal epic bob-cli-ms with proposer attribution and current source evidence; cfc3177c predates mw and no mw file introduces these omissions. Checked task-type ci then all-task semantic search, all 68 task rows created in the last week, and 14 active epic scopes; no same-root task (4j and hp are distinct resolved defects). No new task filed. The focused cargo reproduction timed out during fresh dependency compilation, not a test failure; prior mw.1 baseline reproduction plus unchanged source establishes ownership.

[2026-11-17T23:56:21Z · bob-cli-mw.land] LAND AUDIT / REMAINING WORK: Read mw and all notes on mw.1-.4 plus plan:202611/daily_headline.md. Inspected bob-cli 2a58d067, plugin 0d2fa4be, Mac 18de389e, chezmoi aeaef838, and vault 2659779dd/31395126c in audited opened checkouts. Approved choices verified: empty template slot; #headline POST before open Morning review; obsolete clause dropped only on open occurrence; source and applied post_stages [periods, headline]; glossary exists and rejected decision strand absent. Core contracts are wired through report columns/children, brief day parts, capture --tasks, plugin views, and Mac fixed-row model/measurement/draw. Task mention scanner is task-owned, so the daily preamble does not create Task Mentions. Changes since start (3914ab50 docs trim, 9b8ab39c dot route, 225a6fb0 panel glossary; plugin c1da817/b067881 Record/Schema Card; Mac 394b344 dot route; vault count-only cb5266405) were reviewed and are independent. New active mx agenda walk marks have no landed integration yet; repair coder must recheck drift.

Remaining epic defects: daily_headline::ends_headline_paragraph absorbs + and 1) lists; replace_markdown_links leaves a stray closing paren for balanced URLs. Compiling the actual production daily_headline.rs and markdown.rs in a temporary Rust harness reproduces Ship + unrelated list, Ship 1) unrelated list, and Read the guide) from the plan examples; all 14 existing parser/markdown tests still pass. Two wiki-link walkers duplicate traversal despite the plan sharing requirement. Plugin Summary lacks full-text title, stylesheet has no headline clamp selector, and plugin docs omit Daily Headline; explicit column-headline paint invalidation and original review/day fallback precedence also need completing. Seven current period-parts tests pass but miss those cases.

Mac exact-SHA CI 44201688943 (18de389e) passed lint/build but remains in Test at last check; integrated 394b344 run 44201825837 also pending. No macOS success claimed. Existing Swift source and design tests reviewed. Full just check not run because remaining code work needs the requested plan handoff; a bounded targeted catalog test attempt timed out only compiling dependencies. No check-full. Epic-symbol audit empty; no just symvision recipe. Parent link absent. No code or memory edits made by this audit.

One medium tale, sase_plan_daily_headline_closeout.md, passed explain/edit/revalidate with zero warnings. It covers only the parser/UI/docs omissions, regression checks and deployment, existing exact-SHA Mac CI, post-audit integration, then same-turn normal mw closure, symvision if available, and status: done on plan:202611/daily_headline.md. No close step depends on the tale commit/push. Both proposed follow-ups were fully triaged in the preceding note before proposing; retain those outcomes in the eventual close note.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-mw.1](bob-cli-mw.1.md) | bob-cli reads the Daily Headline and serves it | ✓ closed | medium | 2026-11-17 | 1 | 1 |
| [bob-cli-mw.2](bob-cli-mw.2.md) | Week note Days table and strip show each day's headline | ✓ closed | small | 2026-11-17 | 1 | 0 |
| [bob-cli-mw.3](bob-cli-mw.3.md) | Headline row at the top of the Mac idle agenda | ✓ closed | medium | 2026-11-17 | 1 | 1 |
| [bob-cli-mw.4](bob-cli-mw.4.md) | Template slot, morning checklist row, and POST stage | ✓ closed | small | 2026-11-17 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-mw: Daily Headline: one line a day, shown wherever the week looks at its days [in_progress]"]
    n1["bob-cli-mw.1: bob-cli reads the Daily Headline and serves it [closed]"]
    n2["bob-cli-mw.2: Week note Days table and strip show each day's headline [closed]"]
    n3["bob-cli-mw.3: Headline row at the top of the Mac idle agenda [closed]"]
    n4["bob-cli-mw.4: Template slot, morning checklist row, and POST stage [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n1 -.-> n2
    n1 -.-> n3
    n1 -.-> n4
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-mw.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mw.1/README.md) | [bob-cli-mw.1](bob-cli-mw.1.md) | 1 |
| [bbugyi200.athena.bob-cli-mw.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mw.2.md) | [bob-cli-mw.2](bob-cli-mw.2.md) | 0 |
| [bbugyi200.athena.bob-cli-mw.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mw.3/README.md) | [bob-cli-mw.3](bob-cli-mw.3.md) | 1 |
| [bbugyi200.athena.bob-cli-mw.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mw.4/README.md) | [bob-cli-mw.4](bob-cli-mw.4.md) | 0 |
| [bbugyi200.athena.bob-cli-mw.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mw.land.md) | [bob-cli-mw](README.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2a58d06`](https://github.com/bobs-org/bob-cli/commit/2a58d06701cc74324c055970e69eaa9de8757dba) | feat(periods): serve Daily Headline on week days and capture --tasks | [bob-cli-mw.1](bob-cli-mw.1.md) | 2026-11-17 18:04:26 EST |
| bob-mac-capture | [`bob-mac-capture@18de389`](https://github.com/bobs-org/bob-mac-capture/commit/18de389ef75541ba76144470e5fb0426cccbf57b) | feat(agenda): show Daily Headline row under Today title | [bob-cli-mw.3](bob-cli-mw.3.md) | 2026-11-17 18:42:17 EST |
| bob-cli | [`ce6425f`](https://github.com/bobs-org/bob-cli/commit/ce6425f55773dda9342c7ba4078917222c6259bc) | feat(daily-headline): carry headline report integration | [bob-cli-mw](README.md) | 2026-11-18 06:57:06 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mw.3][1] | need epic scope and decisions for mac phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mw.3/README.md

<!-- sase:referenced-by:end -->
