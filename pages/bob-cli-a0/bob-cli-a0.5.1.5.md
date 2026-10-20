# Bead: bob-cli-a0.5.1.5 — Bootstrap the public host and prove publication safety

[Bead Pages](../README.md) / [bob-cli-a0.5.1](bob-cli-a0.5.1.md) / bob-cli-a0.5.1.5

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.5.md) · **Assignee:** `bob-cli-a0.5.1.5` · **Size:** medium
**Created:** 2026-10-19 23:18:37 EDT
**Plan:** [202610/docs\_gated\_publication.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/docs_gated_publication.md)

## Description

launch: add the three README docs links, configure the authorized public host and homepages, run first publish, broken-link drill, normal recovery and weekly checks, and record live URL and provenance evidence.

## Notes

[2026-10-20T05:26:43Z · bob-cli-a0.5.1.5--3] Verification: monitor p00gkv9h54xj ran `just docs-check` to exit 0 on 2026-10-20, including strict Zensical build, published URL checks, offline fragment checks, search smoke, tutorial, media determinism, and documentation tests. The first `just docs-publish` attempt (monitor gq2v1b4t1rve) failed before a workflow run was accepted: GitHub HTTP 422 rejected the reusable `docs-publish.yml` because its five jobs lacked `runs-on`. Added `runs-on: ubuntu-latest` to all five publish jobs and both weekly jobs; the exact updated source passes docs-check. Changes are pending SASE finalization before the first actual publish.

## Dependencies

- **Depends on:** [bob-cli-a0.5.1.4](bob-cli-a0.5.1.4.md) ✓ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.5.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.5.1.5.md) | [bob-cli-a0.5.1.5](bob-cli-a0.5.1.5.md) | 0 |
