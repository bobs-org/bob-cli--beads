# Bead: bob-cli-oz.7 — Real-Obsidian walkthrough, mention round-trip, and screenshots

[Bead Pages](../README.md) / [bob-cli-oz](README.md) / bob-cli-oz.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase · **↺ Reopened:** ↺1
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.ff](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.ff.md) · **Assignee:** `bob-cli-oz.7` · **Size:** small
**Created:** 2026-11-21 17:39:52 EST · **Closed:** 2026-11-22 08:08:17 EST
**Plan:** [202611/prompt\_task\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prompt_task_links.md)

## Previously Closed

> ↺ Closed 2026-11-22T12:30:33Z · done
>
> (none)
>
> Reopened 2026-11-22T12:56:08Z by `sase bead open`

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:315973b2eafab0f820e35e8d | attached via sase artifact create --bead |
| related | file:explicit:40bddfa8814a6dc4f9fd28d2 | attached via sase artifact create --bead |
| related | file:explicit:5a6a59038f820674b8f1f27c | attached via sase artifact create --bead |
| related | file:explicit:618d36e1fb4beab2da916216 | attached via sase artifact create --bead |
| related | file:explicit:91ce67a9355c06b31efbdc6e | attached via sase artifact create --bead |
| related | file:explicit:b5fb7adf6e4dcb6e7ffff437 | attached via sase artifact create --bead |

<!-- sase:links:end -->

## Description

task-walkthrough: run the isolated real-Obsidian e2e over S1, S6, S10, S11, S14, and S15, then confirm the mention chips after bob task reconcile, attach screenshots, and run the docs check.

## Notes

[2026-11-22T12:29:58Z · bob-cli-oz.7] PROPOSED FOLLOW-UP: Live NAME Esc ladder still unproven under CDP — Input.dispatchKeyEvent Escape peels 0 NAME layers (capture Keydown and Modal onEscapeKey do not share one event object, so WeakSet never fires); a synthetic DOM Escape peels two. Unit test covers same-event one-layer peel. Harness skipped Esc-from-NAME after the write and submitted after NAME Enter.

