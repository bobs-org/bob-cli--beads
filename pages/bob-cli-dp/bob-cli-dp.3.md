# Bead: bob-cli-dp.3 — Forward Justfile overrides through the editable reinstall

[Bead Pages](../README.md) / [bob-cli-dp](README.md) / bob-cli-dp.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-df.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.land.md) · **Assignee:** `bob-cli-dp.3` · **Size:** medium
**Created:** 2026-10-28 11:23:29 EDT · **Closed:** 2026-10-28 11:49:51 EDT
**Plan:** [202610/backlog\_batch\_b5.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_b5.md)

## Description

editable-reinstall-overrides: resolve bob-cli-di in sase Justfile _install-venv/_setup/_core-overrides-arg by forwarding the effective venv_dir/sase_core_dir settings (or binding the actual local wheel) through the nested just _core-overrides-arg call used in editable reinstalls, preserving normal published-pin resolution when no local core is requested. Regression-test both source (SASE_CORE_DIR) and SASE_CORE_WHEEL paths. Verify the installed wheel provenance/version before interpreting test results.

## Notes

[2026-10-28T15:41:18Z · bob-cli-dp.3] Helper + live repro: --set sase_core_dir with fake Cargo.toml emits --overrides into the scratch venv; bare nested just _core-overrides-arg emits empty (published-pin path). SASE_CORE_WHEEL emits overrides into --set venv_dir. Dry-run install-venv/_setup/_setup-visual/_setup-terminal-smoke/_setup-demos all forward --set venv_dir and --set sase_core_dir. tests/test_justfile_sase_core_dir.py: 31 passed. This clone has sase-core-rs 0.42.7 published (no .sase-core-rs-source.json; default sase_core_dir ../sase-core is absent).

[2026-10-28T15:49:46Z · bob-cli-dp.3] PROPOSED FOLLOW-UP: sase just check lint(symvision) fails importing private _RecoveryAssessment — ToolRun d6a84ef0ab38f1b655e7569a22f79be8; identical on clean origin/master at src/sase/finalizers/_failed_close_recovery_assess.py; this phase only changed Justfile and tests/test_justfile_sase_core_dir.py; no matching bob-cli task bead

[2026-10-28T15:49:51Z · bob-cli-dp.3] Forwarded --set venv_dir and --set sase_core_dir through every nested just _core-overrides-arg in _setup/_install-venv/_setup-visual/_setup-demos/_setup-terminal-smoke. Isolated helper: --set sase_core_dir emits overrides, bare nested call is empty (published pin), SASE_CORE_WHEEL writes overrides into --set venv_dir. tests/test_justfile_sase_core_dir.py 31 passed in sase .venv (sase-core-rs 0.42.7 published, matches pyproject pin, no source stamp). Live repro: bare=[], forwarded and wheel emit --overrides. sase tool run check d6a84ef0ab38f1b655e7569a22f79be8: fmt/ruff/mypy passed; lint(symvision) failed on pre-existing _RecoveryAssessment private import, reproduced on clean HEAD. epic-symbols: none. Did not close parent bob-cli-dp or task bob-cli-di.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-dp.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-dp.3/README.md) | [bob-cli-dp.3](bob-cli-dp.3.md) | 0 |
