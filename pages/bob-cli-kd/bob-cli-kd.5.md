# Bead: bob-cli-kd.5 — Prove every transaction — coverage, presence, balance

[Bead Pages](../README.md) / [bob-cli-kd](README.md) / bob-cli-kd.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1be](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1be.md) · **Assignee:** `bob-cli-kd.5` · **Size:** medium
**Created:** 2026-11-11 11:24:16 EST · **Closed:** 2026-11-12 07:44:49 EST
**Plan:** [202611/bank\_daily\_acknowledgment.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_daily_acknowledgment.md)

## Description

bank-balance: derive each account's anchor from the bank's own numbers, prove coverage, presence, and balance, report possible twins, unmatched typed rows, and edited amounts, and fill account status in check, list, report, and import. Add `import -F` to restore deleted rows deliberately.

## Notes

[2026-11-12T12:39:15Z · bob-cli-kd.5] PROPOSED FOLLOW-UP: Fix the dangling plugin validation link in docs/develop/plugins/validation.md:55; it makes strict docs-check fail while lint and generated checks pass.

[2026-11-12T12:41:31Z · bob-cli-kd.5] PROPOSED FOLLOW-UP: Bring docs/reference/plugins/bob-ledger-tools.md under the 6000-word reference cap; docs lint currently reports 6012 words, and the page is unchanged by this phase.

[2026-11-12T12:44:49Z · bob-cli-kd.5] Implemented QFX anchor, coverage, balance/presence findings and derived account status across check/list/report/import; added -F missing-row restoration and docs. Verified 114 bank tests, docs-gen, cargo fmt --check, and git diff --check. docs-check remains blocked by unchanged docs/reference/plugins/bob-ledger-tools.md word cap and the dangling link in docs/develop/plugins/validation.md:55; both follow-ups are recorded.

## Dependencies

- **Depends on:** [bob-cli-kd.4](bob-cli-kd.4.md) ✓ · ⧖ 2026-11-11
- **Blocks:** [bob-cli-kd.7](bob-cli-kd.7.md) ◐ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kd.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.5/README.md) | [bob-cli-kd.5](bob-cli-kd.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kd.5][1] | Need the phase scope and design file, including epic decisions and earlier work notes | 2 |
| read-by | [agent:research.49.cdx][2] | Separate implemented daily CLI from remaining import, proof, and UI acceptance work | 1 |
| read-by | [agent:research.49.cld][3] | research: user guide for first-time bank ack and e2e test of bob-cli-kd | 1 |
| read-by | [agent:research.49.final][4] | Check sub-phase state and any notes for the consolidated kd e2e test gating | 1 |
| read-by | [agent:research.49.gem][5] | Understand phase 5 balance check | 1 |
| read-by | [agent:research.49.grk][6] | Need import, balance, and Obsidian child-epic status so the first-run guide does not promise unshipped gestures | 1 |
| read-by | [agent:research.49.mus][7] | research kd epic phase scope for user guide | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.5/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.cdx/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.cld/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.final/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.gem/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.grk/README.md
[7]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.mus/README.md

<!-- sase:referenced-by:end -->
