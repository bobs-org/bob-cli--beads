# Bead: bob-cli-ir.10.1.2 — Decode records and define portable card state

[Bead Pages](../README.md) / [bob-cli-ir.10.1](bob-cli-ir.10.1.md) / bob-cli-ir.10.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ir.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.10.md) · **Assignee:** `bob-cli-ir.10.1.2` · **Size:** medium
**Created:** 2026-11-09 02:49:44 EST · **Closed:** 2026-11-09 04:04:55 EST
**Plan:** [202611/mac\_record\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_record_card.md)

## Description

card-contract: add tolerant record parse/completion/target models and process-client requests in bob-mac-capture, generate fixtures from real Bob, and implement a portable Record Card presentation and focus reducer with backward-compatibility tests.

## Notes

[2026-11-09T09:04:55Z · bob-cli-ir.10.1.2] card-contract done in bob-mac-capture: tolerant record parse/completion/target decode (CaptureRecordPresentation.swift) + CaptureModels/CaptureTarget/Candidate wiring, BobProcessClient -n/-F with unsupportedOption, cached route preserves record trailing space/continuation, Scripts/generate-record-fixtures.sh with real-Bob fixtures + old-Bob fallbacks, CaptureRecordTests 30 pass, swift test 2299 pass, docs-check + script checks pass, docs/protocol.md updated

## Dependencies

- **Depends on:** [bob-cli-ir.10.1.1](bob-cli-ir.10.1.1.md) ✓ · ⧖ 2026-11-09
- **Blocks:** [bob-cli-ir.10.1.3](bob-cli-ir.10.1.3.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ir.10.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.10.1.2/README.md) | [bob-cli-ir.10.1.2](bob-cli-ir.10.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@1e6fb18`](https://github.com/bobs-org/bob-mac-capture/commit/1e6fb187bb0a2725608255db40b8088a8ac4008f) | feat(mac-capture): decode records and define portable card state | [bob-cli-ir.10.1.2](bob-cli-ir.10.1.2.md) | 2026-11-09 04:06:33 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ir.10.1.2][1] | Need full phase details | 4 |
| read-by | [agent:bob-cli-ir.10.1.land--2][2] | Need closed child notes and outcomes before landing closeout | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ir.10.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.10.1.land.md

<!-- sase:referenced-by:end -->
