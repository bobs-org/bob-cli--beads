# Bead: bob-cli-q5.5.1.1 — Snooze display contract and canonical conformance vectors

[Bead Pages](../README.md) / [bob-cli-q5.5.1](bob-cli-q5.5.1.md) / bob-cli-q5.5.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.5.md) · **Assignee:** `bob-cli-q5.5.1.1` · **Size:** small
**Created:** 2026-11-26 15:37:08 EST · **Closed:** 2026-11-26 15:57:47 EST
**Plan:** [202611/snooze\_display\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snooze_display_marks.md)

## Description

display-contract: publish docs/snooze-marks.md and machine-readable SM vectors in bob-cli before plugin implementation.

## Notes

[2026-11-26T20:57:47Z · bob-cli-q5.5.1.1] display-contract landed: docs/snooze-marks.md (476 lines, principles/placement/anatomy/strings/tooltips/navigation/liveness/toggles/history/performance + 70-vector SM-* index) and tests/fixtures/snooze/marks.json (70 vectors, unique IDs, groups definition/woken/rows/plan, schema_version 1, runners js for byte-for-byte plugin parity via BOB_CLI_DIR). Registered as contract order 61 (contracts.yml), linked from docs/snooze.md, mkdocs nav + llmstxt lists, url_contract, regenerated README/contracts page via just docs-gen, test_contracts count 61 + README SHA updated. Verified: just docs-check exit 0 (447 passed, 1 skipped), JSON parses, 70/70 IDs unique and doc<->fixture parity. No Rust/CLI changes, no version/changelog edits. No epic-symbols leftovers.

## Dependencies

- **Blocks:** [bob-cli-q5.5.1.2](bob-cli-q5.5.1.2.md) ✓ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.5.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.5.1.1/README.md) | [bob-cli-q5.5.1.1](bob-cli-q5.5.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ba21e4c`](https://github.com/bobs-org/bob-cli/commit/ba21e4c2aec89204dd7d84cd28a5f17f75d8b081) | docs(snooze): publish snooze-marks display contract and SM-\* vectors | [bob-cli-q5.5.1.1](bob-cli-q5.5.1.1.md) | 2026-11-26 15:58:49 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.5.1.1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.5.1.1/README.md

<!-- sase:referenced-by:end -->
