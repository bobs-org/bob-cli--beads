# Bead: bob-cli-nu.4.1.1 — Complete the engine contract consumed by inline chips

[Bead Pages](../README.md) / [bob-cli-nu.4.1](bob-cli-nu.4.1.md) / bob-cli-nu.4.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-nu.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-nu.4.md) · **Assignee:** `bob-cli-nu.4.1.1` · **Size:** medium
**Created:** 2026-11-20 07:37:00 EST · **Closed:** 2026-11-20 08:15:23 EST
**Plan:** [202611/command\_chips\_inline.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/command_chips_inline.md)

## Description

engine-contract: complete additive resolver metadata, signature lookup, per-run state callbacks, loading behavior, and catalog invalidation. Preserve existing Command Mode consumers and guards; add focused contract regressions.

## Notes

[2026-11-20T13:14:51Z · bob-cli-nu.4.1.1] PROPOSED FOLLOW-UP: baseline check failures, not caused by this phase — `npm run docs:check` fails only its published-URL step on docs/develop/plugins/architecture.md:74 -> /develop/validation/ (reproduced identically on a clean HEAD worktree; tracked by bob-cli-nv); full `npm test` fails only the load-sensitive 25 ms perf asserts in test-ledger-tools-event-link-times.cjs and test-ledger-tools-frees-marks.cjs (both 40/40 green in isolation; tracked by bob-cli-km and bob-cli-io).

[2026-11-20T13:14:59Z · bob-cli-nu.4.1.1] PROPOSED FOLLOW-UP: report rows with a preview-first policy cannot run from Ctrl+Enter or a chip — the sheet report path (and so runText/openText report stage) calls runner.run without skipGuards, so the runner refuses "Run the preview first". No catalog entry has that combination today; decide whether chip/Ctrl+Enter report runs should pass skipGuards when no confirm guard applies.

[2026-11-20T13:15:05Z · bob-cli-nu.4.1.1] CONTRACT FOR RUNTIME (nu.4.1.2): api.commandMode (bob-command-mode 0.4.0) adds resolve(text) -> frozen {ok,state: ready|invalid|unavailable|loading, signature, steps[{index(1-based),text,argv,entryId,entry_id,title,effect,policy,presentation,hasPreview,confirm}], reason, step}; runText(text,{source,onState}) -> {ok, stage: run|sequence|output|confirm|review|refused, outcome (opened for cards, refused for not-ready), runId, sequenceId, reason?, duplicate? }; onState frozen {state: queued|running|step|finished, kind: run|sequence, signature, runId, sequenceId, step, total, outcome, reason, exitCode, stoppedAt} — exactly one finished per activation that reached execution, none for refusals/cards; activeRun(signature) -> frozen {kind,state,runId,sequenceId,step,total,...} (works between sequence steps, runId = last finished step); catalogInfo() -> frozen {state,status,ready,loading,fingerprint,generation,token}; onCatalogChanged payload {catalog,bobVersion,fingerprint,generation,token,reason}, fired on first usable catalog and on content/fingerprint change. Source line is zero-based-safe (non-negative ints kept). Exact shapes: docs/develop/plugin-apis.md#command-chip-members.

[2026-11-20T13:15:23Z · bob-cli-nu.4.1.1] Engine contract landed in bob-plugins working tree (bob-command-mode 0.3.0 -> 0.4.0, deployed via bob plugins sync; vault main.js byte-matches the build). resolve(text) now frozen with state ready/invalid/unavailable/loading, signature, 1-based failing step/reason, and immutable step metadata (index, trimmed original text, argv, entryId/entry_id, title, effect, policy, presentation, hasPreview, confirm); splitter handles quote-aware && and newline steps, empty-step refusal, literal bob, aliases, exclusions, missing args, host restrictions, and unquoted shell/variable syntax (; | || & > >> < backtick $( ${ $NAME $1). runText/openText whitelist {source,onState}, wait <=5 s only for an in-flight catalog load, and settle normalized stages (run/sequence/output/confirm/review/refused; cards = outcome opened, no events). Guarded per-run onState hooks ride runner records (queued/running) and sequence callbacks (step) with one distinct finished per activation. activeRun(signature) matches immutable sequence signatures, including between steps. Catalog announces on first usable catalog and on fingerprint change even with identical JSON, with fingerprint/generation/token and catalogInfo(). Fixed: runner same-argv race across the save-all await (mutation-tested), unknown-policy confirm guard, provenance rules (vault-relative <=512, non-negative line). Verified: 16 new contract tests + resolve vector fixture (52 vectors); full npm test 7642 pass, only the tracked 25 ms perf flakes fail (green in isolation; bob-cli-io/km); npm run validate 12/12; docs:check passes lint/drift/strict build, fails only the baseline URL check reproduced on clean HEAD (bob-cli-nv). Docs: plugin-apis.md Command-chip members + bob-command-mode.md.

## Dependencies

- **Blocks:** [bob-cli-nu.4.1.2](bob-cli-nu.4.1.2.md) ✓ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-nu.4.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.1/README.md) | [bob-cli-nu.4.1.1](bob-cli-nu.4.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@52b7c31`](https://github.com/bobs-org/bob-plugins/commit/52b7c31486f3594cc0fe663e7ad0487e4d82c10d) | feat(bob-command-mode): complete the command-chip engine contract | [bob-cli-nu.4.1.1](bob-cli-nu.4.1.1.md) | 2026-11-20 08:16:21 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nu.4.1.1][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-nu.4.1.2][2] | Check engine-contract phase notes for API shapes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.2/README.md

<!-- sase:referenced-by:end -->
