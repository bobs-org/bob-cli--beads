# Bead: bob-cli-q5 — Snoozed Tasks: plan it for today, wake it at a time

[Bead Pages](../README.md) / bob-cli-q5

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fx](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fx.md) · **Assignee:** `bob-cli-q5.land`
**Created:** 2026-11-25 10:22:52 EST
**Plan:** [202611/snoozed\_tasks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snoozed_tasks.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/snoozed_tasks.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snoozed_tasks.md

<!-- sase:links:end -->

## Description

Bryan can snooze any open, non-Event task to a clock time today from its Task Link, its definition, capture, or the CLI. While asleep the task is clearly marked with a clock and its time, stays out of Today, the walks, and plan.max_links. At its time, bob wakes it into an untimed open Pomodoro, the woken Task Link shows its wake time, and one hard-to-miss notice announces it and then goes away on its own.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-q5.1](bob-cli-q5.1.md) | bob snooze core, wake writer, and tick step | ✓ closed | large | 2026-11-25 | 1 | 0 |
| [bob-cli-q5.2](bob-cli-q5.2.md) | Snoozed rows in reconcile, walks, plan, and the agenda JSON | ◐ in_progress | large | 2026-11-25 | 1 | 0 |
| [bob-cli-q5.3](bob-cli-q5.3.md) | Capture z:\<when\> snooze token | ◐ in_progress | large | 2026-11-25 | 1 | 0 |
| [bob-cli-q5.4](bob-cli-q5.4.md) | Plugin snoozed index, exclusions, cleanup parity, and Obsidian waker | ◐ in_progress | large | 2026-11-25 | 1 | 0 |
| [bob-cli-q5.5](bob-cli-q5.5.md) | Clock marks, woken-link pills, Snoozed-row paint, and plan chip | ◐ in_progress | large | 2026-11-25 | 1 | 0 |
| [bob-cli-q5.6](bob-cli-q5.6.md) | Alt+Z Snooze Card and Task Card z | ◐ in_progress | large | 2026-11-25 | 1 | 0 |
| [bob-cli-q5.7](bob-cli-q5.7.md) | Mac Later-today band, woken accents, and exact-minute waker | ◐ in_progress | large | 2026-11-25 | 1 | 0 |
| [bob-cli-q5.8](bob-cli-q5.8.md) | Presence-aware wake notice on the Mac | ◐ in_progress | large | 2026-11-25 | 1 | 0 |
| [bob-cli-q5.9](bob-cli-q5.9.md) | Glossary, guide, decision record, and end-to-end verification | ◐ in_progress | medium | 2026-11-25 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-q5: Snoozed Tasks: plan it for today, wake it at a time [in_progress]"]
    n1["bob-cli-q5.1: bob snooze core, wake writer, and tick step [closed]"]
    n2["bob-cli-q5.1.1: Snooze wake engine for bob-cli-q5.1 [closed]"]
    n3["bob-cli-q5.1.1.1: Snooze row, clock, and resolved-state contracts [closed]"]
    n4["bob-cli-q5.1.1.2: Pure add, drop, and never-running wake planners [closed]"]
    n5["bob-cli-q5.1.1.3: Public snooze CLI and guarded write shell [closed]"]
    n6["bob-cli-q5.1.1.4: Wake receipts, notification arbitration, and first tick step [closed]"]
    n7["bob-cli-q5.1.1.5: Trailing-section writer audit and complete wake-engine verification [closed]"]
    n8["bob-cli-q5.2: Snoozed rows in reconcile, walks, plan, and the agenda JSON [in_progress]"]
    n9["bob-cli-q5.2.1: Snoozed reader integrations for bob-cli-q5.2 [in_progress]"]
    n10["bob-cli-q5.2.1.1: Share snoozed reads and preserve recovery-only reach [closed]"]
    n11["bob-cli-q5.2.1.2: Exclude planned-today tasks from freshness and walks [in_progress]"]
    n12["bob-cli-q5.2.1.3: Report the snoozed meter and nonbinding wake forecast [in_progress]"]
    n13["bob-cli-q5.2.1.4: Publish later-today agenda rows and wake provenance [in_progress]"]
    n14["bob-cli-q5.3: Capture z:&lt;when&gt; snooze token [in_progress]"]
    n15["bob-cli-q5.3.1: Capture snooze token and atomic row operations [in_progress]"]
    n16["bob-cli-q5.3.1.1: Parse snooze intents and expose editor spans [closed]"]
    n17["bob-cli-q5.3.1.2: Apply capture snooze operations atomically [closed]"]
    n18["bob-cli-q5.3.1.3: Complete snooze times and publish the capture contract [in_progress]"]
    n19["bob-cli-q5.4: Plugin snoozed index, exclusions, cleanup parity, and Obsidian waker [in_progress]"]
    n20["bob-cli-q5.5: Clock marks, woken-link pills, Snoozed-row paint, and plan chip [in_progress]"]
    n21["bob-cli-q5.6: Alt+Z Snooze Card and Task Card z [in_progress]"]
    n22["bob-cli-q5.7: Mac Later-today band, woken accents, and exact-minute waker [in_progress]"]
    n23["bob-cli-q5.8: Presence-aware wake notice on the Mac [in_progress]"]
    n24["bob-cli-q5.9: Glossary, guide, decision record, and end-to-end verification [in_progress]"]
    n0 --> n1
    n1 --> n2
    n2 --> n3
    n2 --> n4
    n2 --> n5
    n2 --> n6
    n2 --> n7
    n0 --> n8
    n8 --> n9
    n9 --> n10
    n9 --> n11
    n9 --> n12
    n9 --> n13
    n0 --> n14
    n14 --> n15
    n15 --> n16
    n15 --> n17
    n15 --> n18
    n0 --> n19
    n0 --> n20
    n0 --> n21
    n0 --> n22
    n0 --> n23
    n0 --> n24
    n1 -.-> n8
    n1 -.-> n14
    n3 -.-> n4
    n4 -.-> n5
    n5 -.-> n6
    n6 -.-> n7
    n8 -.-> n19
    n8 -.-> n22
    n10 -.-> n11
    n10 -.-> n12
    n10 -.-> n13
    n11 -.-> n12
    n12 -.-> n13
    n14 -.-> n22
    n14 -.-> n24
    n16 -.-> n17
    n17 -.-> n18
    n19 -.-> n20
    n20 -.-> n21
    n21 -.-> n24
    n22 -.-> n23
    n23 -.-> n24
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.1.md) | [bob-cli-q5.1](bob-cli-q5.1.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.1.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.1.1.1/README.md) | [bob-cli-q5.1.1.1](bob-cli-q5.1.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-q5.1.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.1.1.2/README.md) | [bob-cli-q5.1.1.2](bob-cli-q5.1.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-q5.1.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.1.1.3.md) | [bob-cli-q5.1.1.3](bob-cli-q5.1.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-q5.1.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.1.1.4/README.md) | [bob-cli-q5.1.1.4](bob-cli-q5.1.1.4.md) | 1 |
| [bbugyi200.athena.bob-cli-q5.1.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.1.1.5/README.md) | [bob-cli-q5.1.1.5](bob-cli-q5.1.1.5.md) | 1 |
| [bbugyi200.athena.bob-cli-q5.1.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.1.1.land.md) | [bob-cli-q5.1.1](bob-cli-q5.1.1.md) | 3 |
| [bbugyi200.athena.bob-cli-q5.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.2.md) | [bob-cli-q5.2](bob-cli-q5.2.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.2.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.2.1.1.md) | [bob-cli-q5.2.1.1](bob-cli-q5.2.1.1.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.2.1.2.md) | [bob-cli-q5.2.1.2](bob-cli-q5.2.1.2.md) | 2 |
| [bbugyi200.athena.bob-cli-q5.2.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.2.1.3/README.md) | [bob-cli-q5.2.1.3](bob-cli-q5.2.1.3.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.2.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.2.1.4/README.md) | [bob-cli-q5.2.1.4](bob-cli-q5.2.1.4.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.2.1.land/README.md) | [bob-cli-q5.2.1](bob-cli-q5.2.1.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.3.md) | [bob-cli-q5.3](bob-cli-q5.3.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.3.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.3.1.1/README.md) | [bob-cli-q5.3.1.1](bob-cli-q5.3.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-q5.3.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.3.1.2/README.md) | [bob-cli-q5.3.1.2](bob-cli-q5.3.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-q5.3.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.3.1.3/README.md) | [bob-cli-q5.3.1.3](bob-cli-q5.3.1.3.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.3.1.land/README.md) | [bob-cli-q5.3.1](bob-cli-q5.3.1.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.4/README.md) | [bob-cli-q5.4](bob-cli-q5.4.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.5/README.md) | [bob-cli-q5.5](bob-cli-q5.5.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.6/README.md) | [bob-cli-q5.6](bob-cli-q5.6.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.7/README.md) | [bob-cli-q5.7](bob-cli-q5.7.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.8/README.md) | [bob-cli-q5.8](bob-cli-q5.8.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.9/README.md) | [bob-cli-q5.9](bob-cli-q5.9.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.land/README.md) | [bob-cli-q5](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`cd59455`](https://github.com/bobs-org/bob-cli/commit/cd594550547b07285f54a181896b69c3233a29a3) | feat(snooze): add later-today row-model contracts, vectors, and docs | [bob-cli-q5.1.1.1](bob-cli-q5.1.1.1.md) | 2026-11-25 12:15:51 EST |
| bob-cli | [`e6eb52a`](https://github.com/bobs-org/bob-cli/commit/e6eb52a103656add99a1a49f2f0b3d791536abc4) | feat(snooze): add pure add, drop, and never-running wake planners | [bob-cli-q5.1.1.2](bob-cli-q5.1.1.2.md) | 2026-11-25 13:38:56 EST |
| bob-cli | [`68dee6e`](https://github.com/bobs-org/bob-cli/commit/68dee6e1f280f235971d55ee915ce46e82902b29) | feat(snooze): add public CLI and guarded write shell | [bob-cli-q5.1.1.3](bob-cli-q5.1.1.3.md) | 2026-11-25 16:17:12 EST |
| bob-cli | [`9dd67c6`](https://github.com/bobs-org/bob-cli/commit/9dd67c6253060c6492a19a591971f67b25b476c7) | feat(snooze): deliver wake receipts, notices, and first tick step | [bob-cli-q5.1.1.4](bob-cli-q5.1.1.4.md) | 2026-11-25 17:23:07 EST |
| bob-cli | [`6a3e5df`](https://github.com/bobs-org/bob-cli/commit/6a3e5df6a6613b57bf08b00880a6a8d1fcfa2ffb) | feat(snooze): audit trailing-section writers and complete verification | [bob-cli-q5.1.1.5](bob-cli-q5.1.1.5.md) | 2026-11-25 18:26:55 EST |
| bob-cli | [`03ca3f7`](https://github.com/bobs-org/bob-cli/commit/03ca3f7e38f5708651c5351f305c586875466319) | feat(snooze): settle notes on add and retire unwired re-export allowances | [bob-cli-q5.1.1](bob-cli-q5.1.1.md) | 2026-11-25 19:09:08 EST |
| bob-cli | [`19e7fe5`](https://github.com/bobs-org/bob-cli/commit/19e7fe54e2a638c0856d3ded57e57b2947045fb9) | fix(snooze): refuse unplaceable wake destinations without writing | [bob-cli-q5.1.1](bob-cli-q5.1.1.md) | 2026-11-25 19:27:45 EST |
| bob-cli--plans | [`bob-cli--plans@9ce9939`](https://github.com/bobs-org/bob-cli--plans/commit/9ce99398218d55ce419c52105973d45f382ab95f) | chore(plans): mark snooze wake engine plan done | [bob-cli-q5.1.1](bob-cli-q5.1.1.md) | 2026-11-25 19:28:34 EST |
| bob-cli | [`1b38663`](https://github.com/bobs-org/bob-cli/commit/1b386638ff031506bb1058853af17b9cab398281) | feat(capture): add snooze z:\<when\> grammar with drop claims | [bob-cli-q5.3.1.1](bob-cli-q5.3.1.1.md) | 2026-11-25 22:59:52 EST |
| bob-cli | [`b867865`](https://github.com/bobs-org/bob-cli/commit/b8678657640747b58ab418ef2206c86786b240db) | feat(freshness): exclude planned-today tasks from review and walks | [bob-cli-q5.2.1.2](bob-cli-q5.2.1.2.md) | 2026-11-26 03:38:14 EST |
| bob-cli | [`bbcae8e`](https://github.com/bobs-org/bob-cli/commit/bbcae8e03383b33cae1efc21856c00488fe68e16) | test(walks): distinguish ignored snooze states from reasons | [bob-cli-q5.2.1.2](bob-cli-q5.2.1.2.md) | 2026-11-26 04:01:22 EST |
| bob-cli | [`ae78dbb`](https://github.com/bobs-org/bob-cli/commit/ae78dbb2dbcd61ce5b8cc9a0dd4db904d93ea745) | feat(capture): apply snooze operations atomically | [bob-cli-q5.3.1.2](bob-cli-q5.3.1.2.md) | 2026-11-26 04:15:50 EST |
