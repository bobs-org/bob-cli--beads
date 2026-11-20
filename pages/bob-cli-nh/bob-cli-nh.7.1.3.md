# Bead: bob-cli-nh.7.1.3 — Period navigation, YAML excursion, command entry points, and docs

[Bead Pages](../README.md) / [bob-cli-nh.7.1](bob-cli-nh.7.1.md) / bob-cli-nh.7.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-nh.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.7.md) · **Assignee:** `bob-cli-nh.7.1.3` · **Size:** medium
**Created:** 2026-11-19 18:17:37 EST · **Closed:** 2026-11-20 03:44:35 EST
**Plan:** [202611/intention\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/intention_card.md)

## Description

navigation: add in-place parent and sibling navigation, missing-note states, the intentions YAML excursion, Edit intentions and Reflect on yesterday palette/Command Mode entries, and the non-Vim fallback. Document the complete card in docs/intention-card.md and nav; test, regenerate, and sync plugins.

## Notes

[2026-11-20T08:44:09Z · bob-cli-nh.7.1.3] PROPOSED FOLLOW-UP: docs-check published-URLs gate has 2 broken obligations reproducing identically on the clean base (docs/develop/plugins/architecture.md:74 -> /develop/validation/; docs/reference/glossary.md:301 -> /bob-copy-chips/); needs its own fix, not this phase.

[2026-11-20T08:44:16Z · bob-cli-nh.7.1.3] PROPOSED FOLLOW-UP: test-obsidian-album-schema-writer-e2e self-test fails identically on the clean base (held-lock apply created 2 commits, expected 1); unrelated to intention navigation, needs its own fix.

[2026-11-20T08:44:35Z · bob-cli-nh.7.1.3] Navigation phase landed in bob-plugins: in-modal [/= travel with missing-note disabled states and target-pinned async, intentions YAML excursion with empty-op-preview Done, edit-intentions + reflect-on-yesterday palette/CM/fallback entries, [n==r and ==[r compositions, docs/intention-card.md + nav + ledger link. Verified: 129 focused tests pass (incl. 6 new navigation tests), build/build:check/validate green, docs lint+strict build green, plugins synced (4 copied). docs-check URL gate (2 broken) and album-writer self-test fail identically on clean base, recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-nh.7.1.2](bob-cli-nh.7.1.2.md) ✓ · ⧖ 2026-11-19
- **Blocks:** [bob-cli-nh.7.1.4](bob-cli-nh.7.1.4.md) ◐ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-nh.7.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-nh.7.1.3/README.md) | [bob-cli-nh.7.1.3](bob-cli-nh.7.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@ea47caf`](https://github.com/bobs-org/bob-plugins/commit/ea47cafc8606283a355212806257153be6d336de) | feat(ledger-tools): intention card period navigation, YAML excursion, and entry points | [bob-cli-nh.7.1.3](bob-cli-nh.7.1.3.md) | 2026-11-20 03:45:47 EST |
