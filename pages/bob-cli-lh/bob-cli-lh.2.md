# Bead: bob-cli-lh.2 — Shared bank badge model and painter

[Bead Pages](../README.md) / [bob-cli-lh](README.md) / bob-cli-lh.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.4l.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.4l.linker.w0.md) · **Assignee:** `bob-cli-lh.2` · **Size:** medium
**Created:** 2026-11-14 06:52:51 EST · **Closed:** 2026-11-14 07:40:15 EST
**Plan:** [202611/bank\_badge\_strip\_family.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_badge_strip_family.md)

## Description

badge-core: replace the daily chip with one pure badge model and one painter (visibility, tone, copy, tooltip, read-only target), new tokens and CSS, the stats.bank_badge key, decoder support for coverage/navigation, and migrate the daily plan host.

## Notes

[2026-11-14T12:40:15Z · bob-cli-lh.2] Implemented and built the shared Bank Badge model/painter, decoder support, navigation, styling, docs, memory glossary, and tests. Badge/decode tests, offline UI self-test, build checks, and docs checks pass. Full parallel npm test has intermittent existing 25 ms performance benchmark failures; the affected benchmark files pass individually. Obsidian runtime E2E unavailable in this environment. Epic-symbol check found no leftovers.

## Dependencies

- **Blocks:** [bob-cli-lh.3](bob-cli-lh.3.md) ✓ · ⧖ 2026-11-14
- **Blocks:** [bob-cli-lh.4](bob-cli-lh.4.md) ◐ · ⧖ 2026-11-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-lh.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lh.2/README.md) | [bob-cli-lh.2](bob-cli-lh.2.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`28f48be`](https://github.com/bobs-org/bob-cli/commit/28f48be9d37da4aea1afe95f2ffb7f966c07192b) | feat(bank): add Bank Badge glossary | [bob-cli-lh.2](bob-cli-lh.2.md) | 2026-11-14 07:43:15 EST |
| bob-plugins | [`bob-plugins@008700b`](https://github.com/bobs-org/bob-plugins/commit/008700bd3adb4db6de7f5f0dcea0406fc9f35cd4) | feat(ledger-tools): add shared Bank Badge | [bob-cli-lh.2](bob-cli-lh.2.md) | 2026-11-14 07:44:11 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-lh.2][1] | Need the phase scope, prior work notes, decisions, and design file before implementation | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-lh.2/README.md

<!-- sase:referenced-by:end -->
