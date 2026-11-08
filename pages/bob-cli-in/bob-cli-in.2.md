# Bead: bob-cli-in.2 — Host-local, idempotent commit and journal recovery

[Bead Pages](../README.md) / [bob-cli-in](README.md) / bob-cli-in.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.19v](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.19v.md) · **Assignee:** `bob-cli-in.2` · **Size:** medium
**Created:** 2026-11-08 06:23:52 EST · **Closed:** 2026-11-08 09:24:50 EST
**Plan:** [202611/gmail\_sync\_ii3\_completion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_sync_ii3_completion.md)

## Description

recovery: move the sync recovery evidence to host-local state, make its replay idempotent per event and ownership-checked per path, stop writing auxiliary files on runs that save no note, keep in-flight filings from being filed twice, and add the temporary-Git-vault recovery tests.

## Notes

[2026-11-08T14:24:39Z · bob-cli-in.2] Recovery work complete: host-local evidence, idempotent replay, ownership hashes, aux gating, in-flight skip, 13 new tests green; tree fast-forwarded onto origin/master 063f9c23 with no conflicts. Land agent: uncommitted changes in src/native/gmail/{save.rs,sync/command.rs,sync/enroll.rs,sync/file.rs,sync/report.rs} are the phase deliverable.

[2026-11-08T14:24:50Z · bob-cli-in.2] Recovery phase done and verified. Host-local evidence at XDG_STATE_HOME/bob/gmail/sync-recovery-<digest>.json (SHA-256 over account + canonical vault path), atomic writes, delete-instead-of-empty, load/write failures and invalid ids become body-free warning + ok=false (no panics). Per-stage replay (save, origins, enrollment) with persist-after-each-success; adoptions never produce gmail.save; failed adoption enrollment defers and stays out of the watch count. Owned paths carry SHA-256 hashes and replay only while bytes match (mismatch warns, drops, still finishes events); aux files planned only when a mail note is written; in-flight threads never refiled; recovered rows render the index link; dry-run projects recovery rows read-only. Tests: 13 new (commit-failure replay incl. image/hub/unrelated/custom + replay with empty candidates + dry-run projection, closed-task and edited-path duplicate prevention, journal-failure replay incl. origins-only failure and adoption-only, corrupt/invalid/empty evidence, image rollback, double-conflict deferral) plus enroll in-flight and report deferred-watch unit tests. Verified: cargo test -p bob-obsidian --lib gmail:: (397 passed), gmail_sync/gmail_shell/gmail_pull_attach integration targets (2/61/11), cargo fmt --check, just lint, epic-symbols none. Tree fast-forwarded onto origin/master 063f9c23; no conflicts with the landed threads.list discovery change.

## Dependencies

- **Depends on:** [bob-cli-in.1](bob-cli-in.1.md) ✓ · ⧖ 2026-11-08
- **Blocks:** [bob-cli-in.3](bob-cli-in.3.md) ✓ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-in.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-in.2/README.md) | [bob-cli-in.2](bob-cli-in.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e5a7b2a`](https://github.com/bobs-org/bob-cli/commit/e5a7b2a32ac7195f11914e0e85cdd50b5e1386d9) | fix(gmail): host-local idempotent sync recovery evidence | [bob-cli-in.2](bob-cli-in.2.md) | 2026-11-08 09:26:02 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-in.2][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-in.2/README.md

<!-- sase:referenced-by:end -->
