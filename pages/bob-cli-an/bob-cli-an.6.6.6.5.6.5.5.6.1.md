# Bead: bob-cli-an.6.6.6.5.6.5.5.6.1 — Exit quietly instead of panicking when bob's stdout reader closes early

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6](bob-cli-an.6.6.6.5.6.5.5.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.1` · **Size:** small
**Created:** 2026-10-25 08:44:09 EDT · **Closed:** 2026-10-25 09:09:06 EDT
**Plan:** [202610/backlog\_batch9\_epipe\_listen\_publish\_refresh\_flakes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch9_epipe_listen_publish_refresh_flakes.md)

## Description

epipe-clean-exit: resolve bob-cli-bl so a closed stdout or stderr pipe ends bob quietly at the run_bob boundary without changing SIGPIPE handling, with a large-output CLI regression test.

## Notes

[2026-10-25T13:08:55Z · bob-cli-an.6.6.6.5.6.5.5.6.1] Done: quiet EPIPE exit. Baseline repro on unpatched tree: bob stats -r 2026-01-01..2026-10-11 -f json | head -c 10 -> exit 101 plus thread-main panicked: failed printing to stdout: Broken pipe (os error 32). Fix in src/runner.rs: run_bob installs a conditional-silent panic hook plus catch_unwind around run_bob_inner; is_epipe_print_panic maps only stdout/stderr failed-printing + BrokenPipe payloads to exit 0, everything else rethrown after hook restore (message + 101 preserved). No SIGPIPE change (grep confirms no new signal calls). Also maps BrokenPipe from root clap error.print to 0 and capture-expand write_all BrokenPipe to quiet 0. Tests: 2 new classifier unit tests (accept stdout/stderr EPIPE incl. &str payload; reject ENOSPC print failure, unrelated panic, non-string payload) and tests/cli/epipe.rs regression (349KB fixture, 10-byte read then close, asserts exit 0 and no panicked/Broken pipe on stderr). Verified: repro now exit 0 empty stderr; closed-stderr variant exit 0; full stats output intact (353663B); bob --help | head and stats --help | head exit 0 empty stderr incl. 20/20 loop; bogus subcommand still exit 2. Gates: cargo fmt clean, clippy exit 0, full cargo test --no-fail-fast green (18 suites ok, 0 failed). No docs exit-status contract exists so no docs change. No follow-ups discovered.

[2026-10-25T13:09:06Z · bob-cli-an.6.6.6.5.6.5.5.6.1] EPIPE exits quietly: repro now exit 0 with empty stderr; classifier unit tests + committed tests/cli/epipe.rs regression green; fmt/clippy/full cargo test green

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.1/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.1](bob-cli-an.6.6.6.5.6.5.5.6.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6292c35`](https://github.com/bobs-org/bob-cli/commit/6292c35b61aa230b24b070523341b85576eeae54) | fix(cli): exit 0 quietly on EPIPE instead of panicking | [bob-cli-an.6.6.6.5.6.5.5.6.1](bob-cli-an.6.6.6.5.6.5.5.6.1.md) | 2026-10-25 09:10:13 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.1/README.md

<!-- sase:referenced-by:end -->
