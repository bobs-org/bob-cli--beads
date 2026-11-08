# Bead: bob-cli-ii.3.1.1 — Enrollment journal and watching-task membership

[Bead Pages](../README.md) / [bob-cli-ii.3.1](bob-cli-ii.3.1.md) / bob-cli-ii.3.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ii.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ii.3.md) · **Assignee:** `bob-cli-ii.3.1.1` · **Size:** medium
**Created:** 2026-11-07 18:12:56 EST · **Closed:** 2026-11-07 18:40:06 EST
**Plan:** [202611/gmail\_sync\_filing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_sync_filing.md)

## Description

membership: implement the body-free enrollment fold and append API, the vault-wide watching-task scan, and adoption decisions with focused tests.

## Notes

[2026-11-07T23:40:06Z · bob-cli-ii.3.1.1] Membership landed in src/native/gmail/sync/{mod,enroll,scan}.rs plus a shared src/native/gmail/vault_walk.rs (link -a's walk factored out; link.rs now uses it, its regression tests kept in place). API for later phases: sync::ThreadKey (lowercase account + lowercase hex id; index_key() matches MailIndex.by_identity); enroll::EnrollmentFold::load (cross-host gmail.pulled/filed/adopted fold, writer order, bounded malformed-line/event warnings; is_enrolled/origin Legacy|Sync -> already_pulled|already_filed/records/latest with note, task_file, via, route); enroll::append(vault, host, &EnrollmentEvent::{Filed{via: Route|Inbox|Problem, route?}, Adopted}) writes body-free values; scan::scan_watching_tasks(vault, mail_folder, &MailIndex) -> WatchScan {tasks(): path, 1-based line, exact text, block_id, status, targets[{key, note, placement TaskLine|ChildBullet{line}}]; watchers(key), threads(), warnings()}; enroll::Membership::new(&fold, &scan).decide(key) -> Enrolled(origin)|Adopt(AdoptionIntent)|File, adoptions(account) (label-free, from the local scan, per child plan), watched(account). Scan/decide never write; apply phase owns appends. Unused-API allowances are per-item cfg_attr(not(test), allow(dead_code)) for the command phase to remove; journal::pulled_identities/append_pulled stay for old pull until dispatch switches. Note for land/command: per the child plan, adoptions() adopts any open-task-linked unenrolled mail note of the account, including hand-linked notes that never carried the label. Verified: 20 new sync tests + 2 vault_walk tests; cargo test --lib (5547 passed); gmail_pull_attach, gmail_shell, gmail_search_peek, gmail_compose_contract, gmail_draft, gmail_send integration tests pass; cargo fmt --check clean; just lint clean (only pre-existing non-gated warnings).

## Dependencies

- **Blocks:** [bob-cli-ii.3.1.2](bob-cli-ii.3.1.2.md) ✓ · ⧖ 2026-11-07
- **Blocks:** [bob-cli-ii.3.1.3](bob-cli-ii.3.1.3.md) ✓ · ⧖ 2026-11-07
- **Blocks:** [bob-cli-ii.3.1.4](bob-cli-ii.3.1.4.md) ✓ · ⧖ 2026-11-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ii.3.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ii.3.1.1/README.md) | [bob-cli-ii.3.1.1](bob-cli-ii.3.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`343b4d8`](https://github.com/bobs-org/bob-cli/commit/343b4d8ff7e0be48e41a0dc980d2e8be815c3677) | feat(gmail): add sync enrollment fold, watching-task scan, and adoption decisions | [bob-cli-ii.3.1.1](bob-cli-ii.3.1.1.md) | 2026-11-07 18:49:30 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ii.3.1.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ii.3.1.1/README.md

<!-- sase:referenced-by:end -->
