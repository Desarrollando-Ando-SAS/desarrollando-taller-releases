---
name: computer-use
description: >-
  Drives the GUI of a visible local app window through `dsa computer`: accessibility
  tree, clicks, typing, menus, dialogs, and screenshots in native apps and external
  browser windows (Chrome, Edge, Safari) or webviews. Prefer a programmatic path
  (shell, filesystem, git, HTTP, existing CLIs) whenever it can complete the task.
  Use only when a visible window needs GUI control those cannot reach. Do not use
  for DesarrollAndo's embedded browser (`dsa-cli`).
---

# Computer Use

This discovery stub loads the version-matched guide from the DesarrollAndo executable used for this session.

## Resolve the CLI for this session

Choose the executable once and reuse it for every later command:

- If the `ORCA_CLI_COMMAND` environment variable is set, use its value. DesarrollAndo exports this
  for managed WSL sessions.
- Otherwise, in a dev checkout whose session exposes `ORCA_DEV_REPO_ROOT`, use `orca-dev`.
- Otherwise, use `dsa`.

Below, `DSA` is a placeholder for the executable you resolved. Substitute it before
running anything; do not create a shell variable or run `DSA` literally. This works the
same way in POSIX shells, PowerShell, and cmd.exe.

If the selected executable cannot run, report its exact error and stop. Do not fall through
to another executable, which could silently target a different DesarrollAndo build.

## Load the version-matched guide before running DesarrollAndo commands

```text
DSA skills get computer-use
```

Prefer `--json`. Use the selected executable's `--help` for commands or flags the guide does
not cover. If a command reports that DesarrollAndo is not running, start it with `DSA open --json`
and retry. If it fails with `runtime_access_denied`, your sandbox blocked the connection:
re-run it with escalated permissions, and do not run `DSA open` or restart DesarrollAndo. If
`skills get` is unknown, explain that updating DesarrollAndo restores the guide; use `--help` for
read-only discovery and do not guess unsupported commands.