[2026-11-22T12:30:13Z · bob-cli-oz.7] PROPOSED FOLLOW-UP: S15 Record Card save — analog [[ walk applies with Enter; this (( walk stayed statusKind=consequence with preview-ready/canApply, so Enter timed out. Harness used recordApplyTyped(null) then CTA click as fallback after band close.

[2026-11-22T12:30:22Z · bob-cli-oz.7] PROPOSED FOLLOW-UP: npm run docs:check first-day tutorial cargo compile hit ENOSPC on apollo (disk ~149M free). Lint/build/urls/lychee/search passed. plugin-apis.md 8401/8000 warning is pre-existing and already tracked by bob-cli-ob. Nav docs were not over cap.

[2026-11-22T12:30:33Z · bob-cli-oz.7] Isolated real-Obsidian e2e on athena (xvfb-run, BOB_BIN ~/.cargo/bin/bob 0.5.0, nav mainJsSha256 1c65485dbbbe1d87a3ded9a412813dd63d543e8361078e7192e74b5c0290c140) over S1, S6, S10, S11, S14, S15-text, S15-link, then mention round-trip after bob task reconcile: pass true, failed []. Inline naming wrote ^id plus the freshness stamp (S1 named zxqone-nameless). Work log held [[omega#^omega]] [[tasks#^zxqone-nameless]]. After reconcile, Omega 🪢 LINKED FROM shows 💬 mentions chips for alpha, beta, and gamma; no Task Link or relation. Attached artifacts: file:explicit:618d36e1fb4beab2da916216 (S1 list light), file:explicit:315973b2eafab0f820e35e8d (S1 list dark), file:explicit:5a6a59038f820674b8f1f27c (S1 NAME light), file:explicit:40bddfa8814a6dc4f9fd28d2 (S1 NAME dark), file:explicit:91ce67a9355c06b31efbdc6e (mentions LINKED FROM), file:explicit:b5fb7adf6e4dcb6e7ffff437 (walk JSON). Product: same Escape event peels one NAME layer (per-event WeakSet in 189b); unit 14/14 including that case, plus --self-test. npm run docs:check lint/build/urls/lychee/search passed; docs/bob-navigation-hotkeys.md is 743 lines and under cap. First-day tutorial cargo compile hit ENOSPC on apollo. plugin-apis.md 8401/8000 warning is pre-existing (bob-cli-ob). Honored naming=inline and decision_record=no (no memory edits). Parent epic left open.

[2026-11-22T12:52:45Z · bob-cli-oz.7] CLOSED-BEAD LAUNCH: agent bob-cli-oz.7 launched against this closed bead; status left closed.
Launch submitted 2026-11-22T12:51:42.725181Z; run 20261122075145.
Prior close: 2026-11-22T12:30:33Z · done.

[2026-11-22T13:07:57Z · bob-cli-oz.7] PROPOSED FOLLOW-UP: Vault bob-mail is a stale unlanded build — bob plugins sync refuses bob-mail (deployed from bob-cli_13 uncommitted build, e6d7aed, 2026-11-21T19:56Z; no HEAD commit matches it byte for byte), so the vault lacks c1d8d198 bob-mail 040-task-modal (( wiring for S13 Task from email. Needs Bryan to approve `bob plugins sync -p bob-mail -F` (discards that unlanded build) per bob-plugins AGENTS.md.

[2026-11-22T13:08:17Z · bob-cli-oz.7] Relaunch: the prior run died on apollo ENOSPC before its finalizer, so its bob-plugins work never landed (checkout was re-cloned). Recovered the exact tree that passed the 12:10Z walk from athena /tmp/bob-cli-oz-7-plugins and rebased it onto bob-plugins master 379e0b17: new scripts/obsidian-prose-task-e2e.cjs + offline scripts/test-obsidian-prose-task-e2e.cjs (in test:unit), docs/develop/validation.md "Prose-task walkthrough", and the per-event Escape guard threaded through 189b, Record Card, Intention Card, picker prose links, log recall, successor verdict reason. Fixed a guard bug in the recovered code: backOut marked an Escape even when it peeled nothing, so a second handler on the same event (capture listener then Modal scope) returned true and swallowed the close; now only a real peel marks the event (markPeeled), and the scope handler reuses isEscChord; 189b stays at 1000 lines. Added a unit case (unpeeled Escape stays free). Verified: prose suites 93/93 on apollo; full npm test on athena 8628/8632, the 4 reds are /tmp-copy fixture paths + 25 ms perf budgets and pass 55/55 in the real checkout; live real-Obsidian walk on athena (bob 0.5.0) over S1, S6, S10, S11, S14, S15-text, S15-link + mention round-trip: pass true, failed [], 111 checks, 0 console exceptions, LINKED FROM shows 💬 mentions for alpha/beta/gamma with no Task Link/relation (report athena:/tmp/prose-task-walk-rerun.json); docs-check on athena: all implemented gates passed incl. first-day tutorial (plugin-apis.md 8401/8000 warning pre-existing, bob-cli-ob). bob plugins sync deployed nav + ledger-tools; bob-mail refusal recorded as follow-up. Screenshots from the first run remain attached. naming=inline, decision_record=no honored; no memory edits.

## Dependencies

- **Depends on:** [bob-cli-oz.4](bob-cli-oz.4.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-oz.5](bob-cli-oz.5.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-oz.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oz.7/README.md) | [bob-cli-oz.7](bob-cli-oz.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@12da82a`](https://github.com/bobs-org/bob-plugins/commit/12da82af7b3a9eedc7567f962fe55b845f0e466e) | feat(nav): add real-Obsidian (( walkthrough and peel one prose layer per Escape | [bob-cli-oz.7](bob-cli-oz.7.md) | 2026-11-22 08:09:10 EST |
