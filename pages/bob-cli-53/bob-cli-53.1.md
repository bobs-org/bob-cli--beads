# Bead: bob-cli-53.1 — Date marks in bob-ledger-tools

[Bead Pages](../README.md) / [bob-cli-53](README.md) / bob-cli-53.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0xq](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0xq.md) · **Assignee:** `bob-cli-53.1` · **Size:** medium
**Created:** 2026-10-07 08:19:07 EDT · **Closed:** 2026-10-07 08:55:32 EDT
**Plan:** [202610/task\_date\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_date_marks.md)

## Description

date-marks: add the pure date-mark core (a parser for several canonical date fields per line, the calendar label grammar, tooltips, the element, and the widget). Add the Live Preview extension with whitespace-run folding and per-field reveal, the rendered-view post-processor, the midnight rollover relabel, the session toggle, `api.dateMarks` v1, and the CSS glyph set, tones, and repair flag. Add the conformance tests and the authoritative `docs/date-marks.md` contract, then deploy with `bob plugins sync`.

## Notes

[2026-10-07T12:55:32Z · bob-cli-53.1] Date marks shipped: 34/34 new conformance tests pass, full plugin suite 2028/2028, npm run validate 6/6, build current, bob-ledger-tools 1.31.0 deployed to vault via plugins sync. Live Obsidian checklist pending for Bryan.

## Dependencies

- **Blocks:** [bob-cli-53.2](bob-cli-53.2.md) ✓ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-53.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-53.1/README.md) | [bob-cli-53.1](bob-cli-53.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`67f0cbb`](https://github.com/bobs-org/bob-cli/commit/67f0cbb7b48505f2caa88976fd40ae30de1eda4f) | feat(docs): add task date marks display contract (bob-cli-53.1) | [bob-cli-53.1](bob-cli-53.1.md) | 2026-10-07 08:56:51 EDT |
| bob-plugins | [`bob-plugins@d29034b`](https://github.com/bobs-org/bob-plugins/commit/d29034b42f5db394c05748ca0ffb21ae6ebfb58d) | feat(ledger-tools): render canonical task dates as compact date marks (bob-cli-53.1) | [bob-cli-53.1](bob-cli-53.1.md) | 2026-10-07 08:57:41 EDT |
