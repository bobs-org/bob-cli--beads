# Bead: bob-cli-nu.4.1.2 — Shared command-chip state and activation

[Bead Pages](../README.md) / [bob-cli-nu.4.1](bob-cli-nu.4.1.md) / bob-cli-nu.4.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-nu.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-nu.4.md) · **Assignee:** `bob-cli-nu.4.1.2` · **Size:** medium
**Created:** 2026-11-20 07:37:00 EST · **Closed:** 2026-11-20 08:43:45 EST
**Plan:** [202611/command\_chips\_inline.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/command_chips_inline.md)

## Description

runtime: add source policy, cached resolution, CommandChipRunStore, and commandChipActivate with stale checks, a synchronous latch, output deduplication, copy-only behavior, and cleanup. Publish shared hooks for renderers and the outer fence/keymap phases.

## Notes

[2026-11-20T13:42:57Z · bob-cli-nu.4.1.2] CONTRACT FOR LIVE/READING/FENCE/KEYMAP (bob-chips 0.8.0): new fragments 067-command-policy.js (commandChipEligibility(app, ctx) -> frozen {mode run|copy, reason, sourcePath, engine}; no-run roots mail/ref/ref_history/.bob/_conflicts case-insensitive; query origin needs ctx.sourceVerified===true; ctx.resolveSourcePath() wins; commandChipResolveSourceLink, commandChipLiveSourceCheck(view,{from,to,raw}), commandChipTextSourceCheck(text,{line,from,to,raw}), commandChipCheckSource(ctx)), 068-command-run-store.js (CommandChipRunStore: snapshot/subscribe/subscribeAll/begin/apply/settle/revert/fail/rekey/tryLatch/settleLatch/claimOutput/setArmed/armedTarget/isArmed/dispose; states idle|pending|queued|running|completed(1.6 s)|attention|failed; pending paints as resting; keys = signature or text:+payload; commandChipTargetId uses chipAt coords, block chips by fence.open), 069-command-runtime.js (plugin.commandChipRuntime {store, cache}; commandChipPaintModel(plugin, chip, ctx) -> frozen {face, mode, reason, verdict, key, snapshot, armed, sourcePath}; commandChipOnCatalogChanged(plugin, fn); one workspace catalog-changed subscription per plugin), 075-command-activate.js (commandChipActivate(chip, ctx) with ctx.plugin required; settles frozen {action run|open|copy|output|duplicate|stale|refused|inert|error, ok, stage, outcome, reason, runId, sequenceId, signature}; ctx.copyFeedback(result) optional, else copy feedback on ctx.element). All exported via module.exports.helpers; documented in docs/develop/plugin-apis.md#command-chip-runtime-internal.

[2026-11-20T13:43:08Z · bob-cli-nu.4.1.2] PROPOSED FOLLOW-UP: baseline check failures, not caused by this phase — `npm run docs:check` fails only its published-URL step on docs/develop/plugins/architecture.md:74 -> /develop/validation/ (reproduced identically in a clean HEAD 52b7c31 worktree; tracked by bob-cli-nv); full `npm test` (7682 tests) fails only the load-sensitive 25 ms perf asserts in test-ledger-tools-event-link-times.cjs and test-ledger-tools-frees-marks.cjs (40/40 green in isolation; tracked by bob-cli-km and bob-cli-io).

[2026-11-20T13:43:16Z · bob-cli-nu.4.1.2] PROPOSED FOLLOW-UP: docs word budget — docs/develop/plugin-apis.md is now ~7,830 words (wc) against the 8,000-word develop/ cap (warning severity); the live, reading, and evidence phases each add command-chip contracts there, so the land agent may need to move the command-chip API/runtime contracts to their own develop page (nav + url contract change) or trim.

[2026-11-20T13:43:45Z · bob-cli-nu.4.1.2] Runtime landed in the bob-plugins working tree (Bob Chips 0.7.0 -> 0.8.0, deployed with bob plugins sync; bob plugins list shows bob-chips 0.8.0 synced). New fragments 067-command-policy.js (source/host/engine eligibility and fresh source checks), 068-command-run-store.js (CommandChipRunStore with pending/queued/running/completed 1.6 s/attention/failed, 400 ms+acceptance latch, output dedup, armed target with source+span identity), 069-command-runtime.js (bounded resolve cache per engine+catalog token+payload, loading never cached, one catalog-changed subscription per plugin, paint model), 075-command-activate.js (commandChipActivate: copy-only path, stale check, sync latch before any await, post-await recheck, runText/openText with only {source,onState}, card/preview revert, one Notice per refusal/failure, no retry, Alt inert); wired into 090-plugin.js setup/unload and 099-exports.js; api.commandChips v1 and api.copyChips v2 unchanged. Verified: scripts/test-command-chips-runtime.cjs 34/34 (5 repeat runs) covering every transition, duplicate signatures across mounts, async-read coalescing, sub-400 ms completion, shift opening, exceptions, mid-run rebuild, timer races, source/mobile/engine policy, no task/walk plugin access, and two real Command Mode engine runs against fake bob (exact argv once on double click; failing step 2 halts with persistent failed ink). npm run build and validate pass; full npm test 7676/7682 with only the known load-sensitive ledger perf asserts failing (40/40 in isolation; bob-cli-km, bob-cli-io); docs:check passes lint/drift/strict build and fails only the baseline published-URL step reproduced identically on a clean HEAD worktree (bob-cli-nv). Internal contract documented in docs/develop/plugin-apis.md (Command-chip runtime (internal)). No epic symbols.

## Dependencies

- **Depends on:** [bob-cli-nu.4.1.1](bob-cli-nu.4.1.1.md) ✓ · ⧖ 2026-11-20
- **Blocks:** [bob-cli-nu.4.1.3](bob-cli-nu.4.1.3.md) ✓ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-nu.4.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.2/README.md) | [bob-cli-nu.4.1.2](bob-cli-nu.4.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@e902351`](https://github.com/bobs-org/bob-plugins/commit/e902351ee65cdacfecc63349854fe00af57241a4) | feat(bob-chips): add shared command-chip runtime and activation | [bob-cli-nu.4.1.2](bob-cli-nu.4.1.2.md) | 2026-11-20 08:44:26 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nu.4.1.2][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-nu.4.1.3][2] | Need runtime phase notes to see what landed | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.3/README.md

<!-- sase:referenced-by:end -->
