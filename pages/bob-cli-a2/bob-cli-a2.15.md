# Bead: bob-cli-a2.15 — Install, pilot on a vault copy, reach the MacBook, guide, and memory

[Bead Pages](../README.md) / [bob-cli-a2](README.md) / bob-cli-a2.15

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.53.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.53.linker.w0.md) · **Assignee:** `bob-cli-a2.15` · **Size:** medium
**Created:** 2026-10-20 09:08:24 EDT · **Closed:** 2026-10-20 13:16:54 EDT
**Plan:** [202610/task\_relations.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_relations.md)

## Description

rollout: install bob and the plugins on athena, then check that the live reconcile dry run shows zero relation changes. Run the pilot script on a vault copy, update the MacBook best-effort, write the user guide, add the memory records the accepted decisions allow, and record what is left for Bryan.

## Notes

[2026-10-20T17:16:22Z · bob-cli-a2.15] Rollout verified 2026-10-20. `just install` installed bob at 8755ffc8 on athena; `bob plugins sync --no-pull` and `bob plugins list` reported 7/7 synced and 0 drift. Mac bob-cli was already at 8755ffc8; `just install` succeeded there, and plugin sync/list also reported 7/7 synced and 0 drift. Both live `bob task reconcile --dry-run -f json` runs had zero linked_from_line_updates, zero minted_relation_source_block_ids, and zero relation_warnings; Mac had no warnings, while athena had only the unrelated pending_cap_exceeded warning. Athena capture dry-run resolved an existing task and previewed the expected LINKS, LINKED FROM, and source-id changes without writing. Pilot on a temporary Markdown vault copy verified same-note ~, labeled cross-note ~, reverse ~~; mixed & plus ~ retained dependency blocking while adding the inert relation; two reconciles were zero-change and byte-stable; deleting LINKED FROM lines rebuilt exact bytes; removing one mirror entry restored it; kill switch false removed mirrors without minting and true restored exact bytes; parser guards for ~~old~~, =~2, and Clean ~/Downloads produced no relation spans and preserved input. Scratch copy was deleted.

[2026-10-20T17:16:26Z · bob-cli-a2.15] Bryan follow-up after this rollout: reload nav, bob-ledger-tools, task-status-cycler, and block-id-prompt in Obsidian on the Mac; install/update Bob Mac Capture from GUI Terminal with the login keychain unlocked; then run the research six-step pilot, especially remove a relation from the incoming side and predict which note changes, and exercise ＋ / × on both LINKS and LINKED FROM rows. Mac app update was not installed here: `just signing-check` exited 77 over SSH because the login keychain is locked and cannot show its unlock prompt; ad-hoc install would reset Accessibility permission. Opened bob-mac-capture validation passed: `just portable-check` (1465 tests), scratch bundle build, and `just typecheck-tests` (BobMacCapture, BobMacCaptureInstallHelper, CaptureCore, RefsCore).

[2026-10-20T17:16:29Z · bob-cli-a2.15] PROPOSED FOLLOW-UP: Add Task Card cancel-as-duplicate/merged/superseded gestures; opt-in dry-run adoption for existing Merged into, See, and RELATED bullets; a make-this-a-prerequisite conversion; label near-duplicate lint and one-shot relabel; configurable inverse phrases; and a read-only `bob relations` report. These are deliberate non-goals listed in plan:202610/task_relations.md for the epic land agent to triage.

[2026-10-20T17:16:33Z · bob-cli-a2.15] PROPOSED FOLLOW-UP: `just docs-check` passed lint, generated drift, strict Zensical build, URL/link checks, search smoke, executable tutorial, and CLI media determinism, then failed docs unit tests (437 passed, 2 skipped, 2 failed) because `github-callouts` is missing (`ModuleNotFoundError`). This environment failure is already recorded on bob-cli-a2.14 notes #1 and #3; `sase bead search 'github-callouts' --regex --type task` found no matching task bead.

[2026-10-20T17:16:37Z · bob-cli-a2.15] PROPOSED FOLLOW-UP: `just check` failed only `native::highlights_ref::fetch::tests::fetch_covers_redirects_statuses_and_exit_codes` under the full parallel lib run with `Text file busy (os error 26)` executing fake-curl.sh; 3117 lib tests passed and all remaining check targets passed. The isolated exact test rerun passed. Existing flake task bob-cli-5l tracks this same in-place fake executable race.

[2026-10-20T17:16:54Z · bob-cli-a2.15] Installed bob and plugins on athena and Mac; both live reconcile dry-runs had zero relation changes, the isolated vault-copy pilot converged with stable mirror bytes, the guide and authorized glossary updates are in place, and Mac app/user follow-ups plus known check failures are recorded in phase notes.

## Dependencies

- **Depends on:** [bob-cli-a2.10](bob-cli-a2.10.md) ✓ · ⧖ 2026-10-20
- **Depends on:** [bob-cli-a2.12](bob-cli-a2.12.md) ✓ · ⧖ 2026-10-20
- **Depends on:** [bob-cli-a2.14](bob-cli-a2.14.md) ✓ · ⧖ 2026-10-20
- **Depends on:** [bob-cli-a2.4](bob-cli-a2.4.md) ✓ · ⧖ 2026-10-20
- **Depends on:** [bob-cli-a2.7](bob-cli-a2.7.md) ✓ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-a2.15](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-a2.15/README.md) | [bob-cli-a2.15](bob-cli-a2.15.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`eefdeb4`](https://github.com/bobs-org/bob-cli/commit/eefdeb4717c003aeb23e09c9288f66fa36ee6203) | docs(relations): document relation usage and rollout | [bob-cli-a2.15](bob-cli-a2.15.md) | 2026-10-20 13:17:35 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a2.15][1] | Confirm whether this phase has prior notes before planning | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-a2.15/README.md

<!-- sase:referenced-by:end -->
