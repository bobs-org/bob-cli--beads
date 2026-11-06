# Bead: bob-cli-hn.1 — Contract, vectors table, and decision record

[Bead Pages](../README.md) / [bob-cli-hn](README.md) / bob-cli-hn.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.191](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.191/README.md) · **Assignee:** `bob-cli-hn.1` · **Size:** medium
**Created:** 2026-11-05 18:41:46 EST · **Closed:** 2026-11-05 18:55:36 EST
**Plan:** [202611/successor\_card\_verdicts.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/successor_card_verdicts.md)

## Description

contract: write the binding bob-cli docs contract in docs/task-dependencies.md §12.22–12.23 and the §12.5/§12.13/§12.14 additions (the SV vector table, canonical copy, CLI/JSON/API shapes), plus the memory changes the accepted decisions authorize.

## Notes

[2026-11-05T23:54:36Z · bob-cli-hn.1] PROPOSED FOLLOW-UP: resolve the epic memory-authorization collision before superseding the offers decision — memory_offers_supersede=yes authorizes a supersession by a new decision record, while memory_verdict_record=no forbids creating that record; this phase left memory unchanged.

[2026-11-05T23:55:02Z · bob-cli-hn.1] PROPOSED FOLLOW-UP: docs-check still reports the four undocumented BOB_GMAIL_* names in src/native/google/profile.rs; this is unrelated to the contract and is already tracked by bob-cli-hl.1, whose note records the same clean-HEAD failure.

[2026-11-05T23:55:36Z · bob-cli-hn.1] Added the §12.5, §12.13, and §12.14 offer-close contract plus §12.22–§12.23 copy and SV vectors. git diff --check passed and epic-symbols is clean. docs-check still reports four pre-existing BOB_GMAIL_* documentation lint errors tracked by bob-cli-hl.1; memory changes were left unchanged because the final plan decisions conflict, recorded for triage.

## Dependencies

- **Blocks:** [bob-cli-hn.2](bob-cli-hn.2.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hn.4](bob-cli-hn.4.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hn.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.1/README.md) | [bob-cli-hn.1](bob-cli-hn.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`723af32`](https://github.com/bobs-org/bob-cli/commit/723af3246886bd84fba1899a4aa19f280314ca05) | feat(docs): define successor offer verdict contract | [bob-cli-hn.1](bob-cli-hn.1.md) | 2026-11-05 18:56:31 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hn.1][1] | Verify recorded phase notes before closing | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.1/README.md

<!-- sase:referenced-by:end -->
