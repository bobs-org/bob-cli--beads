# Bead: bob-cli-lk.3.1.4 — Finish reply-reopen reports, documentation, and regression coverage

[Bead Pages](../README.md) / [bob-cli-lk.3.1](bob-cli-lk.3.1.md) / bob-cli-lk.3.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-lk.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-lk.3.md) · **Assignee:** `bob-cli-lk.3.1.4` · **Size:** medium
**Created:** 2026-11-14 14:00:56 EST · **Closed:** 2026-11-14 19:48:30 EST
**Plan:** [202611/gmail\_closed\_reply\_reopen.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_closed_reply_reopen.md)

## Description

reopen-contract: finish the additive reopened watch row and reason, quiet human news, doctor config output, public contracts, and the inherited authorized Gmail Task glossary correction. Complete the acceptance matrix and run the full code and documentation gates. Implement section 4. Leave ancestor closure to this child epic's land agent.

## Notes

[2026-11-15T00:33:33Z · bob-cli-lk.3.1.4] PROPOSED FOLLOW-UP: docs-check offline lychee fails on docs/bank.md:210 link ../reference/plugins/bob-navigation-hotkeys.md#bank-walk which climbs out of docs/ (should be reference/plugins/...); defect is in committed bank-workstream content untouched by this phase and fails independent of it (base-tree docs-check also red); same defect class as bob-cli-l7 (different file) -r record pre-existing docs-check failure so the land agent can triage

[2026-11-15T00:48:30Z · bob-cli-lk.3.1.4] Section 4 verified: watch[] action=reopened with reason replied/bounced and restored task locators; quiet prints reopened rows and dry-run previews them; refusal exits 1 once then stays quiet; doctor config shows reopen on/off; docs/gmail.md gains Config/Reopen/Reports/JSON/doctor updates; freshness.md gains UB19 writer+vector+rollout; json-outputs.md documents reopened reason/locators within budget; glossary Gmail Task amended via inherited memory_gmail_task_glossary=yes with docs-gen republished. just check green: fmt+clippy clean, full workspace suite passed except one subprocess_runner load flake that passes in isolation and in the lib re-run (7026 passed). docs-check budget clean; lychee blocked only by pre-existing bank.md out-of-docs link recorded as PROPOSED FOLLOW-UP. No epic-symbol entries.

[2026-11-15T01:02:44Z · bob-cli-lk.3.1.4--1] PROPOSED FOLLOW-UP: just-check lib flake subprocess_runner pipe-drain failed under load but passes in isolation — monitor 9r12q4vpf4ne exit 101 on native::subprocess_runner::tests::run_bounds_pipe_drain_when_detached_grandchild_holds_output (assert output truncated), rerun single test ok, gmail_sync reopen 7/7 ok; phase files untouched, bead stays closed

## Dependencies

- **Depends on:** [bob-cli-lk.3.1.3](bob-cli-lk.3.1.3.md) ✓ · ⧖ 2026-11-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-lk.3.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-lk.3.1.4.md) | [bob-cli-lk.3.1.4](bob-cli-lk.3.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ff272bc`](https://github.com/bobs-org/bob-cli/commit/ff272bc6758d643caebe1fa607fd1ecc14fabb0c) | feat(gmail): finish reply-reopen reports, docs and regression coverage | [bob-cli-lk.3.1.4](bob-cli-lk.3.1.4.md) | 2026-11-14 20:05:23 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-lk.3.1.4--1][1] | Need phase scope and status after monitor check failure | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-lk.3.1.4.md

<!-- sase:referenced-by:end -->
