# MCP

The agent connects to **MCP** (Model Context Protocol) servers to reach external tools and data sources — your email, your code host, your design tool, your data warehouse, your ticketing system.

## What MCP gives the agent

- **Tools** — functions the agent can call (read, write, search, act) against an external system
- **Resources** — content the agent can read (a doc, a ticket, a row in a table)
- **Prompts** — pre-defined operations a server exposes for the agent to use directly

## Installed servers

A library of connected servers. Each has its own connection state, scope, and approval rules. Common starting set:
- Gmail, Google Calendar (feeds the [calendar](../entities/calendar.md)), Google Drive
- GitHub, Linear, Jira
- Slack, Notion, Figma

You can add custom servers — local or remote — including ones you build yourself.

## How the agent uses them

- The agent picks an MCP tool the way it picks a [skill](skills.md) — implicitly based on what you're asking, or you can name the tool directly.
- Read calls against trusted servers run freely.
- Writes and external sends always pass through the [approval workflow](approval.md).
- Results stream into chat and can be saved into the workspace: a Linear ticket becomes a linked task; an email thread becomes a note; a Figma file becomes a reference on a doc.

## Configuration

- Per-server — enabled / disabled, credentials, scope, approval tier override.
- Per-tool — rename, hide, or pin so it's easy to invoke.
- Per-resource — pull live or cache; some resources are sensitive enough to never cache.

## What MCP is not

- Not a sync layer — MCP is on-demand read/write, not continuous mirroring. Exception: a specific server may offer sync (Google Calendar does, into the [calendar](../entities/calendar.md)).
- Not a replacement for the [files](../entities/files.md) tree or the workspace graph — external content lives on the other side; the agent fetches what it needs and saves what's worth keeping.
