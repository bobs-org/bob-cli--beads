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

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snoozed_tasks.md

<!-- sase:links:end -->

## Description

Bryan can snooze any open, non-Event task to a clock time today from its Task Link, its definition, capture, or the CLI. While asleep the task is clearly marked with a clock and its time, stays out of Today, the walks, and plan.max_links. At its time, bob wakes it into an untimed open Pomodoro, the woken Task Link shows its wake time, and one hard-to-miss notice announces it and then goes away on its own.

## Notes

[2026-11-26T10:46:28Z · bob-cli-q5.3.1.land] DISCOVERED ISSUE: Shared relative-time wording/rounding needs an outer-epic resolution before final docs/vector rollout. Proposed by bob-cli-q5.3.1.2 note #2; this lander reviewed snooze/when.rs and docs/snooze.md. parse_relative_delta rounds the duration (ceil(delta/5)*5), then resolve_relative adds it to unrounded now: 12:03 +45m -> 12:48, +1h -> 13:03. docs/snooze.md says relative times round upward to a five-minute boundary. q5.1 note #2 already flags the same interpretation (13:02 +45m -> 13:47). Capture correctly shares the core parser and pins that result; do not introduce capture-only time semantics. Clarify the wording or change the shared rule/vectors and every consumer consistently under this outer epic. No standalone task: q5 owns the originating parser/docs.

