# Bead: bob-cli-kd.1 — Restart the habit in the vault with no code

[Bead Pages](../README.md) / [bob-cli-kd](README.md) / bob-cli-kd.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1be](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1be.md) · **Assignee:** `bob-cli-kd.1` · **Size:** small
**Created:** 2026-11-11 11:24:16 EST · **Closed:** 2026-11-11 11:34:26 EST
**Plan:** [202611/bank\_daily\_acknowledgment.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_daily_acknowledgment.md)

## Description

bank-restart: create `bank.md` under `cash` with its `bank:` config, the `bank_month` type note, and this month's bank month note in the final template. Capture the daily PRE chore, retire the decaying `^daily-bank-records-again` as superseded, and gate on link and task counts.

## Notes

[2026-11-11T16:34:15Z · bob-cli-kd.1] # bank-restart phase report

Ritual restarts tomorrow (2026-11-12) with today's bob, no code.
Decision applied: accounts = checking (checking-only seed; no card).
Starter categories sanity-checked against 2025 `_habit.md` @BANK rows
(dining = eat/*, groceries = 711/amazon, subscriptions = old_recur,
cash = (w) withdrawals): contract's 12 keys kept as-is, no relabels.
Built-ins (income/refund/transfer/cash) left undeclared.

\## Gates (before -> after)

- Unresolved-link count: 10067 -> 10066. Exactly one resolved
  (`cash.md: [[bank]]`), zero newly unresolved (diffed full sets).
  Script kept: /tmp/bank_baseline_links.py (excludes .bob/,
  _conflicts/, gitignored trees).
- #task occurrences: 4762 -> 4763 (+1 = the chore). Open task lines
  563 -> 563 (+1 chore, -1 cancelled ^daily-bank-records-again).
  Done/cancelled lines 4152 -> 4153. Script: /tmp/bank_baseline_tasks.sh.
- `bob notebooks check`: 37 notebooks, 2 errors, 14 warnings — unchanged.
- `bob records check`: 104 restaurants, 15 podcasts, 23 tv shows,
  10 movies, 0 errors, 0 warnings — unchanged.
- `bob.md ^bank-records` left open ([/]), flagged for Bryan.
- Vault commits (vault-sync carried): `63918afdb` bank.md +
  bank/2026-11.md + bank_month.md; `d10d5aef0`/`fdd265e0a` chore;
  `4aea28db9` cash.md + gtd_daily.md retire.

\## PRE chore (via `bob capture`, not by hand)

- [?] #task #gtd #pre **Acknowledge bank** ... [repeat:: every day when done]
  [created::2026-11-11] [scheduled::2026-11-12] ^acknowledge-bank
  (in gtd_daily.md line 10; task-status hooks placed it)

\## Retire (via bob's own gesture, cancel label)

`@cash:daily-bank-records-again ~gtd_daily:acknowledge-bank|"superseded by"`
=> cash.md ^daily-bank-records-again [?] -> [-] with
[cancelled:: 2026-11-11] and LINKS line:
`[[bob#^bank-records]] • superseded by [[gtd_daily#^acknowledge-bank]]`.

\## Files created, in full

\### bank.md
---
parent: "[[cash]]"
type: "[[area]]"
created: 2026-11-11T11:31:42-05:00
bank:
  accounts:
    checking:
      label: WF Checking
      kind: checking
      start: 2026-11-11
  categories:
    groceries: 🛒 Groceries
    dining: 🍽️ Dining
    coffee: ☕ Coffee
    transit: 🚆 Transit
    car: 🚗 Car
    home: 🏠 Home
    utilities: 💡 Utilities
    dog: 🐶 Dog
    kids: 🧸 Kids
    health: 💊 Health
    shopping: 🛍️ Shopping
    subscriptions: 🔁 Subscriptions
    fun: 🎟️ Fun
    fees: 🧾 Fees
  rules:
    - match: VENMO
      cat: transfer
---

\# 🏦 Bank

Every transaction and deposit in our accounts, acknowledged daily. Each month has one
note under `bank/`. Under each day, type what posted, ticked:
`- [x] $13.71 Smashburger [cat:: dining]`. Use `+$` for money in, `⚑` (or `!!`) for
anything to look into, and `—` (or `--`) for a note. Money tasks like disputes and
cancellations live here too.

\```bob-bank
view: queue
\```

\### bank_month.md
---
parent: "[[type]]"
created: 2026-11-11T11:31:42-05:00
---

Bank month notes hold one month of bank rows under day headings, oldest first. Ticking a row acknowledges it.

Run `bob bank` to see what is waiting; the `bob bank` commands ship with bank-cli.

\### bank/2026-11.md
---
parent: "[[bank]]"
type: "[[bank_month]]"
month: 2026-11
created: 2026-11-11T11:31:42-05:00
---

\# 🏦 November 2026

\```bob-bank
view: month
\```

\## Wed Nov 11
\```

[2026-11-11T16:34:26Z · bob-cli-kd.1] bank-restart done and gated: bank.md (checking-only, start 2026-11-11), bank_month.md, bank/2026-11.md (Wed Nov 11 heading, no rows) created; PRE chore captured via bob capture with repeat daily + scheduled 2026-11-12 (^acknowledge-bank); cash.md ^daily-bank-records-again cancelled via superseded-by relation gesture; bob.md ^bank-records left open. Gates: unresolved links 10067->10066 (only cash [[bank]] resolved, none new); #task +1 total (+1 chore, -1 cancelled); notebooks/records checks unchanged. Full report on bead note.

## Dependencies

- **Blocks:** [bob-cli-kd.7](bob-cli-kd.7.md) ✓ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kd.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.1/README.md) | [bob-cli-kd.1](bob-cli-kd.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:research.49.cdx][1] | Establish initial vault rollout and end-to-end verification state | 1 |
| read-by | [agent:research.49.cld][2] | research: user guide for first-time bank ack and e2e test of bob-cli-kd | 1 |
| read-by | [agent:research.49.gem][3] | Understand phase 1 habit restart | 1 |
| read-by | [agent:research.49.grk][4] | Need closed restart/CLI phases and wrap-up e2e proof so the first-run guide matches shipped work | 1 |
| read-by | [agent:research.49.mus][5] | research kd epic phase scope for user guide | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.cdx/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.cld/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.gem/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.grk/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.mus/README.md

<!-- sase:referenced-by:end -->
