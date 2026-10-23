# Bead: bob-cli-at.3 — Coordinated marker writes, holds, and human reporting

[Bead Pages](../README.md) / [bob-cli-at](README.md) / bob-cli-at.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.56.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.56.linker.w0.md) · **Assignee:** `bob-cli-at.3` · **Size:** medium
**Created:** 2026-10-23 11:44:15 EDT
**Plan:** [202610/highlights\_coordinated\_marker\_writes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_coordinated_marker_writes.md)

## Description

executor: when the policy is on, wrap each marker-write PDF's whole v1/v2 write sequence in one coordinated accessor. That covers scan (human and JSON), `ref sync -w`, and create-time ingest. Inside the accessor, re-check the PDF first. Same digest: write as today. Changed digest with the same marker: write to the freshly located annotation and record saved-first. Changed marker: hold `marker_changed`. Add the `editor_active` reading hold for unattended scans only, plus the new `-a, --attended` scan flag, and the `coordination_timeout` hold with the per-PDF budget and scan cap. Add `ScanWriteOutcome::Held` and the marker-write report (mode, saved-first, status transition, wait time). Holds exit 0. Add the yellow `held` concise line, the summary count, and the verbose and `ref sync` lines. JSON mode counts holds as neither notes nor failures for now. With the key off, output stays byte-identical. Document the contract and the config key, then run `just docs-gen` for the flag.

## Dependencies

- **Depends on:** [bob-cli-at.1](bob-cli-at.1.md) ◐ · ⧖ 2026-10-23
- **Depends on:** [bob-cli-at.2](bob-cli-at.2.md) ✓ · ⧖ 2026-10-23
- **Blocks:** [bob-cli-at.4](bob-cli-at.4.md) ◐ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-at.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-at.3/README.md) | [bob-cli-at.3](bob-cli-at.3.md) | 0 |
