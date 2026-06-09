# GitHub Copilot Integration Validation

This document records validation for the GitHub Copilot plugin metadata and session-start bootstrap integration.

## Local hook smoke test

Command:

```bash
cd /tmp/workspace/vagwada/superpowers
COPILOT_CLI=1 hooks/run-hook.cmd session-start
```

Expected result:

- Output is valid JSON.
- Output uses the Copilot-compatible top-level `additionalContext` field.
- The injected context includes the `using-superpowers` bootstrap content.

Observed result:

- Pending: run after implementation.

## Clean-session acceptance test

Required prompt:

```text
Let's make a react todo list
```

Required behavior:

- A clean GitHub Copilot session loads the Superpowers bootstrap at session start.
- The `brainstorming` skill auto-triggers before any code is written.

Transcript:

```text
Pending: this must be captured from a real clean GitHub Copilot session with the plugin installed.
```
