# Bead: bob-cli-3j.9 — Finish shell completion — correct results, bash insertion, and an honest lifecycle

[Bead Pages](../README.md) / [bob-cli-3j](README.md) / bob-cli-3j.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-3j.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-3j.land.md) · **Assignee:** `bob-cli-3j.9.land`
**Created:** 2026-10-02 14:29:06 EDT · **Closed:** 2026-10-02 15:39:38 EDT
**Plan:** [202610/shell\_completion\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/shell_completion_landing_fixes.md)

## Description

Every shell-completion reply means what bob itself would do with it, bash inserts exactly what bob returned, and `bob completion` / `just install` probe quickly from a real terminal and report registration, exit codes, and closers honestly — so epic bob-cli-3j can land.

## Notes

[2026-10-02T19:39:38Z · bob-cli-3j.9.land] Verified both closed phases against the plan, the source, and the commits.

results (712d277, bob-cli-3j.9.1): shell_completion's PomodoroBlockId arm calls build_block_id_field and offers existing tasks only for Link intent; new and project-note intent offer the field's suggestions as new block IDs. VaultSoon is gone and the generic text slot is FreeText. value_lines prefers a path-specific kinds entry, then a non-Unknown ValueHint, then a generic entry. PDF *.pdf output is scoped to highlights clip and highlights create. An empty cursor word at a non-trailing positional with a value decision offers that slot. The bash adapter strips every COMP_WORDBREAKS character, leaves an open quote unescaped, %q-escapes other unquoted values, and filters !files-in by the text after the kept prefix. Docs and goldens cover solo @dev:, body-bearing new IDs, and =x/=*/=! offering nothing.

lifecycle (8f01f33, bob-cli-3j.9.2): probes call setsid, kill the process group at the deadline, and drain stdout on a reader thread. compinit runs only when _comps is unset. status does not probe or fail a shell with no file and no manifest entry, and status without -v never spawns a shell. Install with no SHELL arguments selects $SHELL plus owned adapters; -t with no SHELL arguments selects only $SHELL. not registered / shadowed / bound render fail and exit 1; unverified warns and exits 0; -n says registration was not checked. Dry runs print no closer, and "Completion is live" prints only when every row is unchanged and registered. An unrecorded stamped file with different bytes is outdated (externally managed) and refused without -f. A -t move removes a matching previous adapter. The ~/.zfunc home default always prints the fpath line. needless_option_as_deref at verify.rs is gone.

Tests this turn: cargo test --lib and --test cli, filter completion. 130 lib tests passed. 105 cli completion tests passed, including the new readline e2e, the no-stall zpty probe, close-shorthand goldens, ValueHint goldens, and the lifecycle cases. completion::zsh_adapter::default_styles_use_green_headers failed only because this process exports NO_COLOR=1 and the stubbed driver inherits it; env -u NO_COLOR passes that test, and no_color_uses_plain_header passed in the same run. _bob.zsh and that test were not changed by either 3j.9 commit. Recorded on the parent as a blocker. just check and just symvision are not recipes in this justfile. No --epic-symbol entries.

Integration: the only commits after this epic was created are its own, and 712d277 is stacked on 8f01f33. The in-flight capture commits 74f47d4 and f589d07 are covered by the results goldens (close_shorthands_offer_nothing and named_start_after_inline_close passed). 0791fb6 does not touch completion. In-progress epic bob-cli-3l has not committed on master.

Follow-ups:
- bob-cli-3j.9.1 zpty empty-write gotcha: declined, no task. The lifecycle zpty driver sends a non-empty zpty -w command (zsh appends the newline) and probe_without_controlling_terminal_via_zpty passed. The bash readline tests already send Enter as zpty -w -n $'\r'.
- bob-cli-3j.9.2 clippy deny at tests/cli/capture/pomodoro_name.rs:808: no new task. Same || true assertion already owned by in-progress epic bob-cli-28. Corroborated there as a DISCOVERED ISSUE from this landing, naming bob-cli-3j.9.2. Weekly task sweep and a task search found no separate bead.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-3j.9.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-3j.9.land/README.md) | [bob-cli-3j.9](bob-cli-3j.9.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli--plans | [`bob-cli--plans@2517d71`](https://github.com/bobs-org/bob-cli--plans/commit/2517d712c79cacc372160cb3b8537d0606910c27) | docs(plan): mark shell completion landing fixes done | [bob-cli-3j.9](bob-cli-3j.9.md) | 2026-10-02 15:40:59 EDT |
