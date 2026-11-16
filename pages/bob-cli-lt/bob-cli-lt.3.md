# Bead: bob-cli-lt.3 — The Setup header on the bank hub

[Bead Pages](../README.md) / [bob-cli-lt](README.md) / bob-cli-lt.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1co](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1co.md) · **Assignee:** `bob-cli-lt.3` · **Size:** medium
**Created:** 2026-11-15 13:16:08 EST · **Closed:** 2026-11-15 16:26:53 EST
**Plan:** [202611/bank\_setup\_render\_and\_edit.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_setup_render_and_edit.md)

## Description

setup-header: render the collapsed/expanded Setup header in both views, scope the bank row hide to it, and paint Source-mode lint.

## Notes

[2026-11-15T21:26:14Z · bob-cli-lt.3] PROPOSED FOLLOW-UP: trim 55 words from docs/bob-ledger-tools.md or raise the reference tier cap — page sits at 6055 words (cap 6000) after the required Setup header section landed; base was exactly at cap so any addition needs an offset trim elsewhere on the page or a ceiling decision (tooling forbids raising limits)

[2026-11-15T21:26:26Z · bob-cli-lt.3] PROPOSED FOLLOW-UP: docs:check also fails on docs/reference/configuration.md at 6009 words on the clean base tree (pre-existing, untouched by this phase)

[2026-11-15T21:26:36Z · bob-cli-lt.3] PROPOSED FOLLOW-UP: full-suite timing flakes in event-link-times, keep-moving-marks-surface, and off-clock-link-chips (25ms-class budgets) fail under load and pass in isolation; unrelated subsystems, no bank-setup involvement

[2026-11-15T21:26:53Z · bob-cli-lt.3] Setup header done and verified: config decode + data service fetch, model/DOM/tiles, Reading + Live Preview mount with signature repaint, surface-scoped hide (body untouched), YAML jumps, Source lint with edit mapping, queue pointer. 21 new tests pass; affected suites (marks, category card, data, decode, cards, album header, plugin build) pass; build:check, inventory check, validate, and bob plugins sync pass. Full unit suite: only unrelated load flakes (pass in isolation). docs:check still red: pre-existing configuration.md overage plus +55 words on the setup page recorded as follow-up.

## Dependencies

- **Depends on:** [bob-cli-lt.1](bob-cli-lt.1.md) ✓ · ⧖ 2026-11-15
- **Blocks:** [bob-cli-lt.6](bob-cli-lt.6.md) ✓ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-lt.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-lt.3/README.md) | [bob-cli-lt.3](bob-cli-lt.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-lt.3][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-lt.3/README.md

<!-- sase:referenced-by:end -->
