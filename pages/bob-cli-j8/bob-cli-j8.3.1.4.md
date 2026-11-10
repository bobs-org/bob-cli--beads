# Bead: bob-cli-j8.3.1.4 — Expose notebook capture targets and verify the complete contract

[Bead Pages](../README.md) / [bob-cli-j8.3.1](bob-cli-j8.3.1.md) / bob-cli-j8.3.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-j8.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-j8.3.md) · **Assignee:** `bob-cli-j8.3.1.4` · **Size:** medium
**Created:** 2026-11-09 13:50:25 EST · **Closed:** 2026-11-09 20:30:52 EST
**Plan:** [202611/notebook\_capture\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/notebook_capture_notes.md)

## Description

notebook-capture-contract: add the opt-in notebook target scanner and route rows, suppress Similar tasks for notebook items, complete cross-surface regressions and docs, and provide closure evidence for bob-cli-j8.3.

## Notes

[2026-11-10T01:30:52Z · bob-cli-j8.3.1.4] Implemented opt-in notebook scanner (scan_capture_targets_with_notebooks, base scan unchanged), routed bob capture-targets and route completion to it with kind:notebook title/summary/owner/breadcrumb rows after projects, notebook shell/human badge with breadcrumb, excluded notebooks from task homes (parent, link, corpus, walk, doctor, transfer, providers), suppressed Similar-tasks band for notebook drafts (mixed retains). Verified: 3 new focused tests pass, 65 lib + 177 CLI related/complete pass, 9 capture-targets CLI pass, project clippy gate passes, just docs-check passes, docs-gen regenerated.

## Dependencies

- **Depends on:** [bob-cli-j8.3.1.3](bob-cli-j8.3.1.3.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-j8.3.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-j8.3.1.4/README.md) | [bob-cli-j8.3.1.4](bob-cli-j8.3.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`12692eb`](https://github.com/bobs-org/bob-cli/commit/12692ebb95db9b30704ab1e5dd9fc7df70509849) | feat(capture)!: expose notebook capture targets and verify contract | [bob-cli-j8.3.1.4](bob-cli-j8.3.1.4.md) | 2026-11-09 20:32:13 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-j8.3.1.3][1] | Check sibling phase to avoid overlap | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-j8.3.1.3/README.md

<!-- sase:referenced-by:end -->
