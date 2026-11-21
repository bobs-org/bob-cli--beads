# Bead: bob-cli-oo.2 — Quiet prose caption on every row surface

[Bead Pages](../README.md) / [bob-cli-oo](README.md) / bob-cli-oo.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5q.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5q.linker.w0.md) · **Assignee:** `bob-cli-oo.2` · **Size:** small
**Created:** 2026-11-21 12:07:07 EST · **Closed:** 2026-11-21 14:13:40 EST
**Plan:** [202611/bank\_row\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_row_notes.md)

## Description

note-caption: render notes as a muted italic dash-led caption in Live Preview, Reading view, and the queue card, with contrast-safe CSS and tests.

## Notes

[2026-11-21T19:12:31Z · bob-cli-oo.2] PROPOSED FOLLOW-UP: deploy note-caption — bob plugins sync refused for bob-ledger-tools (agent in another workspace holds an uncommitted deployed build); after it lands, run git fetch, ff to upstream, and bob plugins sync --repo <bob-plugins> --no-pull -p bob-ledger-tools

[2026-11-21T19:12:38Z · bob-cli-oo.2] PROPOSED FOLLOW-UP: npm run docs:check lint fails on bob-cli docs reference/plugins/bob-navigation-hotkeys.md (6302 words) and reference/vault-format.md (6037 words) over the 6000 cap — unrelated to this phase

[2026-11-21T19:12:46Z · bob-cli-oo.2] PROPOSED FOLLOW-UP: perf tests (200-link ledger 25 ms budget) fail only under load avg ~200 — timing flake, not caused by this phase

[2026-11-21T19:13:40Z · bob-cli-oo.2] Live Preview BankNoteWidget, Reading-view wrap with dash-less fallback, queue-card note span, contrast-safe CSS, tests (55 bank marks/cards pass; npm test all green except 2 load-sensitive perf timing tests), docs sentence. Deploy via bob plugins sync pending: refused by another agent's uncommitted ledger-tools build.

## Dependencies

- **Depends on:** [bob-cli-oo.1](bob-cli-oo.1.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-oo.3](bob-cli-oo.3.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-oo.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oo.2/README.md) | [bob-cli-oo.2](bob-cli-oo.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@d9fe19d`](https://github.com/bobs-org/bob-plugins/commit/d9fe19d8f22f73c360c30812bd5a4a1ac38ba0b8) | feat(ledger-tools): caption bank row notes as quiet prose | [bob-cli-oo.2](bob-cli-oo.2.md) | 2026-11-21 14:17:56 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-oo.2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oo.2/README.md

<!-- sase:referenced-by:end -->
