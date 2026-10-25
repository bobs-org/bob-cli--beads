# Bead: bob-cli-bj.11 — Decision records, docs sweep, and end-to-end acceptance

[Bead Pages](../README.md) / [bob-cli-bj](README.md) / bob-cli-bj.11

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2e.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2e.linker.w0.md) · **Assignee:** `bob-cli-bj.11` · **Size:** small
**Created:** 2026-10-24 13:34:47 EDT · **Closed:** 2026-10-24 19:33:24 EDT
**Plan:** [202610/relation\_label\_vocabulary.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_label_vocabulary.md)

## Description

records: write the accepted memory changes, drop planned markers and check cross-links across bob-cli, Mac, and plugin docs, and run and record the end-to-end acceptance.

## Notes

[2026-10-24T23:33:02Z · bob-cli-bj.11] PROPOSED FOLLOW-UP: memory_glossary=no skipped the one-sentence glossary:task-relation addition (label hide via Ctrl+D / bob relations hide / one-off ||, global rename via bob relations rename); corroborates the bj.3 #2 follow-up — file a memory task bead for it at land.

[2026-10-24T23:33:24Z · bob-cli-bj.11] Records done and verified. Memory: 4 decision strands added (relation-label-hide-is-suggestions-only, relation-label-prefs-live-in-per-host-journal, relation-label-rename-rewrites-history, relation-card-tab-accepts-ctrl-d-hides), roster extended to 36, sase memory init clean with twin links resolving. Glossary sentence skipped per memory_glossary=no (follow-up noted). Docs: all planned (phase ...) markers dropped from task-relations.md §16 (RV1-RV9 shipped); Shared-vectors paragraph corrected (rename fold cases live in fold; no separate rename section). just docs-gen + docs-check green (448 passed); CLI reference lists bob relations under Tasks and projects. Cross-repo: refreshed the stale bob-plugins vectors copy (was pinned at 57d77612, missing the rename fold vectors incl. one changed expectation) and fixed the JS fold to match Rust (rename moves state then applies to_name; case-only rename updates display spelling); relation-index vectors test + 97 related plugin tests green. Acceptance: live vault read-only 4 labels/10 links/1 hidden via human+JSON; relation_label probe hidden_count=1 with key/count/replacement/hide_replacement; latency p95 14.6ms (budget 150ms); scratch rename preview->apply one commit (bob relations rename: inspired by -> prompted by) with journal event, git revert restores; hide/unhide round trip with contract copy; 67 CLI relation tests + 21 relation_label unit tests green. Mac card gestures (items 1-2) covered by closed bj.7/bj.9 macOS CI, not re-runnable from Linux. Full just check not run: no bob-cli code changed and clean-base reds are tracked by bc/an/bo beads. bob-plugins changes (src+built main.js+fixtures) left uncommitted and NOT synced to ~/bob — land agent decides commit/deploy.

## Dependencies

- **Depends on:** [bob-cli-bj.10](bob-cli-bj.10.md) ✓ · ⧖ 2026-10-24
- **Depends on:** [bob-cli-bj.9](bob-cli-bj.9.md) ✓ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bj.11](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.11/README.md) | [bob-cli-bj.11](bob-cli-bj.11.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8f50b30`](https://github.com/bobs-org/bob-cli/commit/8f50b304b97bcf2e28a98cf4bd60020f0b8df58c) | docs(records): add relation-label decisions, drop planned markers, record acceptance | [bob-cli-bj.11](bob-cli-bj.11.md) | 2026-10-24 19:34:36 EDT |
| bob-plugins | [`bob-plugins@21e9923`](https://github.com/bobs-org/bob-plugins/commit/21e99230f819184c8b6b14d4a1c62fe960520dcd) | fix(relation-labels): refresh shared vectors and match Rust rename fold rule | [bob-cli-bj.11](bob-cli-bj.11.md) | 2026-10-24 19:35:34 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-bj.11][1] | Read phase notes for acceptance baselines | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.11/README.md

<!-- sase:referenced-by:end -->
