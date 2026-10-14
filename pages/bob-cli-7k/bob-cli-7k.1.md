# Bead: bob-cli-7k.1 — bob-cli serializes the frontmatter id as marker\_id

[Bead Pages](../README.md) / [bob-cli-7k](README.md) / bob-cli-7k.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.19.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.19.linker.w0.md) · **Assignee:** `bob-cli-7k.1` · **Size:** small
**Created:** 2026-10-14 09:32:31 EDT · **Closed:** 2026-10-14 09:38:40 EDT
**Plan:** [202610/refs\_ctrl\_y\_copy\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/refs_ctrl_y_copy_card.md)

## Description

bob-marker-id: make `bob ref list/show/find` JSON rows carry the frontmatter `id` as an additive `marker_id` field (null when absent), with tests and docs/ref.md updated.

## Notes

[2026-10-14T13:38:40Z · bob-cli-7k.1] Exposed frontmatter id as additive marker_id in list/show/find JSON; added present/null CLI coverage and docs/ref.md. Verified cargo fmt --check, git diff --check, and cargo test --test cli ref_library (91 passed); epic-symbols reports no leftovers.

## Dependencies

- **Blocks:** [bob-cli-7k.4](bob-cli-7k.4.md) ◐ · ⧖ 2026-10-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7k.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7k.1/README.md) | [bob-cli-7k.1](bob-cli-7k.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e7e98d2`](https://github.com/bobs-org/bob-cli/commit/e7e98d2e49e6c9b034e864dbbc263ffa0dbabf48) | feat(ref): expose marker ids in JSON | [bob-cli-7k.1](bob-cli-7k.1.md) | 2026-10-14 09:39:35 EDT |
