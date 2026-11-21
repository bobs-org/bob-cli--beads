# Bead: bob-cli-oj.1 — Group-link grammar, one resolver, and the \[N / \]N commands

[Bead Pages](../README.md) / [bob-cli-oj](README.md) / bob-cli-oj.1

**Status:** ○ open · **Type:** ↳ phase · **↺ Reopened:** ↺1
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1es](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1es.md) · **Assignee:** `bob-cli-oj.1` · **Size:** medium
**Created:** 2026-11-21 07:41:35 EST
**Plan:** [202611/bracket\_n\_group\_jumps.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bracket_n_group_jumps.md)

## Previously Closed

> ↺ Closed 2026-11-21T13:12:36Z · done
>
> (none)
>
> Reopened 2026-11-21T13:19:51Z by `sase bead open`

## Description

nav-grammar: in bob-navigation-hotkeys, tighten the `[n`/`]n` matcher so doubled arrows never step, recognize `«`/`»` (typed `<<`/`>>`) group links on link-only nav lines, build the one resolver (authored, then the Ledger Tools provider), add the group commands with the creation guard and repeat guard, route `[{`/`]}` on family `n`, publish `walkMode.links` v7, and map `[N`/`]N` in the vault vimrc.

## Notes

[2026-11-21T13:12:08Z · bob-cli-oj.1] Vault scan before matcher change: 0 live-vault notes use «/»/<<</>> link labels (only the research source doc holds plan-example « Part 2 / Part 4 » labels); nothing regresses.

[2026-11-21T13:12:15Z · bob-cli-oj.1] PROPOSED FOLLOW-UP: just docs-check lint fails on docs/reference/vault-format.md (6016 words, cap 6000) on the clean base tree; untouched by this phase.

[2026-11-21T13:12:19Z · bob-cli-oj.1] PROPOSED FOLLOW-UP: bob plugins sync refuses bob-ledger-tools (foreign uncommitted build from workspace bob-cli_11); nav-hotkeys 2.96.0 deployed, ledger left untouched per no -F rule.

[2026-11-21T13:12:23Z · bob-cli-oj.1] PROPOSED FOLLOW-UP: skipped memory change per decision memory_decision_group_stops=no (decisions-web record that group stops are derived on Bob notes and authored only on nav lines).

[2026-11-21T13:12:36Z · bob-cli-oj.1] nav-grammar done: doubled-arrow matcher, link-only nav-line group links with conflict/dedup, one resolver (authored then api.navGroups) with legacy step fill-in, openGroupLink with creation guard and repeat guard, [{/]} on family n, walkMode.links v7, [N/]N vimrc maps. Verified: npm run build, build:check, docs:gen, inventory:check green; 75 nav tests + plugin-build + walker-footer (141 total) pass; bob-navigation-hotkeys.md 5983 words within budget; manifest 2.96.0 committed (merge 726f9a5) and synced to vault (vault shows 2.96.0). Pre-existing docs-check failure on vault-format.md and foreign ledger-tools sync refusal recorded as follow-ups.

[2026-11-21T13:17:22Z · bob-cli-oj.1] CLOSED-BEAD LAUNCH: agent bob-cli-oj.1 launched against this closed bead; status left closed.
Launch submitted 2026-11-21T13:16:31.634870Z; run 20261121081632.
Prior close: 2026-11-21T13:12:36Z · done.

[2026-11-21T13:19:55Z · bob-cli-oj.1] Recovery: prior run closed the phase before its finalizer refused local-only commit 726f9a5c653164a6219b7bdd6eef5a9f2715b55f in workspace 13. Fetched origin/master lacks nav-grammar. Recovering the existing implementation instead of reimplementing it.

## Dependencies

- **Blocks:** [bob-cli-oj.5](bob-cli-oj.5.md) ◐ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-oj.6](bob-cli-oj.6.md) ◐ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-oj.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.1/README.md) | [bob-cli-oj.1](bob-cli-oj.1.md) | 0 |
