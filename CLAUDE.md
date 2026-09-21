@AGENTS.md

# Travel Hacking Toolkit - Claude Code adapter

The imported `AGENTS.md` is the shared instruction body; this file maps Claude Code tools and mechanisms only.

## Tool mapping

The MCP servers named in `AGENTS.md` "Tools at Your Disposal" are configured in `.mcp.json` and reach Claude Code under these identifiers:

| Server (AGENTS.md name) | Claude Code tools |
|---|---|
| Skiplagged | `mcp__skiplagged__*` |
| Kiwi.com | `mcp__kiwi__*` |
| Trivago | `mcp__trivago__*` |
| Ferryhopper | `mcp__ferryhopper__*` |
| Airbnb | `mcp__airbnb__*` |
| LiteAPI | `mcp__liteapi__*` |

Call them directly; they need no setup beyond the keys described in `AGENTS.md` "API Keys".

## Skills

`.claude/skills` is a symlink to the repository's `skills/` directory, so every skill listed in `AGENTS.md` is discoverable through the Skill tool under its bare name (for example `compare-flights`, `seats-aero`, `southwest`).

## Personal notes

Keep uncommitted personal instructions in `CLAUDE.local.md` (gitignored); Claude Code loads it after this file.
