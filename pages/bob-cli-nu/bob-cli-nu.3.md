# Bead: bob-cli-nu.3 — run:/bob-run grammar, command-chip cursor rule, and vectors

[Bead Pages](../README.md) / [bob-cli-nu](README.md) / bob-cli-nu.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5k.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5k.linker.w0.md) · **Assignee:** `bob-cli-nu.3` · **Size:** medium
**Created:** 2026-11-20 05:59:33 EST · **Closed:** 2026-11-20 07:25:45 EST
**Plan:** [202611/command\_chips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/command_chips.md)

## Description

grammar: build the pure run: and bob-run grammar on the shared scanner, with a serializer, link spans, and the command-chip chipAt rule (under cursor, link, line, task). Publish the pure members of api.commandChips v1, pinned by JSON vectors and a round-trip test.

## Notes

[2026-11-20T12:25:14Z · bob-cli-nu.3] PROPOSED FOLLOW-UP: copyChipSerialize can emit a bob-copy fence that an indented body line closes early — it counts fence runs only at column 0, so text "a\n  ```\nb" serializes with a ``` marker and the "  ```" body line closes it (payload truncates to "a"). runChipSerialize avoids this with closerAware; copy was left byte-stable for C11. Fix by counting runs after leading whitespace, update copy vectors deliberately, and re-pin COPY_VECTORS_SHA256 in scripts/test-command-chips-grammar.cjs.

[2026-11-20T12:25:21Z · bob-cli-nu.3] PROPOSED FOLLOW-UP: commandChipAt only shields run chips inside math and comments that open on the same line. A run chip inside a multi-line %% / <!-- --> comment block or a $$ block that opened on an earlier line still resolves for ⌘↵ (Live Preview hides it via the syntax tree, the pure rule does not). The keymap phase (bob-cli-nu.6) or a small follow-up should track cross-line comment and math state in commandChipAt, outside fences.

[2026-11-20T12:25:28Z · bob-cli-nu.3] PROPOSED FOLLOW-UP: pre-existing check failures that reproduce on the clean base: (1) docs-check published URLs: docs/develop/plugins/architecture.md:74 -> /develop/validation/ (bob-plugins docs/develop/architecture.md quotes `docs/develop/validation.md`; same failure on a clean bf13f43 worktree; also noted by bob-cli-nu.2 and bob-cli-nh.7.1.3); (2) load-sensitive 25 ms perf flakes in test:unit, already tracked by bob-cli-io (frees-marks) and bob-cli-km (event-link-times); both pass alone.

[2026-11-20T12:25:45Z · bob-cli-nu.3] Grammar phase done in bob-plugins plugins/bob-chips (0.6.0 -> 0.7.0), rebased onto the engine commit 591998e. Shared one-pass chipScanLine (kind-tagged copy|run; run spans also skip same-line math and %%/HTML comments); copyChipScanLine is now its copy filter. runChipParseContent / runChipScanLine / runChipParseFenceInfo / runChipSerialize (bob-run fence; refuses a block in a table cell; fence marker outruns indented closer-like lines); chipLinkSpans (md links and images, wikilinks and embeds, autolinks, bare http(s) URLs, outside code spans); commandChipAt implements rules 1-7 with frozen none / ambiguous{via,message} / ready{via,chip}; block chips carry fence:{open,close}; task scan generalized as chipScanTaskScope. api.commandChips v1 (version, parse, scanLine, parseFenceInfo, fencePayload, serialize, chipAt) beside the unchanged copyChips v2, plus a fallback namespace. Verified: scripts/fixtures/command-chips-vectors.json (20 chips, 22 non-chips, 4 mixed, 15 serialize, 10 fence_info, 16 link_spans, 33 chip_at covering every state and via); test-command-chips-grammar.cjs (pins the copy vectors sha256) and test-command-chips-roundtrip.cjs (5000-case property test), both in test:unit; a 200k-case differential fuzz of copy parse/scan/fenceInfo/serialize/chipAt against the pre-change bundle was byte-identical; 202/202 chip and copy-card tests; test:perf 9/9 (Live Preview at 21.6 of 35 ms); build:check, docs:inventory:check, and validate (12/12) green; docs-check lint, drift, and strict build pass. Docs: bob-chips.md "Command chip grammar" plus the ⌘↵ rule; plugin-apis.md "Command chips". Deployed with bob plugins sync -p bob-chips: synced and enabled, the vault bundle matches the build, and a smoke load of the vault bundle answers commandChips.chipAt. The only full test:unit and docs-check failures are pre-existing (see the follow-up notes).

## Dependencies

- **Depends on:** [bob-cli-nu.1](bob-cli-nu.1.md) ✓ · ⧖ 2026-11-20
- **Blocks:** [bob-cli-nu.4](bob-cli-nu.4.md) ◐ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-nu.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.3/README.md) | [bob-cli-nu.3](bob-cli-nu.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@c8da83f`](https://github.com/bobs-org/bob-plugins/commit/c8da83fda53b966c1b6e2eb6127efc3da9658bb2) | feat(bob-chips): add run:/bob-run grammar and command-chip cursor rule | [bob-cli-nu.3](bob-cli-nu.3.md) | 2026-11-20 07:26:44 EST |
