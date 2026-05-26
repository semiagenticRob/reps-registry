# reps-registry

Central registry for the **100 Reps Project**. This repo is a one-way mirror — it is written to by `semiagenticRob/multi-agent-orchestrator`'s `registry-sync-agent` at every gate approval. Don't edit `reps/` by hand.

## Structure

```
reps/
  <rep-id>/
    status.yml
    scope/scope.md
    design/design.md
    build/build-log.md
    test/test-report.md
    deploy/deploy-manifest.md
    retro.md
    ...
index.yml         # portfolio summary — one entry per rep
```

## Reading the registry

- `index.yml` — fastest way to see all reps and their current phase.
- The git log itself is an audit trail: each commit is `sync: rep-{id} {phase} {result}`.

## Updating

You don't, directly. Run the orchestrator on a rep and approve gates — sync happens automatically.

Manual fixups (rare) should go via PR with a clear "what got out of sync and why" in the description.
