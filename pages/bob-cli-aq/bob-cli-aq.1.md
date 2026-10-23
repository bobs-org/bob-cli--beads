# Bead: bob-cli-aq.1 — The one-key roll command in bob-navigation-hotkeys

[Bead Pages](../README.md) / [bob-cli-aq](README.md) / bob-cli-aq.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.132](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.132.md) · **Assignee:** `bob-cli-aq.1` · **Size:** medium
**Created:** 2026-10-23 06:34:43 EDT · **Closed:** 2026-10-23 07:13:13 EDT
**Plan:** [202610/quick\_roll\_alt\_p.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/quick_roll_alt_p.md)

## Description

quick-roll-key: add the Task card roll-by-recommendation command on the chosen key, run it as a one-shot Task Card intent that stays invisible unless input is needed, alias the key inside the card, rebind the vault hotkey, and document it.

## Notes

[2026-10-23T11:10:47Z · bob-cli-aq.1--1] PROPOSED FOLLOW-UP: bob-plugins npm test reports six failures, reproduced unchanged on clean base 477af35: four unblocked-glyph cases are tracked by bob-cli-6v, the decision-card Keep notice case by bob-cli-6w, and the reverse project conversion BLOCKS-link case by bob-cli-7i. The 11 quick-roll tests pass.

[2026-10-23T11:13:13Z · bob-cli-aq.1--1] Implemented and deployed the Alt+P one-key Task Card roll; focused quick-roll tests (11), plugin build, validate, and docs:check pass. The six full-suite failures reproduce on clean base 477af35 and are recorded against bob-cli-6v, bob-cli-6w, and bob-cli-7i. Cleared the template Alt+P binding and verified vault-sync pushed it with local and remote SHAs matching.

## Dependencies

- **Blocks:** [bob-cli-aq.2](bob-cli-aq.2.md) ✓ · ⧖ 2026-10-23
- **Blocks:** [bob-cli-aq.4](bob-cli-aq.4.md) ✓ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-aq.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-aq.1.md) | [bob-cli-aq.1](bob-cli-aq.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@92d5809`](https://github.com/bobs-org/bob-plugins/commit/92d5809aa0d12c1d1c00ee1ad1d1302619fe48d2) | feat(nav): add Alt+P quick roll command | [bob-cli-aq.1](bob-cli-aq.1.md) | 2026-10-23 07:14:01 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-aq.1--1][1] | Need the phase scope, design file, DECISIONS, and existing notes | 1 |
| read-by | [agent:bob-cli-aq.2][2] | Need phase 1 scope to build phase 2 on top | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-aq.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-aq.2/README.md

<!-- sase:referenced-by:end -->
