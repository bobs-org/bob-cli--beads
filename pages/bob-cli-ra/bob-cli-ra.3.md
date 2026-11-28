# Bead: bob-cli-ra.3 — Rail kit polish, the card-floor helper, and the tree rail adapter

[Bead Pages](../README.md) / [bob-cli-ra](README.md) / bob-cli-ra.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6o.linker.w0.md) · **Assignee:** `bob-cli-ra.3` · **Size:** medium
**Created:** 2026-11-27 15:01:37 EST · **Closed:** 2026-11-27 16:36:53 EST
**Plan:** [202611/tree\_note\_link\_walks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/tree_note_link_walks.md)

## Description

rail: add the kit's card-floor helpers, step-item wrap and tooltip support, and the pure tree rail model plus its activation, re-validation, and live-refresh mixin, all unit-tested and previewed. No card mounts it yet.

## Notes

[2026-11-27T21:36:31Z · bob-cli-ra.3] PROPOSED FOLLOW-UP: test-snooze-model-vectors canonical snooze add/drop mutation vector fails identically on the clean base (extra woke 15:32 line); track as a task bead if none exists yet.

[2026-11-27T21:36:41Z · bob-cli-ra.3] Rail ship: bob plugins sync refused by workspace-12 uncommitted deploy (c3729cf, agent still RUNNING); followed refusal protocol (git fetch, no -F, no question). Docs regenerated (docs:gen), manifest bumped to 1.172.13, build + build:check clean, focused suites 65/65 pass, preview self-test 21/21. Full npm test: only the pre-existing snooze vector fails (also fails clean); perf 28/28 pass. No card mounts the rail yet, cards byte-identical.

[2026-11-27T21:36:53Z · bob-cli-ra.3] Rail done: 240u floor helper, 240g wraps/tooltip/source polish (legacy byte-identical), 296j pure tree rail model, 296k activation/revalidation/live-refresh mixin, 378b exports, Link walk rail CSS, floor + tree-walk-rail unit tests in test:unit, 5 tree preview fixtures (self-test 21/21). Verified: build, build:check, focused 65/65 pass, full npm test only pre-existing snooze failure (fails clean too), perf 28/28 incl 30ms/8k tree build. No card mounts rail; sync deferred per refusal protocol (ws12 running).

## Dependencies

- **Depends on:** [bob-cli-ra.1](bob-cli-ra.1.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-ra.4](bob-cli-ra.4.md) ✓ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ra.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ra.3/README.md) | [bob-cli-ra.3](bob-cli-ra.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@061c41b`](https://github.com/bobs-org/bob-plugins/commit/061c41b89e162a2aa4542471c6f789c2adee83f1) | feat(ledger-tools): add tree walk rail floor helper, model, and adapter | [bob-cli-ra.3](bob-cli-ra.3.md) | 2026-11-27 16:40:24 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ra.3][1] | Need the phase scope and design file | 3 |
| read-by | [agent:bob-cli-ra.4][2] | Need rail phase notes and landed helpers before mounting rails on cards | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ra.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ra.4/README.md

<!-- sase:referenced-by:end -->
