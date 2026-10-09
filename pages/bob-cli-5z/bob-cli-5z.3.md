# Bead: bob-cli-5z.3 — Execute swaps with ledger takeover and first-future demotion

[Bead Pages](../README.md) / [bob-cli-5z](README.md) / bob-cli-5z.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.61.w1.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.61.w1.w0.md) · **Assignee:** `bob-cli-5z.3` · **Size:** medium
**Created:** 2026-10-09 13:24:48 EDT · **Closed:** 2026-10-09 14:41:44 EDT
**Plan:** [202610/pomodoro\_override.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_override.md)

## Description

override-swap: implement `==[<X>]#name` (resolve exactly like `=#name`, transfer or re-time the session ledger, demote the old running block to first future with contents intact), fill the `demoted` JSON, `swapped` human output, `=x0` equivalence tests, updated teaching errors, and finish every bob-cli doc surface.

## Notes

[2026-10-09T18:41:37Z · bob-cli-5z.3] PROPOSED FOLLOW-UP: 9 native::highlights_ref::return_links lib tests fail identically on the clean base tree (verified via stash); unrelated LaTeX return-link regressions, no bead tracks them yet

[2026-10-09T18:41:44Z · bob-cli-5z.3] Swap execution done and verified: ==#bugs kept-ledger day file byte-matches the plan worked example; ==3#bugs fresh; again/created targets with kept ledger and did-you-mean spelled ==; ==#capture refuses, ==3#capture restarts byte-identical to ==3; ==3#bugs equals =x0 =3#bugs and ==#bugs equals =x0 =#bugs modulo the ledger; drops/strict/chains/CRLF/rollback/dry-run covered. 28/28 pomodoro_override tests pass; full just check green except 9 highlights_ref lib failures that reproduce identically on the clean base (recorded as follow-up). No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-5z.2](bob-cli-5z.2.md) ✓ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-5z.5](bob-cli-5z.5.md) ◐ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5z.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5z.3/README.md) | [bob-cli-5z.3](bob-cli-5z.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`999816c`](https://github.com/bobs-org/bob-cli/commit/999816cd77b1600fcefe961862cf3fccc878c9ce) | feat(capture): implement pomodoro swap execution with named override | [bob-cli-5z.3](bob-cli-5z.3.md) | 2026-10-09 14:43:16 EDT |
