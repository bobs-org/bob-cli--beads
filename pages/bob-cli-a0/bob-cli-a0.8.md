# Bead: bob-cli-a0.8 — Goal-titled guides and component tags

[Bead Pages](../README.md) / [bob-cli-a0](README.md) / bob-cli-a0.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.95](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.95.md) · **Assignee:** `bob-cli-a0.8` · **Size:** large
**Created:** 2026-10-19 18:55:42 EDT · **Closed:** 2026-10-20 02:37:03 EDT
**Plan:** [202610/bob\_public\_docs\_site.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_public_docs_site.md)

## Description

guides: harvest 10-15 goal-titled how-to guides from the README and contracts, add component tags, and generate the By component index.

## Notes

[2026-10-20T05:49:16Z · bob-cli-a0.8] PROPOSED FOLLOW-UP: Review-walk documentation sources disagree — glossary:task-freshness still lists a REFERENCES tier, while docs/freshness.md describes schema 14 with RECURRING and explicitly no separate reference tier. The guides plan calls for checking current behavior and avoiding a copied tier table. The epic land agent should triage reconciliation of the stale source; this phase does not authorize glossary or decision-memory edits.

[2026-10-20T06:36:41Z · bob-cli-a0.8] PROPOSED FOLLOW-UP: Demo vault Tasks Blocked status is type TODO — bob capture of a dependency against the demo vault fails because Blocked is not status ? / name Blocked / type ON_HOLD. This phase verified dependent-capture dry-run output in a temp vault copied from tests/fixtures/tasks_parity/vault/.obsidian/plugins/obsidian-tasks-plugin/data.json. The epic land agent should triage whether the demo vault should ship that Tasks status set so the add-prerequisites guide can be replayed against the published demo.

[2026-10-20T06:37:03Z · bob-cli-a0.8] Verified goal-titled guides and component tags for bob-cli-a0.8.

Shipped twelve how-to guides under docs/guides/ (filenames are published URLs; nav groups do not relocate them), a Guides hub, Guides tab, homepage Do door, contract reader: mappings, search-smoke queries, tags chips, and generated docs/reference/by-component.md.

Component index generator is deterministic; gen --check reports drift without writing. Tags chips render in both Zensical 0.0.71 and Material 9.7 with hrefs to /reference/by-component/#cli|#obsidian|#macos (no leftover .md in the fragment URL). Hubs and untagged pages omit chips.

just docs-check passed with BOB_DOCS_BOB_PLUGINS_DIR mounted: lint, generated drift, strict Zensical, 111 published URLs, offline lychee, 84 search-smoke cases, first-day tutorial, CLI media, 416 documentation unit tests. just docs-build-material passed. git diff --check is clean.

Checkout bob verified capture/freshness/vault-sync help used in the guides. Dependent-capture dry-run used a temp vault with tasks_parity Tasks statuses. Linux host: no Mac GUI, no real Keep drain, no signing, no host-wide install.

No README deletions, no Rust/JS/Swift behavior changes, no memory edits, no task beads created, parent epic bob-cli-a0 left open. epic-symbols for this phase: none leftover.

## Dependencies

- **Blocks:** [bob-cli-a0.11](bob-cli-a0.11.md) ◐ · ⧖ 2026-10-19
- **Blocks:** [bob-cli-a0.12](bob-cli-a0.12.md) ✓ · ⧖ 2026-10-19
- **Depends on:** [bob-cli-a0.6](bob-cli-a0.6.md) ✓ · ⧖ 2026-10-19
- **Depends on:** [bob-cli-a0.7](bob-cli-a0.7.md) ✓ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.8.md) | [bob-cli-a0.8](bob-cli-a0.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bae9468`](https://github.com/bobs-org/bob-cli/commit/bae9468d692c5c4e9a14ab73558b1d6c50b8787b) | feat(docs): add goal-titled guides and component tags | [bob-cli-a0.8](bob-cli-a0.8.md) | 2026-10-20 02:52:17 EDT |
