# Bead: bob-cli-nh.3 — Day brief, summary drafting, and brief-carried instructions

[Bead Pages](../README.md) / [bob-cli-nh](README.md) / bob-cli-nh.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ef](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ef.md) · **Assignee:** `bob-cli-nh.3` · **Size:** large
**Created:** 2026-11-19 09:35:21 EST · **Closed:** 2026-11-19 15:40:17 EST
**Plan:** [202611/period\_intentions.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/period_intentions.md)

## Description

summary: add the versioned day-summary instruction asset and day brief v1. Every `bob periods brief` prints its instructions first. `bob periods draft` writes a day's summary and splits a period draft into summary plus Review body. A reflection no longer blocks a first draft. Bump the brief to v3 vocabulary, add the seven day summaries to the week brief, and ship v3 callouts. Docs.

## Notes

[2026-11-19T20:40:07Z · bob-cli-nh.3] Baseline for the docs-check lint failure: clean worktree at e7aa392d fails identically (docs/reference/mac-capture/capture-previews.md 6096 words, keyboard.md 6027 words; cap 6000) as this changed tree. My touched docs (periods.md, json-outputs.md, vault-format.md, reference/cli/periods.md) pass lint; vault-format was trimmed back inside its budget. Already tracked by bob-cli-h9 (see bob-cli-j5.1 note). No new task bead per the tale plan.

[2026-11-19T20:40:17Z · bob-cli-nh.3] Implemented plan:202611/period_summary.md. Day brief (day v1) + brief v3 with instruction-first envelopes, v3 neighbours, seven day_summaries with coverage, event counts with titles withheld; day/period draft with split summary+Review, shared eligibility, verified stamps; instructions v3 + day asset; CLI help, docs, regenerated CLI reference + v3 scaffold goldens (callout-only diff). Gates: cargo fmt clean, just lint clean, just test EXIT=0 (lib 7400 + cli 3838 + all targets), just docs-gen clean, just docs-check passes except pre-existing mac-capture budget lint proven identical on clean base e7aa392d and tracked by bob-cli-h9. No memory edits (vocabulary phase owns glossary work).

## Dependencies

- **Depends on:** [bob-cli-nh.1](bob-cli-nh.1.md) ✓ · ⧖ 2026-11-19
- **Blocks:** [bob-cli-nh.5](bob-cli-nh.5.md) ✓ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-nh.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.3.md) | [bob-cli-nh.3](bob-cli-nh.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a29a64f`](https://github.com/bobs-org/bob-cli/commit/a29a64f63884c9cfa960928c7a2d3c6b48693f36) | feat(periods): add day brief, summary drafting, and brief-carried instructions | [bob-cli-nh.3](bob-cli-nh.3.md) | 2026-11-19 16:33:50 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nh.3--1][1] | monitor just check green, need to confirm bead state before close | 1 |
| read-by | [agent:bob-cli-nh.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.3.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.land.md

<!-- sase:referenced-by:end -->
