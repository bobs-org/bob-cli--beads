# Bead: bob-cli-px — Closing an email task asks first (the Mail Close Card)

[Bead Pages](../README.md) / bob-cli-px

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fs](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fs.md) · **Assignee:** `bob-cli-px.land`
**Created:** 2026-11-24 12:22:30 EST
**Plan:** [202611/email\_task\_close\_confirmation.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/email_task_close_confirmation.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/email_task_close_confirmation.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/email_task_close_confirmation.md

<!-- sase:links:end -->

## Description

No interactive gesture in Obsidian, bob capture, or Bob Mac Capture can complete or cancel a Gmail Task without first showing one calm, beautiful confirmation card that says whose turn the thread is on and what closing it will cost; a stray Enter, Alt+[, or muscle-memory keypress keeps the task open.

## Notes

[2026-11-24T21:36:47Z · bob-cli-px.land] LAND TRIAGE (bob-cli-px.land) of every PROPOSED FOLLOW-UP:
(1) px.1 #1 and px.2 #1, just lint props/albums clippy failures: DECLINED, already fixed. Non-epic commit 3deee354 'fix(props): satisfy settings contract lint gates' resolved them, and fmt plus clippy now pass in just check on master 2b3817fe.
(2) px.3 #1 and px.4 #1, ledger-tools 25 ms perf flakes: duplicates. Corroborated with sase bead +1 on bob-cli-io (frees-marks) and bob-cli-km (event-link-times). No new task.
(3) px.6 #1, real-Obsidian trust helper leaves Settings focused: duplicate of bob-cli-ox, already +1'd by bob-cli-px.6. No new task.
(4) px.6 #2, Mac Capture CI compile error at CapturePanelController.swift:3355 (mailCloseVisible passed before moveChoiceVisible, out of CaptureKeyRoutingContext declaration order): CAUSED BY THIS EPIC (px.5, c2a44267). Still unfixed on bob-mac-capture master. Kept as epic work in the remaining-work tale.
(5) Land-agent finding, meetings::profile xelatex failures (2/4 tests fail on master): caused by active epic bob-cli-pw (pw.3, 2b3817fe). Recorded as DISCOVERED ISSUE on bob-cli-pw. Not epic work.
Read-back of the plugin source also found cycler/nav gaps against the plan, kept as epic work in the tale:
- Live Preview checkbox clicks are unguarded: posAtDOM returns a number but the code reads .line.
- Reading view treats section-relative li[data-line] as an absolute line.
- The confirm token is the exact digest, so a batch token does not cover later subset checks. Gestures re-prompt and are not all-or-nothing.
- The cycler normalizeSuccessorChoices drops nav's mailCloseConfirmed context, so the card is asked twice.
- The checkbox e2e is self-test only.
- The footer hardcodes 'y confirms' and the ⌘↵ hint.
- openingKeys are never swallowed.
- The decay card closes before a keep.
- The relation-close line identity may be read against the staged rather than the original line.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-px.1](bob-cli-px.1.md) | Shared Gmail Task close model, vectors, and contract page (bob-cli) | ✓ closed | medium | 2026-11-24 | 1 | 1 |
| [bob-cli-px.2](bob-cli-px.2.md) | bob capture refuses unconfirmed email-task closes | ✓ closed | medium | 2026-11-24 | 1 | 1 |
| [bob-cli-px.3](bob-cli-px.3.md) | Mail Close Card and guard API in Bob Navigation Hotkeys | ✓ closed | medium | 2026-11-24 | 1 | 1 |
| [bob-cli-px.4](bob-cli-px.4.md) | Task Status Cycler closes go through the guard | ✓ closed | medium | 2026-11-24 | 1 | 1 |
| [bob-cli-px.5](bob-cli-px.5.md) | Bob Mac Capture shows the Mail Close Card | ✓ closed | medium | 2026-11-24 | 1 | 1 |
| [bob-cli-px.6](bob-cli-px.6.md) | Cross-surface verification and records | ✓ closed | small | 2026-11-24 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-px: Closing an email task asks first (the Mail Close Card) [in_progress]"]
    n1["bob-cli-px.1: Shared Gmail Task close model, vectors, and contract page (bob-cli) [closed]"]
    n2["bob-cli-px.2: bob capture refuses unconfirmed email-task closes [closed]"]
    n3["bob-cli-px.3: Mail Close Card and guard API in Bob Navigation Hotkeys [closed]"]
    n4["bob-cli-px.4: Task Status Cycler closes go through the guard [closed]"]
    n5["bob-cli-px.5: Bob Mac Capture shows the Mail Close Card [closed]"]
    n6["bob-cli-px.6: Cross-surface verification and records [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n1 -.-> n2
    n1 -.-> n3
    n2 -.-> n5
    n2 -.-> n6
    n3 -.-> n4
    n4 -.-> n6
    n5 -.-> n6
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-px.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-px.1/README.md) | [bob-cli-px.1](bob-cli-px.1.md) | 1 |
| [bbugyi200.athena.bob-cli-px.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-px.2/README.md) | [bob-cli-px.2](bob-cli-px.2.md) | 1 |
| [bbugyi200.athena.bob-cli-px.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-px.3.md) | [bob-cli-px.3](bob-cli-px.3.md) | 1 |
| [bbugyi200.athena.bob-cli-px.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-px.4/README.md) | [bob-cli-px.4](bob-cli-px.4.md) | 1 |
| [bbugyi200.athena.bob-cli-px.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-px.5/README.md) | [bob-cli-px.5](bob-cli-px.5.md) | 1 |
| [bbugyi200.athena.bob-cli-px.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-px.6.md) | [bob-cli-px.6](bob-cli-px.6.md) | 0 |
| [bbugyi200.athena.bob-cli-px.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-px.land.md) | [bob-cli-px](README.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f07c239`](https://github.com/bobs-org/bob-cli/commit/f07c2395e6e30f1a60c72b59e15d5ebd32839ae4) | feat(gmail): add shared mail close card model | [bob-cli-px.1](bob-cli-px.1.md) | 2026-11-24 13:12:16 EST |
| bob-cli | [`976f53b`](https://github.com/bobs-org/bob-cli/commit/976f53ba4e6f47ca80a723ac4f1f9d94495db01a) | feat(capture)!: refuse unconfirmed Gmail Task closes | [bob-cli-px.2](bob-cli-px.2.md) | 2026-11-24 14:13:52 EST |
| bob-mac-capture | [`bob-mac-capture@c2a4426`](https://github.com/bobs-org/bob-mac-capture/commit/c2a442676baa2807b117a85411ef0865c5a5923b) | feat(mac-capture)!: show the Mail Close Card for email-task closes | [bob-cli-px.5](bob-cli-px.5.md) | 2026-11-24 14:46:24 EST |
| bob-plugins | [`bob-plugins@06f236c`](https://github.com/bobs-org/bob-plugins/commit/06f236c21942d7f42bf6445832d0b7afdd337f79) | feat(navigation): guard Gmail task closes with Mail Close Card | [bob-cli-px.3](bob-cli-px.3.md) | 2026-11-24 14:50:25 EST |
| bob-plugins | [`bob-plugins@6150d7e`](https://github.com/bobs-org/bob-plugins/commit/6150d7e65bd7b663ae87dc26bdbb2d9388a718eb) | feat(cycler): guard Gmail task closes with the Mail Close Card | [bob-cli-px.4](bob-cli-px.4.md) | 2026-11-24 15:30:59 EST |
| bob-mac-capture | [`bob-mac-capture@7d369ae`](https://github.com/bobs-org/bob-mac-capture/commit/7d369ae870a9b1fdc7b29654b08ef5171e2ccafb) | fix(mac-capture): order mailCloseVisible after moveChoiceFilterIsEmpty and drop unreachable Return | [bob-cli-px](README.md) | 2026-11-24 17:22:57 EST |
| bob-plugins | [`bob-plugins@4ecbf21`](https://github.com/bobs-org/bob-plugins/commit/4ecbf218ee100fcb26d690930de3bdaac5ac440f) | feat(plugins): finish Mail Close Card prompt-once, checkbox guard, and card spec | [bob-cli-px](README.md) | 2026-11-24 17:23:23 EST |
