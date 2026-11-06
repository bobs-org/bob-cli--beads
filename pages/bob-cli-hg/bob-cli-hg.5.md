# Bead: bob-cli-hg.5 — Mail note layout, label, path, index, and append-only refresh

[Bead Pages](../README.md) / [bob-cli-hg](README.md) / bob-cli-hg.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.cn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.cn.md) · **Assignee:** `bob-cli-hg.5` · **Size:** medium
**Created:** 2026-11-05 12:37:49 EST · **Closed:** 2026-11-05 23:31:32 EST
**Plan:** [202611/bob\_gmail.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_gmail.md)

## Description

mail-note: assemble rendered messages into the mail note file (frontmatter, summary, cards, markers), compute paths and link labels, parse existing notes, merge refreshes append-only, index saved threads, and template the mail hub.

## Notes

[2026-11-06T04:30:57Z · bob-cli-hg.5] PROPOSED FOLLOW-UP: Triage clean-base just check CLI expectation drift — three capture::successor_verdicts assertions, catalog protocol 1 expected count (73 vs 72), and the root-help snapshot missing the Gmail row all fail identically on HEAD; catalog/root-help drift was also recorded in bob-cli-ho #2, and duplicate clipboard failures are tracked by bob-cli-hp.

[2026-11-06T04:31:32Z · bob-cli-hg.5] Implemented Gmail mail-note layout, labels, paths, frontmatter index, hub templates, and append-only refresh. `just check` passed Clippy and all native::gmail::note tests; its unrelated library/CLI failures reproduced identically on clean HEAD and are recorded in the phase follow-up (clipboard cases already tracked by bob-cli-hp).

## Dependencies

- **Depends on:** [bob-cli-hg.3](bob-cli-hg.3.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hg.6](bob-cli-hg.6.md) ◐ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.5/README.md) | [bob-cli-hg.5](bob-cli-hg.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`cfdb68c`](https://github.com/bobs-org/bob-cli/commit/cfdb68c17552da6e13fa0e2f918565bf0aca8f12) | feat(gmail): implement mail note layout and refresh | [bob-cli-hg.5](bob-cli-hg.5.md) | 2026-11-05 23:32:54 EST |
