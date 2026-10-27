# Bead: bob-cli-da.1 — Re-check the macOS aliases completion flake after the deadline pin

[Bead Pages](../README.md) / [bob-cli-da](README.md) / bob-cli-da.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-d7.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-d7.land.md) · **Assignee:** `bob-cli-da.1` · **Size:** large
**Created:** 2026-10-27 16:30:19 EDT · **Closed:** 2026-10-27 17:08:09 EDT
**Plan:** [202610/backlog\_batch\_b2.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_b2.md)

## Description

macos-completion-flake: read bob-cli-b9 with audited reads, re-check it after f00854be (complete() now uses bob_completion_command with the 10000 ms test deadline), investigate complete_values empty-list path in tests/cli/aliases.rs, apply the same pin only if it shares the deadline path, prove with loaded Linux runs, obtain macOS CI evidence via gh, and close only per b9_close_gate = ci_green; otherwise leave a coordination note. Do not assume a Linux pass proves macOS.

## Notes

[2026-10-27T20:49:46Z · bob-cli-da.1] LINUX EVIDENCE from bob-cli-da.1 on athena at SHA 4fd82919009fa061ced90434f8033528c9eb6f85 (f00854be ancestor; aliases.rs/support.rs/completion/mod.rs identical to the pin). complete() uses bob_completion_command() with BOB_COMPLETE_DEADLINE_MS=10000; production COMPLETE_DEADLINE_MS remains 150. complete_values() asserts exit 0 then strips protocol '!' lines, so empty stdout becomes [] even on success. run_complete_inner() recv_timeout expiration (and worker panics) also yield empty stdout with exit 0; BOB_COMPLETE_DEBUG already logs request/response/elapsed/timeout. Isolated `cargo test --locked --test cli aliases::`: 12 passed, 0 failed, 6.75s harness / 6.953s wall, parent affinity 0-63, aliases::completion_offers_group_members_status_flags_and_alias_options ok. Loaded: compiled harness cli-806002a2a1095e1f; 5 waves x 4 concurrent; aliases:: --test-threads=8; launched taskset -c 0,1 from host affinity 0-63; 20/20 exit 0; 240 cases; 20/20 flake-node ok; 38.971s total. No source changes. Original macOS: run 40572791226 attempt 1 job 122433733173 SHA f00854be cargo test --locked --no-fail-fast FAILED overall (2301 passed, 1 failed); aliases node ok 2026-10-27T20:05:20Z; failure completion::zsh_adapter::real_zsh_first_tab_completes FORMAT-TAB MISS / PROMPT-READ-FAILED. HEAD run 40580084264 cancelled. Following equivalent in-progress run 40580690009 SHA f6287847 job 122458945477.

[2026-10-27T21:07:49Z · bob-cli-da.1--1] PROPOSED FOLLOW-UP: macOS zsh PTY readiness failure persists after f00854be — run 40572791226 attempt 1, job 122433733173 failed completion::zsh_adapter::real_zsh_first_tab_completes at FORMAT-TAB while the aliases node passed; related closed bead bob-cli-8q and phase bob-cli-d7.3; this observation predates 8q closure.

Fresh equivalent-run evidence (the one allowed rerun of 40572791226 was not used; pending equivalent run 40580690009 was followed instead): run 40580690009 attempt 1 SHA f628784743a47d9f295aabc93114d41c52f47f0b job 122458945477 https://github.com/bobs-org/bob-cli/actions/runs/40580690009/job/122458945477 ran cargo test --locked --no-fail-fast and logged completion::zsh_adapter::real_zsh_first_tab_completes ... ok at 2026-10-27T20:55:21Z; CLI suite 2302 passed, 0 failed; macOS job success. The original FORMAT-TAB / PROMPT-READ-FAILED failure did not reproduce on this green full-suite job. Do not treat this as a post-8q-close reproduction or automatically reopen 8q. Lander owns triage; this phase did not expand into PTY repair.

[2026-10-27T21:08:09Z · bob-cli-da.1--1] Verified the landed f00854be aliases completion deadline pin without further source changes. complete() uses bob_completion_command(); tests/cli/support.rs sets BOB_COMPLETE_DEADLINE_MS=10000; production COMPLETE_DEADLINE_MS remains 150. complete_values() empty stdout becomes [] even on exit 0.

Fresh Linux at SHA 4fd82919009fa061ced90434f8033528c9eb6f85: isolated `cargo test --locked --test cli aliases::` 12/12 pass; loaded 20 instances / 240 cases all pass (logs /tmp/bob-cli-da1/).

macOS original: run 40572791226 attempt 1 SHA f00854be job 122433733173 FAILED overall on completion::zsh_adapter::real_zsh_first_tab_completes; aliases node passed. Qualifying green full-suite: run 40580690009 attempt 1 SHA f628784743a47d9f295aabc93114d41c52f47f0b (includes f00854be; helpers unchanged) job 122458945477 test (macos-latest) SUCCESS; command cargo test --locked --no-fail-fast; aliases::completion_offers_group_members_status_flags_and_alias_options ok at 2026-10-27T20:54:45Z; CLI 2302 passed, 0 failed. https://github.com/bobs-org/bob-cli/actions/runs/40580690009/job/122458945477

bob-cli-b9 ci_green gate is met. Recorded READY FOR LANDER CLOSURE on b9 and left b9 open. PROPOSED FOLLOW-UP on this bead owns the original zsh PTY observation plus the green equivalent-run evidence for lander triage. epic-symbols bob-cli-da.1 had no leftover entries.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-da.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-da.1.md) | [bob-cli-da.1](bob-cli-da.1.md) | 0 |
