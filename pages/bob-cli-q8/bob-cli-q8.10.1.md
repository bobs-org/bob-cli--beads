# Bead: bob-cli-q8.10.1 — PT12 CRLF vectors and the missing LR31/LR35 reconcile cases

[Bead Pages](../README.md) / [bob-cli-q8.10](bob-cli-q8.10.md) / bob-cli-q8.10.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-q8.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-q8.land.md) · **Assignee:** `bob-cli-q8.10.1` · **Size:** small
**Created:** 2026-11-26 02:09:19 EST · **Closed:** 2026-11-26 03:03:45 EST
**Plan:** [202611/finish\_plain\_link\_ties.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_plain_link_ties.md)

## Description

tie-vector-coverage: add the CRLF and no-final-newline PT12 cases to the shared tie vectors and their JS mirror, add the missing LR31 skip cases (uncertain target, quiet-deferred), and make LR35 compare the whole dry-run JSON with the apply JSON.

## Notes

[2026-11-26T08:03:45Z · bob-cli-q8.10.1] tie-vector-coverage done and verified. PT12b (non-first drop keeps trailing CR) and PT12c (only entry DeleteLine) added to vectors.json and re-copied verbatim into bob-plugins plain-link-tie-vectors.cjs; required a contained 087 twin fix (strip one trailing CR, re-append on rewrite) because JS dot never matches CR and the 085 bullet regex rejected CR lines. LR31 gained uncertain-target (target with malformed Depends-On on a third task) and quiet-deferred (future-mtime note) skip cases. New LR27 CRLF variant asserts LF/CRLF byte parity (dry absorption rows equal; CRLF apply equals LF apply with CRLF endings; no final newline survives). LR35 now compares the whole dry-run and apply JSON apart from dry_run plus the apply-only write receipts applied_files and recovery_directory (verified empirically these differ: tasks.md receipt and a recovery path; deferred_files stays compared and matches). Docs PT/LR tables updated. Verified: 49/49 task_status_hooks::relations CLI tests, 41/41 task_relations lib tests, just lint, just docs-check, cargo fmt clean, JS tie suite 22/22, npm build:check, npm docs:check, bob plugins sync deployed bob-navigation-hotkeys. No epic-symbol entries left. One deviation from the phase letter: LR35 also excludes applied_files/recovery_directory since literal whole-JSON equality is impossible (apply-only receipts); docs LR35 row says so.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-q8.10.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-q8.10.1/README.md) | [bob-cli-q8.10.1](bob-cli-q8.10.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1c23bce`](https://github.com/bobs-org/bob-cli/commit/1c23bce7a8a0024e7874f0955bee104f4207870c) | feat(ties): PT12 CRLF vectors, missing LR31 skips, whole-JSON LR35 | [bob-cli-q8.10.1](bob-cli-q8.10.1.md) | 2026-11-26 03:05:03 EST |
| bob-plugins | [`bob-plugins@e82bd93`](https://github.com/bobs-org/bob-plugins/commit/e82bd9328781baae85122e337617c8a2e404216e) | feat(ties): mirror PT12b/PT12c vectors, CR-tolerant drop twin | [bob-cli-q8.10.1](bob-cli-q8.10.1.md) | 2026-11-26 03:05:56 EST |
