# Bead: bob-cli-e2 — Task root fields replace the GTD review buckets

[Bead Pages](../README.md) / bob-cli-e2

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.15o](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.15o.md) · **Assignee:** `bob-cli-e2.land`
**Created:** 2026-10-28 22:26:42 EDT · **Closed:** 2026-10-29 02:13:45 EDT
**Plan:** [202610/task\_root\_fields.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_root_fields.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/task_root_fields.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | [bead:bob-cli-e3][2] | Active epic that added theme: PLAN to gtd_daily.md and retired the daily-review suggestion step |
| related | [bead:bob-cli-e4][3] | e2.5's plugin-mirror sync hit the protection and proposed this reconcile |
| related | [bead:bob-cli-e5][4] | e2 retired homes kind review and theme source review, which made this Swift copy dead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_root_fields.md
[2]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-e3/README.md
[3]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-e4/README.md
[4]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-e5/README.md

<!-- sase:links:end -->

## Description

A task can name its root parent with `[root:: NOTE]`, rendered in Obsidian as a calm hue-dot place mark. Every daily `^gtd` task carries `[root:: gtd_daily]`, so morning review time is attributed through Task Links exactly like all other work. The `@daily` "GTD" bucket, the `@review:<NAME>` "PLAN review" buckets, review sessions, and the "daily review" theme step are gone from Rust, the Obsidian mirror, docs, and memory.

## Notes

[2026-10-29T04:28:35Z · bob-cli-dm.7.1.land] DISCOVERED ISSUE: dm.7.1 land independently reproduced the generated glossary drift proposed by bob-cli-dm.7.1.3 note #1 and bob-cli-dm.7.1.4 note #1. On clean bob-cli 8b4d1b89 and bob-plugins 21f2a0e, BOB_DOCS_BOB_PLUGINS_DIR pointing to the opened plugin checkout uv run --project tools/docs bob-docs gen --check exits 1: Plugin documentation inventory is up to date; out of date: docs/reference/glossary.md (run just docs-gen). Commit 8b4d1b89 belongs to bob-cli-e2.2 and changes only glossary/root-parent.md without regenerating its docs page. e2.4 owns remaining docs/memory retirement; regenerate the glossary with the finished root contract and verify docs-check. Same-type/all-type searches and last-week task sweep found no matching live task; routed to this causally responsible active epic instead of creating a duplicate task.

[2026-10-29T05:32:59Z · bob-cli-dm.land] DISCOVERED ISSUE (bob-cli-dm land, plugins 2e1e881 / bob-cli 511c7ad7): e2.4 retired the Rust 'daily review' theme step. Consumers that bob-cli-dm phases added after the e2 plan was written still carry a 'review' branch or copy, and the plugin-mirror phase does not name them: (1) bob-navigation-hotkeys src/313-task-card-theme-projection.js:150 returns suggestion.label || 'daily review'; (2) block-id-prompt src/085-pomodoro-link-picker-modal.js:637 comment plus docs/block-id-prompt.md:50, which still documents 'Suggested · daily review'. The plan already names 077-pomodoro-picker-intent.js:106/167, 279-plugin-task-theme-marks.js:325, and 279-plugin-task-theme-suggest.js:200; all are still present at 2e1e881. (3) Optional: bob-mac-capture Sources/CaptureCore/CaptureTaskThemePresentation.swift:10,24-25 keeps a dead 'review' -> 'daily review suggests X' case. Decoding is tolerant, so it is harmless, but it is now dead copy. Also: bob-ledger-tools in the vault is still the c59819c deploy (pre-0fb4b92 root marks; bob plugins list shows drift). The generated glossary drift is still the only failing docs-check gate at 511c7ad7: docs/reference/glossary.md is out of date against the glossary/root-parent.md strand. With it regenerated, every other gate passes (447 docs tests). bob-cli-dm did not edit any of these, to avoid colliding with in-progress e2.5.

[2026-10-29T05:57:33Z · bob-cli-e2.land] LAND TRIAGE (bob-cli-e2.land): (a) e2.5 note #1 PROPOSED FOLLOW-UP (reconcile protected bob-navigation-hotkeys deploy) -> created bob-cli-e4 (bug, small, ready). Scope widened to task-status-cycler, which is also stuck on a dirty bob-cli_12 deploy. Not caused by e2: e2's only nav-hotkeys change is dead-copy removal. The protection comes from bob-cli-cu, and the drift is mostly bob-cli-dm's Task Card work. (b) Epic note #2 item 3 (dead 'review' homes kind and 'daily review suggests' copy in bob-mac-capture) -> created bob-cli-e5 (feature, small, ready). The approved plan explicitly scoped Mac Capture out and runtime decoding is tolerant, so this is optional cleanup, not epic work. (c) Epic note #1 and note #2 glossary drift: resolved by 48da7636; bob-docs gen --check and just docs-check pass. (d) Note #2 items 1-2 (313-task-card-theme-projection.js, 085 comment, docs/block-id-prompt.md) and the plan-named 077/279 review copy: fixed in bob-plugins 06cda80. The ledger-tools deploy is now synced. (e) Remaining epic-caused work, planned as a tale: Rust task_root::is_invalid_root_value rejects whitespace, contrary to R11, the plan, and the JS mirror. pomodoro_homes/facts.rs prefilters on the literal 'root::', so a '[root :: X]' Task Link target is ignored for Pomodoro attribution while stats task metrics and the JS mirror honor it.

[2026-10-29T06:13:45Z · bob-cli-e2.land] Land verified all 5 phases against code and notes. e2.1 (818b8755): root parser, per-block facts, as-if-residence resolver, home_for_task, stats in:/parts/health lints, PT13 walk from X, shared vectors, R11. e2.2 (bob-plugins 0fb4b92): root marks in Live Preview, Reading view, and Tasks rows. e2.3 (vault b4be331d8): template plus 133 ^gtd lines backfilled with [root:: gtd_daily]; gtd_daily.md gets theme: PLAN. e2.4 (511c7ad7, breaking): no @daily, @review, short_label, SessionKind::Review, ReviewFilter, or daily-review step left in src; review_time is in:[gtd_daily]; glossary:root-parent rewritten (the only authorized memory edit; decision_record=no honored). e2.5 (bob-plugins 06cda80): homes mirror plus root-field parity test; homes and themes vectors byte-identical to bob-cli; review copy removed, including the dm-added 313/085/block-id-prompt docs; ledger-tools and block-id-prompt deployed. Epic notes #1 and #2: glossary drift fixed by 48da7636; note #2 items 1-2 fixed in 06cda80. Land gates at 48da7636: just check green (3893 lib + 2431 cli), bob-docs gen --check and just docs-check green (447), plugins build:check, npm test (4206), and validate green; live stats show worked -r 7d reads root parent gtd_daily 7h 43m with no GTD/PLAN review. Integration: the only non-epic bob-cli commit since start is ce9f9e78 (relations docs, no overlap); bob-cli-dm's bob-plugins commits 14b4fda..2e1e881 were integrated by 06cda80. Follow-ups: bob-cli-e4 (protected nav-hotkeys/task-status-cycler deploys; not epic-caused), bob-cli-e5 (Mac Capture dead review copy; plan scoped Mac out). Epic-symbols: none. Land fix: accepted interior whitespace in root values and spaced root :: keys in per-block facts per R11; just check green (3894 lib + 2431 cli) and just docs-check green (447).

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-e2.1](bob-cli-e2.1.md) | Rust root field contract and attribution | ✓ closed | medium | 2026-10-28 | 1 | 1 |
| [bob-cli-e2.2](bob-cli-e2.2.md) | Obsidian root mark | ✓ closed | medium | 2026-10-28 | 1 | 2 |
| [bob-cli-e2.3](bob-cli-e2.3.md) | Vault template and ^gtd backfill | ✓ closed | small | 2026-10-28 | 1 | 0 |
| [bob-cli-e2.4](bob-cli-e2.4.md) | Retire review buckets in Rust, docs, and memory | ✓ closed | medium | 2026-10-28 | 1 | 1 |
| [bob-cli-e2.5](bob-cli-e2.5.md) | Obsidian homes mirror and Stats cleanup | ✓ closed | medium | 2026-10-28 | 1 | 2 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-e2: Task root fields replace the GTD review buckets [closed]"]
    n1["bob-cli-e2.1: Rust root field contract and attribution [closed]"]
    n2["bob-cli-e2.2: Obsidian root mark [closed]"]
    n3["bob-cli-e2.3: Vault template and ^gtd backfill [closed]"]
    n4["bob-cli-e2.4: Retire review buckets in Rust, docs, and memory [closed]"]
    n5["bob-cli-e2.5: Obsidian homes mirror and Stats cleanup [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n1 -.-> n2
    n1 -.-> n3
    n1 -.-> n4
    n2 -.-> n5
    n3 -.-> n4
    n4 -.-> n5
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-e2.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-e2.1/README.md) | [bob-cli-e2.1](bob-cli-e2.1.md) | 1 |
| [bbugyi200.athena.bob-cli-e2.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-e2.2/README.md) | [bob-cli-e2.2](bob-cli-e2.2.md) | 2 |
| [bbugyi200.athena.bob-cli-e2.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-e2.3/README.md) | [bob-cli-e2.3](bob-cli-e2.3.md) | 0 |
| [bbugyi200.athena.bob-cli-e2.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-e2.4/README.md) | [bob-cli-e2.4](bob-cli-e2.4.md) | 1 |
| [bbugyi200.athena.bob-cli-e2.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-e2.5.md) | [bob-cli-e2.5](bob-cli-e2.5.md) | 2 |
| [bbugyi200.athena.bob-cli-e2.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-e2.land.md) | [bob-cli-e2](README.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`818b875`](https://github.com/bobs-org/bob-cli/commit/818b875556cd20643a319cae39070611d073f7c4) | feat(homes): add \[root::\] field for as-if-residence attribution | [bob-cli-e2.1](bob-cli-e2.1.md) | 2026-10-28 23:12:54 EDT |
| bob-cli | [`8b4d1b8`](https://github.com/bobs-org/bob-cli/commit/8b4d1b89a3141d1abd92baa2530af5ea93f9685b) | docs(memory): update root parent glossary for root fields | [bob-cli-e2.2](bob-cli-e2.2.md) | 2026-10-28 23:45:36 EDT |
| bob-plugins | [`bob-plugins@0fb4b92`](https://github.com/bobs-org/bob-plugins/commit/0fb4b92330bf136f3ec8fc36dde683fbcf242974) | feat(ledger-tools): render task root marks across views | [bob-cli-e2.2](bob-cli-e2.2.md) | 2026-10-28 23:53:01 EDT |
| bob-cli | [`511c7ad`](https://github.com/bobs-org/bob-cli/commit/511c7ad7b9e2a9d418b15ba5522d483c948a46f1) | feat!: retire GTD review buckets | [bob-cli-e2.4](bob-cli-e2.4.md) | 2026-10-29 00:37:34 EDT |
| bob-cli | [`48da763`](https://github.com/bobs-org/bob-cli/commit/48da7636e7eed1f32161fa039aa99b80b614b015) | docs: regenerate root parent glossary | [bob-cli-e2.5](bob-cli-e2.5.md) | 2026-10-29 01:28:29 EDT |
| bob-plugins | [`bob-plugins@06cda80`](https://github.com/bobs-org/bob-plugins/commit/06cda805dd71310c46f047ad50c514ede221b51b) | feat(plugins)!: mirror root fields and retire review buckets | [bob-cli-e2.5](bob-cli-e2.5.md) | 2026-10-29 01:30:00 EDT |
| bob-cli | [`808189c`](https://github.com/bobs-org/bob-cli/commit/808189caa8b338a25dd36dc38ae458fdc026a9c8) | fix(homes): accept spaced root names and keys per R11 | [bob-cli-e2](README.md) | 2026-10-29 02:36:00 EDT |
| bob-cli--plans | [`bob-cli--plans@e2bc881`](https://github.com/bobs-org/bob-cli--plans/commit/e2bc881d4cc7ea526f666a347ea295f3347e1e2c) | chore(plans): mark task\_root\_fields epic done | [bob-cli-e2](README.md) | 2026-10-29 02:37:36 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-dm.land][1] | Check whether root-parent epic owns plugin mirror of retired review suggestion | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-dm.land/README.md

<!-- sase:referenced-by:end -->
