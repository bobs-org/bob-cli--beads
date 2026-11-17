# Bead: bob-cli-ms.1 — Per-record read and record fingerprint in bob records show

[Bead Pages](../README.md) / [bob-cli-ms](README.md) / bob-cli-ms.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.55.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.55.linker.w0.md) · **Assignee:** `bob-cli-ms.1` · **Size:** medium
**Created:** 2026-11-17 11:29:54 EST · **Closed:** 2026-11-17 13:38:46 EST
**Plan:** [202611/record\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_card.md)

## Description

record-read: add an optional STEM to bob records show that returns one record's typed properties with source lines, identity and other keys, findings, full ranked suggestions, and a semantic record fingerprint, read-only, with human and JSON output and docs.

## Notes

[2026-11-17T17:26:09Z · bob-cli-ms.1] Verified optional STEM on bob records show: typed properties, identity, findings, fingerprint; 6 CLI tests; live vault zettel bead_lifecycle, subscription chatgpt, restaurant mr_js_deli; docs-gen; epic-symbols empty. TYPE-only JSON unchanged. just check via prepared monitor.

[2026-11-17T17:50:11Z · bob-cli-ms.1--1] Fixed just check: records show STEM now has a RecordStem completion kinds decision; native::completion::kinds::tests all pass.

[2026-11-17T18:14:12Z · bob-cli-ms.1--2] Fixed just check flake: capture ! shell completion used the 150ms production deadline and returned empty stdout under load. Switched capture/article __complete tests to bob_completion_command (10s test deadline).

[2026-11-17T18:38:46Z · bob-cli-ms.1--3] Closed by explicit `sase stitch create -B close` after create_commit landed 99005975 ("feat(records): add per-record show STEM and fingerprint"). The commit author requested bead completion after verifying the bead scope. Reopen with `sase bead open bob-cli-ms.1` if more work remains.

## Dependencies

- **Blocks:** [bob-cli-ms.2](bob-cli-ms.2.md) ◐ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ms.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ms.1.md) | [bob-cli-ms.1](bob-cli-ms.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ms.1--3][1] | Confirm phase scope is complete before closing on host submit | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ms.1.md

<!-- sase:referenced-by:end -->
