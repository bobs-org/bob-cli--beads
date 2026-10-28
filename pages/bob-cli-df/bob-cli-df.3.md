# Bead: bob-cli-df.3 — Keep a failed links inlet from consuming the scratch plan

[Bead Pages](../README.md) / [bob-cli-df](README.md) / bob-cli-df.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-dd.land--3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-dd.land.md) · **Assignee:** `bob-cli-df.3` · **Size:** medium
**Created:** 2026-10-27 21:24:44 EDT · **Closed:** 2026-10-27 21:34:40 EDT
**Plan:** [202610/backlog\_batch\_b4.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_b4.md)

## Description

plan-propose-inlet: resolve bob-cli-5n in sase by validating or publishing the plan links inlet before move_plan_to_sase, or rolling that move back on inlet failure, so a failed propose leaves the scratch plan in place with a clear error.

## Notes

[2026-10-28T01:34:40Z · bob-cli-df.3] Fixed plan propose inlet ordering in sase src/sase/main/plan_propose_handler.py: publish failure (InletError or any store/lock RuntimeError) and missing canonical ref now restore scratch from original and unlink archive with clear error, no gate/handoff. Added 2 regression tests in tests/test_plan_command_handler_formatting.py (InletError + RuntimeError rollback). Verified: 8 passed formatting suite, 24 passed plan handler + metadata suites (incl. successful links inlet archives), ruff check/format clean, mypy clean. Epic-symbols clean.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-df.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-df.3/README.md) | [bob-cli-df.3](bob-cli-df.3.md) | 0 |
