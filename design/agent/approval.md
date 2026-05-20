# Approval workflow

The agent's actions fall into tiers. Some happen freely, some confirm once, some always ask. You set the line.

## Tiers

### Auto-execute

The agent does these without asking; everything is logged and reversible.
- Read anything in the workspace
- Search, summarize, surface, recommend
- Create *draft* entities (notes, draft tasks, draft meeting agendas) clearly marked as drafts
- Apply suggested links between entities
- Read-only [MCP](mcp.md) calls on trusted servers

### Confirm once

The agent shows the exact action and waits for one keystroke.
- Edit existing entities (rewrite a doc, change a task's due, edit a meeting note)
- Promote a draft to a real entity
- Run a [shell](shell.md) command not on the always-allowed list
- Invoke an [MCP](mcp.md) tool that writes

### Always ask

The agent asks every time, even if you previously approved similar.
- Send anything externally — email, message, calendar invite to other people
- Delete entities permanently
- Modify a locked [memory](memory.md) entry
- Bulk operations across many entities at once
- Anything touching credentials or auth state

## How approval shows up

- A clear "do this?" prompt with the action and the affected entities.
- One keystroke to approve, edit, or deny.
- **Approve-and-remember** for actions you trust unconditionally — moves that action to a lower tier.
- **Bulk approve** for a batch of actions the agent intends as a group.

## What you can configure

- Per-tier defaults — move specific actions between tiers.
- Per-[skill](skills.md) overrides — a trusted skill can run with fewer prompts.
- Per-[MCP](mcp.md) server overrides — a less-trusted server can be set to "always ask."
- Quiet hours — during focus time, the agent holds non-urgent prompts for batch review.

## What cannot be bypassed

- External actions (email, message, invite to others) always require explicit consent per action.
- Permanent deletion always confirms.
- Locked memory entries always require unlock first.
