# Bead: bob-cli-gg.3 — Real-Obsidian e2e and visual review (bob-plugins, bob-cli)

[Bead Pages](../README.md) / [bob-cli-gg](README.md) / bob-cli-gg.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.ca](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.ca.md) · **Assignee:** `bob-cli-gg.3` · **Size:** medium
**Created:** 2026-11-03 10:19:38 EST · **Closed:** 2026-11-03 12:03:55 EST
**Plan:** [202611/event\_link\_times.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/event_link_times.md)

## Description

live_verify: isolated real-Obsidian e2e with light/dark screenshots, then a Live verification section in the bob-cli contract.

## Notes

[2026-11-03T15:39:42Z · 17b--code] COORDINATION NOTE (from a planning agent; not remaining work and not an earlier attempt at this phase): Read the CROSS-EPIC COORDINATION note on epic bob-cli-gg. Item 4 applies to every `bob plugins sync` in this phase. If gf has landed, cover EP3 and item 6 (pill dashed exactly when the chip shows) in the live run.

[2026-11-03T17:01:18Z · bob-cli-gg.3] PROPOSED FOLLOW-UP: Regenerate docs/reference/glossary.md and rerun both docs gates — clean-base docs checks report stale generated drift there; this phase did not change glossary sources.

[2026-11-03T17:01:28Z · bob-cli-gg.3] SYNC PENDING: bob-ledger-tools deploy — npm run build leaves the current master output unchanged and includes both feature commits, but bob plugins sync --no-pull --repo refuses to replace its recorded uncommitted build from bob-cli_10; the epic coordination rule forbids -F.

[2026-11-03T17:03:55Z · bob-cli-gg.3] Added isolated real-Obsidian event-link timing E2E harness and Live verification contract section; offline self-test, registered Node test, build:check, syntax checks, and diff checks pass. The live run correctly reported skipped because /snap/bin/obsidian is unavailable here, so it produced no screenshots or live timings. Docs generated glossary drift and the guarded plugin sync refusal are recorded in phase notes.

## Dependencies

- **Depends on:** [bob-cli-gg.2](bob-cli-gg.2.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-gg.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gg.3/README.md) | [bob-cli-gg.3](bob-cli-gg.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a5e1c51`](https://github.com/bobs-org/bob-cli/commit/a5e1c519a3aa749b50106ab2a122e21fdb4b086f) | docs(event-link-times): record live verification | [bob-cli-gg.3](bob-cli-gg.3.md) | 2026-11-03 12:10:52 EST |
| bob-plugins | [`bob-plugins@9b5b285`](https://github.com/bobs-org/bob-plugins/commit/9b5b2857f02f441cd2920b1f7738522b2ddc8b57) | test(event-link-times): add isolated Obsidian e2e | [bob-cli-gg.3](bob-cli-gg.3.md) | 2026-11-03 12:11:29 EST |
