# Bead: bob-cli-9j.3 — docs: teach the \`=\` override

[Bead Pages](../README.md) / [bob-cli-9j](README.md) / bob-cli-9j.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.91](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.91.md) · **Assignee:** `bob-cli-9j.3` · **Size:** medium
**Created:** 2026-10-18 16:26:21 EDT · **Closed:** 2026-10-18 18:40:40 EDT
**Plan:** [202610/eq\_overrides\_running\_pomodoro.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/eq_overrides_running_pomodoro.md)

## Description

docs: rewrite the Pomodoro start, named-start, and override sections of docs/capture.md plus README.md around `=`, document the new JSON fields, the warning line, `--refuse-override`, and the retired `==` row, quoting bob's real output.

## Notes

[2026-10-18T22:40:16Z · bob-cli-9j.3] PROPOSED FOLLOW-UP: Add the accepted whole-item `=` override policy to the decisions memory web — this phase skipped the strand because the epic decision_record answer is no.

[2026-10-18T22:40:40Z · bob-cli-9j.3] Rewrote docs/capture.md and README.md for the  override, JSON fields, warning, hidden guard, and retired ; checked quoted Bob output from this checkout, README.md:402:| `==` / `==<X>` / `==[<X>]#pomodoro` | Retired: `` `==` is retired: `=` restarts or swaps the running Pomodoro by itself; write `=` ``; change the doubled prefix to one `=` to get the corresponding start (quote in zsh) |
docs/capture.md:117:| `==` / `==<X>` / `==[<X>]#name` | Retired. For example, `` `==` is retired: `=` restarts or swaps the running Pomodoro by itself; write `=` ``; `==3` gives the same message and teaches `=3`; other claimed forms teach their one-`=` rewrite |
docs/capture.md:176:| `==` | Retired: `` `==` is retired: `=` restarts or swaps the running Pomodoro by itself; write `=` `` |
docs/capture.md:177:| `==3` | Retired: `` `==3` is retired: `=` restarts or swaps the running Pomodoro by itself; write `=3` `` |
docs/capture.md:178:| `==#bugs` | Retired; Bob removes one leading `=` and prints the corresponding rewrite (`=#bugs`) |
docs/capture.md:180:| `==important== thing`, `==foo`, `== foo`, `===` | Ordinary task text; `==` is retired, and a bare `==` run followed by prose stays prose, which protects Obsidian highlights |
docs/capture.md:181:| `==x` | Error: `` `==x` is not a close: close the running Pomodoro with `x` `` |
docs/capture.md:227:| `==#bugs@3` | Retired: `` `==#bugs@3` is retired: `=` restarts or swaps the running Pomodoro by itself; write `=#bugs@3` `` (`=3#bugs` is equivalent) |
docs/capture.md:233:| `==#bugs@` | Retired: `` `==#bugs@` is retired: `=` restarts or swaps the running Pomodoro by itself; write `=#bugs@` `` |
docs/capture.md:1608:- Whole-item `x*…` / `x*` are close park operators. `==*` is not a
docs/capture.md:1637:| `==*` | Error: `` `==*` is not a close: close the running Pomodoro with `x*` `` |
docs/capture.md:2554:prose. The retired `==` spelling stays prose when followed by more text,
docs/capture.md:2555:which protects Obsidian highlight syntax; a claimed `==` start token gets
docs/capture.md:3078:| `==x` | `` `==x` is not a close: close the running Pomodoro with `x` `` |
docs/capture.md:3079:| `==X1` | `` `==X1` is not a close: close the running Pomodoro with `x1` `` |
docs/capture.md:3080:| `==*` | `` `==*` is not a close: close the running Pomodoro with `x*` `` |
docs/capture.md:3081:| `==!2` | `` `==!2` is not a close: close the running Pomodoro with `x!2` `` |
docs/capture.md:3113:relationship. (`==x` is a claimed near miss teaching the `x` close, never
docs/capture.md:5137:starts either. A claimed `==` start form is retired: `capture-parse` reports
docs/capture.md:5139:including a rewrite that removes one leading `=`. For example, `==` reports
docs/capture.md:5140:`` `==` is retired: `=` restarts or swaps the running Pomodoro by itself; write `=` ``.
docs/capture.md:5141:A bare `==` followed by prose stays prose, protecting Obsidian highlights
docs/capture.md:5142:(`==important== thing`, `==foo`, `== foo`, `===`, and mid-body `Plan ==3`).
docs/capture.md:5143:The claimed close near misses `==x`, `==X1`, `==*`, and `==!2` report that
docs/capture.md:5145:chain such as `x ==`, the `==` token fails on its own range with the retired-
docs/capture.md:6157:`=#NAME~K` drops by those same lineup numbers; `==#NAME~K` is retired. `--all --tasks`, , and No --epic-symbol entries in this working tree. (no leftovers).

[2026-10-18T22:41:08Z · bob-cli-9j.3] Verification correction — rewrote docs/capture.md and README.md; confirmed restart, swap, overdue warning, refusal JSON, retired-form errors, same-name refusal, and capture-complete context from Bob built at this checkout. The == audit found only retired-form docs, close teaching errors, and highlight examples; git diff --check passed; epic-symbols reported no entries.

## Dependencies

- **Depends on:** [bob-cli-9j.2](bob-cli-9j.2.md) ✓ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-9j.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-9j.3/README.md) | [bob-cli-9j.3](bob-cli-9j.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ec9009f`](https://github.com/bobs-org/bob-cli/commit/ec9009fdb20eab43ac891b94ef2ddb2880afa19d) | docs(capture): document Pomodoro overrides | [bob-cli-9j.3](bob-cli-9j.3.md) | 2026-10-18 18:42:02 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-9j.3][1] | Need the phase scope and design file | 3 |
| read-by | [agent:bob-cli-9j.land--1][2] | Need unchanged phase verification notes and prior commit references for final epic closure. | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-9j.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-9j.land.md

<!-- sase:referenced-by:end -->
