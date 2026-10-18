# Bead: bob-cli-9j.1 — bob: \`=\` restarts or swaps the running session

[Bead Pages](../README.md) / [bob-cli-9j](README.md) / bob-cli-9j.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.91](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.91.md) · **Assignee:** `bob-cli-9j.1` · **Size:** medium
**Created:** 2026-10-18 16:26:21 EDT · **Closed:** 2026-10-18 17:05:45 EDT
**Plan:** [202610/eq\_overrides\_running\_pomodoro.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/eq_overrides_running_pomodoro.md)

## Description

eq-overrides: route every whole-item `=` start with one running session through the existing restart/swap planners, add `override.previous.overdue`, `override.close_first`, the yellow human warning line, the hidden `--refuse-override` guard, and the state-based capture-complete override context; `==` keeps working.

## Notes

[2026-10-18T20:56:52Z · bob-cli-9j.1] PROPOSED FOLLOW-UP: skipped decisions-web record for `=` overriding the running Pomodoro behind a warning (decision_record=no)

[2026-10-18T21:05:24Z · bob-cli-9j.1] PROPOSED FOLLOW-UP: just check leftover mermaid/pandoc failures match clean-base (bob-cli-9i: Mermaid PDF tests read compressed PDF bytes as text when pdftotext is absent; pandoc_maps_every_contract_construct_to_tex also fails on base, cited on bob-cli-8w.1 / bob-cli-87.13)

[2026-10-18T21:05:45Z · bob-cli-9j.1] Whole-item `=` with one running session restarts/swaps through existing planners (swap_clock=keep). JSON carries override.previous.overdue (omit false) and override.close_first (omit idle start). Yellow ⚠ warning under header; dry-run close-first hint. Hidden --refuse-override is Io/exit 1/code pomodoro_override_refused, identical in dry-run. capture-complete override is state-based. Twin `=` vs `==` day files match. Smoked dry-run `=`/`=#bugs` JSON and --refuse-override on the worked example. No epic-symbol leftovers. just check: fmt/clippy green; leftover mermaid/pandoc failures match clean-base bob-cli-9i (pdftotext absent) and pandoc_maps_every_contract_construct_to_tex.

## Dependencies

- **Blocks:** [bob-cli-9j.2](bob-cli-9j.2.md) ✓ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-9j.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-9j.1/README.md) | [bob-cli-9j.1](bob-cli-9j.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5ec1390`](https://github.com/bobs-org/bob-cli/commit/5ec1390ee52ea1bddb1194e0ba3a29565efac77a) | feat(capture): let \`=\` restart or swap the running Pomodoro | [bob-cli-9j.1](bob-cli-9j.1.md) | 2026-10-18 17:07:14 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-9j.1][1] | Need the phase scope, DECISIONS, notes, and design file before close | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-9j.1/README.md

<!-- sase:referenced-by:end -->
