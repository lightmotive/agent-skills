---
name: foss-contrib-init
description: Initialize a cloned open-source repository for contributions by symlinking shared Claude Code settings that disable attribution
disable-model-invocation: true
allowed-tools: Bash(mkdir *), Bash(ln *)
---

Set up this repository for open-source contributions:

1. Create the `.claude` directory if it doesn't exist: `mkdir -p .claude`
2. Symlink the shared FOSS settings: `ln -sf ~/.claude/shared/foss-settings.json .claude/settings.local.json`
3. Confirm the symlink was created successfully by checking `ls -la .claude/settings.local.json`

Report what was done. If `.claude/settings.local.json` already exists (and is not already the correct symlink), warn the user before overwriting.
