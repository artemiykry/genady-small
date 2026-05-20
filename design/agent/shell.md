# Shell

The agent can execute shell commands on your machine. Shell is the agent's bridge to anything outside the workspace — scripts you keep around, CLIs, file operations, ad-hoc data work.

## What it's for

- Running scripts you keep around — the backup, the report generator, the cleanup
- Pulling from CLIs (`gh`, `kubectl`, `jq` pipelines, anything in your `PATH`)
- File operations the agent can't do directly through the [files](../entities/files.md) surface
- Anything you'd otherwise do in a terminal yourself

## How it behaves

- Every command is shown to you before it runs.
- Output streams back into the chat as the command runs.
- Long-running commands can be backgrounded; you're notified when they finish.
- Exit codes and errors are surfaced clearly.
- Each command runs fresh — no persistent shell state between commands (no implicit `cd`, no carried environment variables beyond what you configure).

## What it isn't

- Not unrestricted — see [approval workflow](approval.md) for what runs freely and what waits.
- Not the agent's default — it reaches for shell only when that's the cleanest path. Most actions go through the workspace directly or via an [MCP](mcp.md) tool.
- Not a terminal emulator — there's no interactive prompt; commands are one-shots.

## Configuration

- A working directory the agent operates from by default (typically your [files](../entities/files.md) root).
- A list of commands always allowed without confirmation (e.g. `ls`, `git status`).
- A list of commands always denied.
- Environment variables and PATH adjustments the agent inherits.
