# Bead: bob-cli-hg.4 — bob gmail noun group, config, login, logout, and doctor

[Bead Pages](../README.md) / [bob-cli-hg](README.md) / bob-cli-hg.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.cn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.cn.md) · **Assignee:** `bob-cli-hg.4` · **Size:** medium
**Created:** 2026-11-05 12:37:49 EST · **Closed:** 2026-11-05 19:20:16 EST
**Plan:** [202611/bob\_gmail.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_gmail.md)

## Description

gmail-shell: register `bob gmail`, parse the `gmail:` config block, add Gmail read methods to the gog transport, ship login/logout/doctor on the isolated bob-gmail client, the test harness, catalog rows, and the first docs.

## Notes

[2026-11-06T00:20:06Z · bob-cli-hg.4] PROPOSED FOLLOW-UP: catalog clipboard entry is in both ENTRIES and EXCLUDED without fixed/url slot, failing public_leaves_are_entries_or_excluded on clean base too; triage as task bead

[2026-11-06T00:20:16Z · bob-cli-hg.4] gmail-shell landed: bob gmail noun group, gmail: config parsing, Gmail gog reads with --readonly --gmail-no-send --enable-commands, login/logout/doctor on isolated bob-gmail client, fake-gog harness plus 10 gmail_shell tests green, gcal_auth 55 green, catalog 73 entries (clipboard dual-list failure pre-exists on base, noted as follow-up), just lint and just docs-check green, docs/gmail.md plus connect-google-mail guide and generated CLI reference

## Dependencies

- **Depends on:** [bob-cli-hg.1](bob-cli-hg.1.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hg.6](bob-cli-hg.6.md) ✓ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.4/README.md) | [bob-cli-hg.4](bob-cli-hg.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8890707`](https://github.com/bobs-org/bob-cli/commit/889070741f4fab7b118429ffa660696a84a84e8a) | feat(gmail): add bob gmail shell with config, login, logout, doctor | [bob-cli-hg.4](bob-cli-hg.4.md) | 2026-11-05 19:22:21 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hg.4][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-hg.9][2] | Confirm the same catalog overlap was reproduced on the clean base | 1 |
| read-by | [agent:research.5s.mus][3] | gmail user guide research | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.9/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.5s.mus/README.md

<!-- sase:referenced-by:end -->
