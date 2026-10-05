# OpenOrc Runtime Test Fixture

A deliberately minimal public Git repository used to qualify OpenOrc-managed agent runtime behavior.

## Purpose

This repository exists as a stable, low-noise target for runtime qualification such as:

- anonymous clone and fetch;
- separate Producer and Reviewer working contexts;
- local filesystem mutation without cross-session leakage;
- checkout and preparation of an exact committed review subject;
- repository-root `AGENTS.md` discovery by an agent runtime;
- reconnect and reconciliation experiments that need a real Git working tree.

## Constraints

- Keep this repository intentionally tiny and dependency-free.
- Do not add application code, CI, language toolchains, credentials, secrets, or general repository-specific agent guidance.
- The root `AGENTS.md` is the deliberate exception: it contains one deterministic probe instruction used only to qualify ordinary repository-instruction discovery.
- Qualification may freely mutate disposable local clones. Ordinary R-series qualification should not require pushing those mutations back here.
- When an experiment needs an exact committed subject, record the Git commit SHA used by that experiment rather than relying on branch position.

The repository is a test fixture, not an OpenOrc product component.
