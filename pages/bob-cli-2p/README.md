# Bead: bob-cli-2p — Named Pomodoro starts with \`=\<X\>#pomodoro\` in \`bob capture\` and Bob Mac Capture

[Bead Pages](../README.md) / bob-cli-2p

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.36.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.36.w0.md) · **Assignee:** `bob-cli-2p.land`
**Created:** 2026-09-29 19:17:57 EDT · **Closed:** 2026-09-29 21:30:05 EDT
**Plan:** [202609/named\_pomodoro\_start.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/named_pomodoro_start.md)

## Description

A whole capture item `=<X>#<pomodoro>` (for example `=#deep-work`, `=3#bugs`, `=-2#bugs`) starts the named Pomodoro now with `se<X>` timing, atomically. It starts the open placeholder whose name matches (whole slug, else prefix), or a new session named like a completed match, or a brand-new named session. The token composes in same-line chains (`=x =#bugs` switches sessions in one line). `bob capture-parse` and `bob capture-complete` expose it, and Bob Mac Capture completes the name with a start-aware list, highlights it, previews the session live, and teaches the syntax.

## Notes

[2026-09-30T00:54:19Z · bob-cli-2p.land] FOLLOW-UP TRIAGE (bob-cli-2p.land): (1) PROPOSED FOLLOW-UP from bob-cli-2p.1, .2 and .3, the clippy deny at tests/cli/capture/pomodoro_name.rs:808 ('|| true', overly_complex_bool_expr). Not caused by this epic; git blame points to bob-cli-28.1 via the 7d1c8dd split. Routed via /sase_new_task to active epic bob-cli-28, which owns it in its closeout, as a DISCOVERED ISSUE corroboration note. No task created; bob-cli-v tracks only the warnings. (2) Plan 'Out of scope' item 'align link forms with the again name rule': declined. The plan makes it conditional on Bryan approving the flagged decision, and there is no record of that approval. (3) Plan out-of-scope items (#name=<X> spelling, =x next-up diagnostic, Obsidian parity) are intentional non-goals; nothing filed. (4) Landing observation: =x<N>#name / =x~<K>#name gets the accurate close-selection 'is not a task list' error, not the E5 =x =#name teaching. The plan defined E5 only for =x#…, so this is per-contract; nothing filed.

[2026-09-30T00:56:20Z · bob-cli-2p.land] LAND AUDIT (bob-cli-2p.land): Reviewed all 5 closed phases and their notes, the plan, and the epic commits (cba59ee, 4a480bf, f41ab05, 8d79b1d, Mac 219983f with green CI 36651453204). Re-verified on a debug build: every worked-example row, the E1-E5, R3, R4 and W1 texts, and the chains. cargo test is green (1256 lib + 592 cli) and cargo fmt is clean. The only clippy error is the pre-existing bob-cli-28 deny, and no clippy warning comes from this epic. INTEGRATION with bob-cli-2o commits 35b96b3 (plan budget) and 754d1f3 (~<K> drop): strict mode never refuses =#name, the budget meter and warning fire, and =x~1 =#decks chains. REMAINING EPIC WORK, planned as tale sase_plan_named_start_land_closeout: (a) pomodoro_start_name 'again' rows are creates_pomodoro but lack plan_themes_after/plan_themes_cap; (b) Bob Mac Capture start-name New/Again rows never show the red after/cap badge, although the real-bob new-row fixture already carries 4/3; (c) capture --help typo =`<X>`#<pomodoro> and its bare-start placeholder claim; (d) help smoke assertions the plan asked for are missing; (e) stale docs/capture.md lines: '= never creates an entry', the strict-mode never-refused list, the completion plan_themes sentence, and =x[<N>][!<M>] missing [~<K>]. The tale ends with the epic closeout.

[2026-09-30T01:30:05Z · bob-cli-2p.land] Phase review: land agent reviewed all five phases and notes and re-verified the shipped feature: bob-cli commits cba59ee, 4a480bf, f41ab05, 8d79b1d and Mac 219983f (CI 36651453204); every worked-example row plus E1-E5, R3, R4, W1; cargo test and cargo fmt --check green; only clippy error is the pre-existing bob-cli-28 deny at tests/cli/capture/pomodoro_name.rs:808.

Integration: bob-cli-2o commits 35b96b3 (plan budget/strict) and 754d1f3 (~<K> drop): strict never refuses named starts, =x~<K> =#name chains, budget meter/warning fire. Gaps fixed here: again-row plan_themes_after/cap preview in pomodoro_start_name, Mac New/Again cap badge via shared planCapBadge helper plus 4 regenerated fixtures, capture help typo fix and new help smoke test, docs/capture.md guards/plan-budget/capture-complete corrections. New Mac CI run 36655132180 fully green.

Follow-up triage (already in epic notes): pomodoro_name.rs:808 deny routed to active epic bob-cli-28 as corroboration; link-form again alignment declined pending Bryan approval; other out-of-scope items are intentional non-goals.

Tale gates: cargo fmt --check clean; cargo test green (1267 lib + 596 cli); cargo clippy --all-targets --all-features shows only the pre-existing 808 deny, no new warnings from this tale (one manual_contains hint at capture_complete.rs:1372 predates it); Mac just-equivalent CI 36655132180 green (format-lint, build, test, bundle, smoke, install).

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-2p.1](bob-cli-2p.1.md) | \`=\<X\>#pomodoro\` grammar, chains, and named session start in \`bob capture\` | ✓ closed | medium | 2026-09-29 | 1 | 1 |
| [bob-cli-2p.2](bob-cli-2p.2.md) | Named starts in \`bob capture-parse\` | ✓ closed | medium | 2026-09-29 | 1 | 1 |
| [bob-cli-2p.3](bob-cli-2p.3.md) | \`pomodoro\_start\_name\` completion context in \`bob capture-complete\` | ✓ closed | medium | 2026-09-29 | 1 | 1 |
| [bob-cli-2p.4](bob-cli-2p.4.md) | Capture docs and README for named starts | ✓ closed | small | 2026-09-29 | 1 | 1 |
| [bob-cli-2p.5](bob-cli-2p.5.md) | Bob Mac Capture support for named starts | ✓ closed | medium | 2026-09-29 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-2p: Named Pomodoro starts with `=&lt;X&gt;#pomodoro` in `bob capture` and Bob Mac Capture [closed]"]
    n1["bob-cli-2p.1: `=&lt;X&gt;#pomodoro` grammar, chains, and named session start in `bob capture` [closed]"]
    n2["bob-cli-2p.2: Named starts in `bob capture-parse` [closed]"]
    n3["bob-cli-2p.3: `pomodoro_start_name` completion context in `bob capture-complete` [closed]"]
    n4["bob-cli-2p.4: Capture docs and README for named starts [closed]"]
    n5["bob-cli-2p.5: Bob Mac Capture support for named starts [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n1 -.-> n2
    n1 -.-> n4
    n1 -.-> n5
    n2 -.-> n3
    n2 -.-> n4
    n2 -.-> n5
    n3 -.-> n4
    n3 -.-> n5
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2p.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2p.1/README.md) | [bob-cli-2p.1](bob-cli-2p.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-2p.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2p.2/README.md) | [bob-cli-2p.2](bob-cli-2p.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-2p.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2p.3/README.md) | [bob-cli-2p.3](bob-cli-2p.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-2p.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2p.4/README.md) | [bob-cli-2p.4](bob-cli-2p.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-2p.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-2p.5.md) | [bob-cli-2p.5](bob-cli-2p.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-2p.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-2p.land.md) | [bob-cli-2p](README.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`cba59ee`](https://github.com/bobs-org/bob-cli/commit/cba59ee919fd88f886c93735688b2994c5810b39) | feat(capture): named Pomodoro starts with =\<X\>#pomodoro | [bob-cli-2p.1](bob-cli-2p.1.md) | 2026-09-29 19:32:06 EDT |
| bob-cli | [`4a480bf`](https://github.com/bobs-org/bob-cli/commit/4a480bf014d8c4448442da8e869dccbcdc624589) | feat(capture): support named pomodoro starts in editor parse | [bob-cli-2p.2](bob-cli-2p.2.md) | 2026-09-29 19:49:07 EDT |
| bob-cli | [`f41ab05`](https://github.com/bobs-org/bob-cli/commit/f41ab0550a1fe9f4ed988a3186e6d5c454f01e00) | feat(capture): add pomodoro\_start\_name completion context for =\<X\>#name | [bob-cli-2p.3](bob-cli-2p.3.md) | 2026-09-29 20:15:51 EDT |
| bob-cli | [`8d79b1d`](https://github.com/bobs-org/bob-cli/commit/8d79b1dfa9b738dae1bc626edabae2cf58836e43) | docs(capture): document =\<X\>#pomodoro named starts | [bob-cli-2p.4](bob-cli-2p.4.md) | 2026-09-29 20:29:45 EDT |
| bob-cli | [`090e3eb`](https://github.com/bobs-org/bob-cli/commit/090e3eb49ae8248c6d9e5ac9b2169ccd742a9365) | fix(capture): preview plan budget on again rows, fix named-start help and docs | [bob-cli-2p](README.md) | 2026-09-29 21:32:24 EDT |
