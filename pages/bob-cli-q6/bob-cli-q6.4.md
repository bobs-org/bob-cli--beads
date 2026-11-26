# Bead: bob-cli-q6.4 — Hide native Properties on bank.md behind the fail-open gate

[Bead Pages](../README.md) / [bob-cli-q6](README.md) / bob-cli-q6.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1g2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1g2.md) · **Assignee:** `bob-cli-q6.4` · **Size:** medium
**Created:** 2026-11-25 12:49:32 EST
**Plan:** [202611/bank\_property\_card\_fold.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_property_card_fold.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:1b2923bd61f38ece409aac18 | attached via sase artifact create --bead |
| related | file:explicit:584357fd5217b2cf25553314 | attached via sase artifact create --bead |
| related | file:explicit:8cb18931c93e107b0e3fe289 | attached via sase artifact create --bead |

_Plus 6 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

bank-takeover: spike bank.md YAML parity in real Obsidian, add bank to the 240q coordinator, acquire and release ownership from the bank host, promote the bank-native e2e to full takeover verification, flip docs, and apply the decision-gated glossary corrections.

## Notes

[2026-11-25T23:05:48Z · bob-cli-q6.4] PROPOSED FOLLOW-UP: Resolve the unchanged docs-check budget failures: docs/reference/capture-syntax.md 6058/6000, json-outputs.md 6007/6000, bob-ledger-tools.md 6040/6000, and bob-navigation-hotkeys.md 6068/6000. These same four failures and counts reproduce on the base docs; plugin-apis.md 9279/8000 is warning-only.

[2026-11-25T23:05:55Z · bob-cli-q6.4] PROPOSED FOLLOW-UP: Investigate the 8 unrelated Navigation Hotkeys unit failures exposed after rebuilding its unchanged source fragments: six task-move history/runtime tests, the routed Alt+N due inbox-row test, and splitRequirementCarry guarded Undo. This full unit run had 9676 passes and 8 failures; the performance stage passed. Related prior carry implementation coverage is bob-cli-on.11.1.4.

## Dependencies

- **Depends on:** [bob-cli-q6.3](bob-cli-q6.3.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q6.6](bob-cli-q6.6.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q6.4.md) | [bob-cli-q6.4](bob-cli-q6.4.md) | 7 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1ca74ec`](https://github.com/bobs-org/bob-cli/commit/1ca74ece68165cc6fc07af59fe4e2bedf7519f4f) | docs(bank): document evidence-gated Properties | [bob-cli-q6.4](bob-cli-q6.4.md) | 2026-11-25 18:24:50 EST |
| bob-plugins | [`bob-plugins@b2e6ea1`](https://github.com/bobs-org/bob-plugins/commit/b2e6ea1f02e1510df1c8dece7e034c32adf2101e) | feat(property-card): gate Properties takeover on evidence | [bob-cli-q6.4](bob-cli-q6.4.md) | 2026-11-25 18:29:15 EST |
| bob-plugins | [`bob-plugins@4c32842`](https://github.com/bobs-org/bob-plugins/commit/4c328428bcfbcde8943088347c04100cec78860b) | test(frontmatter): correct bank takeover matrix expectations | [bob-cli-q6.4](bob-cli-q6.4.md) | 2026-11-25 18:55:00 EST |
| bob-plugins | [`bob-plugins@13b936e`](https://github.com/bobs-org/bob-plugins/commit/13b936ea96fd36fd01735243754aefe082867a57) | fix(e2e): use active note path in bank gate probe | [bob-cli-q6.4](bob-cli-q6.4.md) | 2026-11-25 19:29:09 EST |
| bob-plugins | [`bob-plugins@996c718`](https://github.com/bobs-org/bob-plugins/commit/996c718f534801371e3601bac110a80917d3e268) | fix(bob-ledger-tools): restore bank ownership after eligibility changes | [bob-cli-q6.4](bob-cli-q6.4.md) | 2026-11-25 20:16:02 EST |
| bob-plugins | [`bob-plugins@3f9b8af`](https://github.com/bobs-org/bob-plugins/commit/3f9b8af2786efa0584f9da192d3739b4428ad757) | fix(ledger-tools): reacquire bank ownership after title mount | [bob-cli-q6.4](bob-cli-q6.4.md) | 2026-11-25 20:42:12 EST |
| bob-plugins | [`bob-plugins@dc6c76f`](https://github.com/bobs-org/bob-plugins/commit/dc6c76f4336d20482aa45a45dda97710ee8aa6e9) | fix(ledger-tools): defer bank ownership until mount settles | [bob-cli-q6.4](bob-cli-q6.4.md) | 2026-11-25 21:07:00 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.7.1.land--7][1] | Verify clean-baseline docs budget overages referenced by the docs gate | 1 |
| read-by | [agent:bob-cli-q6.4--1][2] | Need the phase scope, design file, and prior verification notes before resolving the failed real Obsidian matrix | 1 |
| read-by | [agent:bob-cli-q6.4--4][2] | Review q6.4 scope, status, descendants, and recorded acceptance criteria | 1 |
| read-by | [agent:bob-cli-q6.4--6][2] | Review assigned q6.4 acceptance scope and required close conditions | 1 |
| read-by | [agent:bob-cli-q6.4--7][2] | Need q6.4 scope and close criteria before resolving acceptance entries | 1 |
| read-by | [agent:bob-cli-q6.4--8][2] | Review q6.4 acceptance scope and prior phase evidence before classification | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ph.7.1.land.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q6.4.md

<!-- sase:referenced-by:end -->