[2026-11-26T12:30:36Z · bob-cli-ph.land] DISCOVERED ISSUE (from bob-cli-ph.land, triaging bob-cli-ph.10 PROPOSED FOLLOW-UP #4): snooze grammar commit 1b386638 (bob-cli-q5.3.1.1) set GRAMMAR_REVISION to 33 (src/native/capture_language/mod.rs:80), but current-revision prose still advertises 32 on master 4110c073: docs/capture.md:7632 ('capture-parse and capture-complete report grammar revision 32') and docs/reference/compatibility.md:71 ('report the additive top-level grammar: 32 revision'). docs/reference/json-outputs.md:50 already says grammar: 33. Neither page has a Grammar 33 history sentence for snooze z:<when>. Grammar 32 stays the correct historical drawer-cutover revision; only the current-version claim and a 33 entry need adding. just docs-check passes, so no gate catches it. No standalone task filed; owned by this snooze epic.

[2026-11-26T17:10:54Z · bob-cli-q5.4.1.land] DISCOVERED ISSUE: (found by the bob-cli-q5.4.1 land agent) bob snooze wake's deferred report omits fields docs/snooze.md promises for every wake report. src/native/snooze/cli.rs deferred_action() (from bob-cli-q5.1.1.3, commit 68dee6e1) emits only schema_version/date/now/status=deferred/daily_file/notified/wake_id, while docs/snooze.md says Wake reports status, woken, dropped, ignored, pending, next_wake_at, plan, daily_file, notified, and wake_id. Strict consumers that follow the doc reject it: the bob-ledger-tools waker decoder returns bad-shape for the real deferred envelope (reproduced with node against helpers.snoozeWakeDecodeReport on 2026-11-26). Impact: low (deferral retries next minute), but the Mac exact-minute waker (bob-cli-q5.7) and any other decoder face the same mismatch. Fix: either emit empty woken/dropped/ignored/pending, null next_wake_at and the plan block on deferred, or document the slim deferred envelope. The plugin side is being made tolerant of the current slim shape in the bob-cli-q5.4.1 landing tale.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-q5.1](bob-cli-q5.1.md) | bob snooze core, wake writer, and tick step | ✓ closed | large | 2026-11-25 | 1 | 0 |
| [bob-cli-q5.2](bob-cli-q5.2.md) | Snoozed rows in reconcile, walks, plan, and the agenda JSON | ✓ closed | large | 2026-11-25 | 1 | 0 |
| [bob-cli-q5.3](bob-cli-q5.3.md) | Capture z:\<when\> snooze token | ✓ closed | large | 2026-11-25 | 1 | 0 |
| [bob-cli-q5.4](bob-cli-q5.4.md) | Plugin snoozed index, exclusions, cleanup parity, and Obsidian waker | ✓ closed | large | 2026-11-25 | 1 | 0 |
| [bob-cli-q5.5](bob-cli-q5.5.md) | Clock marks, woken-link pills, Snoozed-row paint, and plan chip | ◐ in_progress | large | 2026-11-25 | 1 | 0 |
| [bob-cli-q5.6](bob-cli-q5.6.md) | Alt+Z Snooze Card and Task Card z | ◐ in_progress | large | 2026-11-25 | 1 | 0 |
| [bob-cli-q5.7](bob-cli-q5.7.md) | Mac Later-today band, woken accents, and exact-minute waker | ✓ closed | large | 2026-11-25 | 1 | 0 |
| [bob-cli-q5.8](bob-cli-q5.8.md) | Presence-aware wake notice on the Mac | ◐ in_progress | large | 2026-11-25 | 1 | 0 |
| [bob-cli-q5.9](bob-cli-q5.9.md) | Glossary, guide, decision record, and end-to-end verification | ◐ in_progress | medium | 2026-11-25 | 1 | 0 |

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
| [bbugyi200.athena.bob-cli-q5.2.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.2.1.3/README.md) | [bob-cli-q5.2.1.3](bob-cli-q5.2.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-q5.2.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.2.1.4/README.md) | [bob-cli-q5.2.1.4](bob-cli-q5.2.1.4.md) | 1 |
| [bbugyi200.athena.bob-cli-q5.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.2.1.land.md) | [bob-cli-q5.2.1](bob-cli-q5.2.1.md) | 2 |
| [bbugyi200.athena.bob-cli-q5.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.3.md) | [bob-cli-q5.3](bob-cli-q5.3.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.3.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.3.1.1/README.md) | [bob-cli-q5.3.1.1](bob-cli-q5.3.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-q5.3.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.3.1.2/README.md) | [bob-cli-q5.3.1.2](bob-cli-q5.3.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-q5.3.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.3.1.3.md) | [bob-cli-q5.3.1.3](bob-cli-q5.3.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-q5.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.3.1.land.md) | [bob-cli-q5.3.1](bob-cli-q5.3.1.md) | 2 |
| [bbugyi200.athena.bob-cli-q5.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.4.md) | [bob-cli-q5.4](bob-cli-q5.4.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.4.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.4.1.1.md) | [bob-cli-q5.4.1.1](bob-cli-q5.4.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-q5.4.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.4.1.2/README.md) | [bob-cli-q5.4.1.2](bob-cli-q5.4.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-q5.4.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.4.1.3/README.md) | [bob-cli-q5.4.1.3](bob-cli-q5.4.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-q5.4.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.4.1.4.md) | [bob-cli-q5.4.1.4](bob-cli-q5.4.1.4.md) | 7 |
| [bbugyi200.athena.bob-cli-q5.4.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.4.1.5/README.md) | [bob-cli-q5.4.1.5](bob-cli-q5.4.1.5.md) | 1 |
| [bbugyi200.athena.bob-cli-q5.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.4.1.land.md) | [bob-cli-q5.4.1](bob-cli-q5.4.1.md) | 3 |
| [bbugyi200.athena.bob-cli-q5.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.5.md) | [bob-cli-q5.5](bob-cli-q5.5.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.5.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.5.1.1/README.md) | [bob-cli-q5.5.1.1](bob-cli-q5.5.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-q5.5.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.5.1.2/README.md) | [bob-cli-q5.5.1.2](bob-cli-q5.5.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-q5.5.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.5.1.3/README.md) | [bob-cli-q5.5.1.3](bob-cli-q5.5.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-q5.5.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.5.1.4/README.md) | [bob-cli-q5.5.1.4](bob-cli-q5.5.1.4.md) | 1 |
| [bbugyi200.athena.bob-cli-q5.5.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.5.1.5.md) | [bob-cli-q5.5.1.5](bob-cli-q5.5.1.5.md) | 1 |
| [bbugyi200.athena.bob-cli-q5.5.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.5.1.6/README.md) | [bob-cli-q5.5.1.6](bob-cli-q5.5.1.6.md) | 1 |
| [bbugyi200.athena.bob-cli-q5.5.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.5.1.land/README.md) | [bob-cli-q5.5.1](bob-cli-q5.5.1.md) | 1 |
| [bbugyi200.athena.bob-cli-q5.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.6/README.md) | [bob-cli-q5.6](bob-cli-q5.6.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.7.md) | [bob-cli-q5.7](bob-cli-q5.7.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.7.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.7.1.1/README.md) | [bob-cli-q5.7.1.1](bob-cli-q5.7.1.1.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.7.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.7.1.2.md) | [bob-cli-q5.7.1.2](bob-cli-q5.7.1.2.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.7.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.7.1.3.md) | [bob-cli-q5.7.1.3](bob-cli-q5.7.1.3.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.7.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.7.1.land.md) | [bob-cli-q5.7.1](bob-cli-q5.7.1.md) | 1 |
| [bbugyi200.athena.bob-cli-q5.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.md) | [bob-cli-q5.8](bob-cli-q5.8.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.8.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.1.md) | [bob-cli-q5.8.1.1](bob-cli-q5.8.1.1.md) | 2 |
| [bbugyi200.athena.bob-cli-q5.8.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.8.1.2/README.md) | [bob-cli-q5.8.1.2](bob-cli-q5.8.1.2.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.8.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.3.md) | [bob-cli-q5.8.1.3](bob-cli-q5.8.1.3.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.8.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.4.md) | [bob-cli-q5.8.1.4](bob-cli-q5.8.1.4.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.8.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.8.1.5/README.md) | [bob-cli-q5.8.1.5](bob-cli-q5.8.1.5.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.8.1.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.6.1.md) | [bob-cli-q5.8.1.6.1](bob-cli-q5.8.1.6.1.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.8.1.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.8.1.6.2/README.md) | [bob-cli-q5.8.1.6.2](bob-cli-q5.8.1.6.2.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.8.1.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.8.1.6.3/README.md) | [bob-cli-q5.8.1.6.3](bob-cli-q5.8.1.6.3.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.8.1.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.8.1.6.4/README.md) | [bob-cli-q5.8.1.6.4](bob-cli-q5.8.1.6.4.md) | 0 |
| [bbugyi200.athena.bob-cli-q5.8.1.6.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.8.1.6.5/README.md) | [bob-cli-q5.8.1.6.5](bob-cli-q5.8.1.6.5.md) | 0 |

… and 4 more agents

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
| bob-cli | [`4a81217`](https://github.com/bobs-org/bob-cli/commit/4a8121734d0b16b54d377c81708c7671a2d8ee76) | feat(plan): add snoozed forecast enrichment and cap lint | [bob-cli-q5.2.1.3](bob-cli-q5.2.1.3.md) | 2026-11-26 05:01:32 EST |
| bob-cli | [`712d69d`](https://github.com/bobs-org/bob-cli/commit/712d69d9583cf80896879b501b0a9c886bdde2a4) | feat(capture): add snooze completion token | [bob-cli-q5.3.1.3](bob-cli-q5.3.1.3.md) | 2026-11-26 05:38:58 EST |
| bob-cli | [`f32e774`](https://github.com/bobs-org/bob-cli/commit/f32e774c92ec7ae564c5f6926563bd2a8adef772) | feat(agenda): publish snoozed rows and wake provenance | [bob-cli-q5.2.1.4](bob-cli-q5.2.1.4.md) | 2026-11-26 05:59:33 EST |
| bob-cli | [`7048c5c`](https://github.com/bobs-org/bob-cli/commit/7048c5c489ebadcb577ad1281a4c3fb85c2190de) | feat(capture): finish snooze drop preview parity and completion alias merge | [bob-cli-q5.3.1](bob-cli-q5.3.1.md) | 2026-11-26 06:35:24 EST |
| bob-cli--plans | [`bob-cli--plans@4e1ba6a`](https://github.com/bobs-org/bob-cli--plans/commit/4e1ba6af01afcfed3456b0fd196e3bc12e6f45c1) | docs(plans): close capture snooze token and closeout tales | [bob-cli-q5.3.1](bob-cli-q5.3.1.md) | 2026-11-26 06:36:19 EST |
| bob-cli | [`9778a94`](https://github.com/bobs-org/bob-cli/commit/9778a94d38d986ecb4562816d99d11aa0d3d7073) | feat(snooze): integrate recovery rows into today planning | [bob-cli-q5.2.1](bob-cli-q5.2.1.md) | 2026-11-26 07:44:10 EST |
| bob-cli--plans | [`bob-cli--plans@bf9641d`](https://github.com/bobs-org/bob-cli--plans/commit/bf9641dd4ff16d757c4b67e1cd34e614c3b19c4d) | docs(plan): mark snoozed reader implementation complete | [bob-cli-q5.2.1](bob-cli-q5.2.1.md) | 2026-11-26 07:45:01 EST |
| bob-plugins | [`bob-plugins@a14ccc4`](https://github.com/bobs-org/bob-plugins/commit/a14ccc4658e4ae0f005efae8a6a9f78dfe6e35c0) | feat(snooze): add shared JavaScript row and clock model | [bob-cli-q5.4.1.1](bob-cli-q5.4.1.1.md) | 2026-11-26 08:24:16 EST |
| bob-plugins | [`bob-plugins@7d8a7d4`](https://github.com/bobs-org/bob-plugins/commit/7d8a7d4ac876740b45ee596e556f9d9519f489e1) | feat(snooze): add snoozed planned-today cache and exclusions | [bob-cli-q5.4.1.2](bob-cli-q5.4.1.2.md) | 2026-11-26 09:09:42 EST |
| bob-plugins | [`bob-plugins@1770259`](https://github.com/bobs-org/bob-plugins/commit/1770259cf0b3088d640d44cf00d16027af23a7a2) | feat(navigation): compose Snoozed-row removal into deferred cleanup, Alt+N, and decay \| Snoozed-row explicit removal composes into planDeferredPomodoroLinkCleanup with distinct reporting; offset callers count both passes; Alt+N on a Snoozed row releases through the link transaction; Next-to-Ready decay folds the cleanup while WIP-to-Next preserves the snooze; 14 regression tests. \| SASE\_BEAD=\[bob-cli-q5.4.1.3\] | [bob-cli-q5.4.1.3](bob-cli-q5.4.1.3.md) | 2026-11-26 09:39:07 EST |
| bob-plugins | [`bob-plugins@1a65c42`](https://github.com/bobs-org/bob-plugins/commit/1a65c421395564b0d668cf9edfe8cab2a5aecc97) | feat(snoozed): link active rows to Pomodoros and prune on Done | [bob-cli-q5.4.1.4](bob-cli-q5.4.1.4.md) | 2026-11-26 10:16:35 EST |
| bob-plugins | [`bob-plugins@2744791`](https://github.com/bobs-org/bob-plugins/commit/274479191b06f18bb02aa1ad4494edba01e40577) | fix(snoozed-tasks): preserve note transfer during link-now | [bob-cli-q5.4.1.4](bob-cli-q5.4.1.4.md) | 2026-11-26 10:31:52 EST |
| bob-plugins | [`bob-plugins@4e0a8fd`](https://github.com/bobs-org/bob-plugins/commit/4e0a8fd0e96453a6c92ca8293dfa0c964d1f6111) | fix(plugins): preserve notes when linking snoozed tasks | [bob-cli-q5.4.1.4](bob-cli-q5.4.1.4.md) | 2026-11-26 10:42:06 EST |
| bob-plugins | [`bob-plugins@c534666`](https://github.com/bobs-org/bob-plugins/commit/c5346664d0584d8f93a5e36354a4992f41c8aa47) | fix(plugins): preserve link edits and repair full-test regressions | [bob-cli-q5.4.1.4](bob-cli-q5.4.1.4.md) | 2026-11-26 10:58:35 EST |
| bob-plugins | [`bob-plugins@db4bfd7`](https://github.com/bobs-org/bob-plugins/commit/db4bfd7ba2c58c22314ca15f58270fb99b5ceb4e) | fix(bob-ledger-tools): regenerate stale generated bundle | [bob-cli-q5.4.1.4](bob-cli-q5.4.1.4.md) | 2026-11-26 11:06:03 EST |
| bob-plugins | [`bob-plugins@86f5f34`](https://github.com/bobs-org/bob-plugins/commit/86f5f3409ff5594fe9da2830c69096a3e86531bb) | fix(ledger-tools): restore bank setup live preview fallback | [bob-cli-q5.4.1.4](bob-cli-q5.4.1.4.md) | 2026-11-26 11:15:52 EST |
| bob-plugins | [`bob-plugins@0d82297`](https://github.com/bobs-org/bob-plugins/commit/0d822970ac67951dc6b65c8553b8edf5afe6779b) | fix(ledger-tools): restore Bank Setup live preview anchor | [bob-cli-q5.4.1.4](bob-cli-q5.4.1.4.md) | 2026-11-26 11:26:42 EST |
| bob-plugins | [`bob-plugins@e36ddc6`](https://github.com/bobs-org/bob-plugins/commit/e36ddc686f890c72291002cc6d51676148a5bb0b) | feat(ledger-tools): add desktop snooze wake trigger | [bob-cli-q5.4.1.5](bob-cli-q5.4.1.5.md) | 2026-11-26 11:56:54 EST |
| bob-cli--plans | [`bob-cli--plans@d928866`](https://github.com/bobs-org/bob-cli--plans/commit/d9288663bba8ea4a363cc8ae7f5078de5b7c38e0) | docs(plans): mark mac snoozed agenda done | [bob-cli-q5.7.1](bob-cli-q5.7.1.md) | 2026-11-26 12:46:05 EST |
| bob-cli | [`3659edc`](https://github.com/bobs-org/bob-cli/commit/3659edc091409eed14ec8f0a316eedff400156bb) | feat(snooze): add wake notice ownership and eligibility fields | [bob-cli-q5.8.1.1](bob-cli-q5.8.1.1.md) | 2026-11-26 13:18:07 EST |
| bob-plugins | [`bob-plugins@d7875aa`](https://github.com/bobs-org/bob-plugins/commit/d7875aac6d1844cdb60fdc35a25a0c2e2d6e6a65) | feat(snooze): land plugin plumbing behavior | [bob-cli-q5.4.1](bob-cli-q5.4.1.md) | 2026-11-26 13:38:14 EST |
| bob-cli | [`59037b2`](https://github.com/bobs-org/bob-cli/commit/59037b2343f0b15cf7d98c5acdaf7223028e3d1c) | fix(snooze): correct test paths and anonymize vault example | [bob-cli-q5.8.1.1](bob-cli-q5.8.1.1.md) | 2026-11-26 14:06:20 EST |
| bob-plugins | [`bob-plugins@0bae838`](https://github.com/bobs-org/bob-plugins/commit/0bae8384b586811b8a5a34afd8f3e32f58df7442) | fix(task-status-cycler): preserve snooze during Done recovery | [bob-cli-q5.4.1](bob-cli-q5.4.1.md) | 2026-11-26 15:14:58 EST |
| bob-cli--plans | [`bob-cli--plans@69ff419`](https://github.com/bobs-org/bob-cli--plans/commit/69ff419e5536eebe0ae2ec76a62674a43728ea02) | docs(plan): mark snooze plugin epic complete | [bob-cli-q5.4.1](bob-cli-q5.4.1.md) | 2026-11-26 15:17:25 EST |
| bob-cli | [`ba21e4c`](https://github.com/bobs-org/bob-cli/commit/ba21e4c2aec89204dd7d84cd28a5f17f75d8b081) | docs(snooze): publish snooze-marks display contract and SM-\* vectors | [bob-cli-q5.5.1.1](bob-cli-q5.5.1.1.md) | 2026-11-26 15:58:49 EST |
| bob-plugins | [`bob-plugins@27157a4`](https://github.com/bobs-org/bob-plugins/commit/27157a491ee99e42787aceb4fdeeee896ffee6f4) | feat(snooze): add alarm-clock definition marks and refresh lifecycle | [bob-cli-q5.5.1.2](bob-cli-q5.5.1.2.md) | 2026-11-26 16:22:06 EST |
| bob-plugins | [`bob-plugins@7291726`](https://github.com/bobs-org/bob-plugins/commit/7291726060114bb5ba920b075b07789622e25a52) | feat(snooze): add woken task link pills | [bob-cli-q5.5.1.3](bob-cli-q5.5.1.3.md) | 2026-11-26 17:41:55 EST |
| bob-plugins | [`bob-plugins@514f799`](https://github.com/bobs-org/bob-plugins/commit/514f7992af9ff5a6fa754a24d95687bcf4b144b2) | feat(snooze): paint Snoozed rows and heading summaries | [bob-cli-q5.5.1.4](bob-cli-q5.5.1.4.md) | 2026-11-26 18:36:55 EST |
| bob-plugins | [`bob-plugins@b7f17a5`](https://github.com/bobs-org/bob-plugins/commit/b7f17a51a58cdb44608df3fe48b689fba1005f87) | feat(snooze): add independent plan meter and wake forecast | [bob-cli-q5.5.1.5](bob-cli-q5.5.1.5.md) | 2026-11-26 19:06:55 EST |
| bob-plugins | [`bob-plugins@73d028e`](https://github.com/bobs-org/bob-plugins/commit/73d028e5f22141962c6968edc5108a6ebe37f304) | feat(snooze): add Obsidian visual-proof e2e and fix display integration defects | [bob-cli-q5.5.1.6](bob-cli-q5.5.1.6.md) | 2026-11-26 21:32:16 EST |
| bob-cli | [`dfb5e75`](https://github.com/bobs-org/bob-cli/commit/dfb5e7550051ce797bcb7d2de665900c0eaf2fde) | docs(snooze): describe the landed snooze-marks mirror and cross-link Today marks and plan | [bob-cli-q5.5.1](bob-cli-q5.5.1.md) | 2026-11-26 22:46:13 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.land][1] | Check whether the snooze epic already tracks grammar-33 doc drift | 1 |
| read-by | [agent:bob-cli-q5.7.1.land--4][2] | confirm outer epic left open | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ph.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.7.1.land.md

<!-- sase:referenced-by:end -->
