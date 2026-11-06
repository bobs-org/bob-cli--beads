# Bead: bob-cli-hg.14 — bob gmail pull from the bob label, and attachments on demand

[Bead Pages](../README.md) / [bob-cli-hg](README.md) / bob-cli-hg.14

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.cn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.cn.md) · **Assignee:** `bob-cli-hg.14` · **Size:** medium
**Created:** 2026-11-05 12:37:50 EST · **Closed:** 2026-11-06 08:52:27 EST
**Plan:** [202611/bob\_gmail.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_gmail.md)

## Description

gmail-pull-attach: a read-only, idempotent pull of threads labelled `bob` into tasks in gmail_inbox.md linking saved notes, plus `bob gmail attach` to import one attachment through the attachment journal.

## Notes

[2026-11-06T13:09:50Z · bob-cli-hg.14--1] PROPOSED FOLLOW-UP: refresh the README contract-table snapshot on clean base — `just docs-check` fails only at `test_readme_table_matches_original_contract_index_snapshot` (expected fedc20a..., current 96a429d5...; 446 passed, 1 skipped). The unchanged docs/README.md and tools/docs/tests/test_contracts.py reproduce the same result; already tracked by bob-cli-hg.9 note #1 and bob-cli-hl.5.1.5 note #1.

[2026-11-06T13:51:39Z · bob-cli-hg.14--3] PROPOSED FOLLOW-UP: The full just check run dzdgm0c75474 still reported the unchanged clean-base clipboard failures: native::catalog::tests::public_leaves_are_entries_or_excluded sees clipboard in both ENTRIES and EXCLUDED, and native::completion::kinds::tests::every_table_entry_matches_the_tree sees duplicate clipboard:count. These structural defects are already tracked by bob-cli-hp and independently reproduced on clean bases in its evidence. Phase-caused Gmail completion coverage and root-help snapshot failures are fixed; focused reruns pass.

[2026-11-06T13:52:27Z · bob-cli-hg.14--3] Implemented read-only Gmail label pull and idempotent attachment import, including inbox tasks, attachment journal/origin handling, CLI catalog and docs. Verification: Gmail pull/attach integration tests 5/5 passed; completion value coverage passed; root-help snapshot test passed; capture theme completion tests 7/7 passed; cargo fmt --all -- --check and git diff --check passed; epic-symbol check clear. just docs-gen passed; docs-check lint/site gates passed with the pre-existing README contract snapshot failure recorded in note #1. just check failed only on pre-existing clipboard catalog and duplicate completion entries tracked by bob-cli-hp, recorded in note #2; phase-caused metadata and help snapshot failures were fixed and focused reruns passed.

## Dependencies

- **Depends on:** [bob-cli-hg.6](bob-cli-hg.6.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.14](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.14.md) | [bob-cli-hg.14](bob-cli-hg.14.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ec39e1a`](https://github.com/bobs-org/bob-cli/commit/ec39e1a00e0ac9339d832d22db956ade66731c47) | feat(gmail): pull label mail and import attachments | [bob-cli-hg.14](bob-cli-hg.14.md) | 2026-11-06 11:17:57 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:research.5s.grk][1] | Need remaining Gmail phase user-facing scopes for the guide | 1 |
| read-by | [agent:research.5s.mus][2] | gmail user guide research | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.5s.grk/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.5s.mus/README.md

<!-- sase:referenced-by:end -->
