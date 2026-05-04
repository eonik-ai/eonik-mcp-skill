# eonik MCP companion (Agent Skill)

**Agent Skill** that teaches Claude how to use the **[eonik](https://eonik.ai) remote MCP server** responsibly: Meta Ads audits, creative intelligence, Ad Library research, trends, and gated launch workflows.

Pair this repository with the **eonik MCP server** submission (same directory product). It does **not** replace the MCP connection—it adds procedural guidance so agents pick the right tools and confirm destructive actions.

## Repository layout

| File | Purpose |
|------|---------|
| `SKILL.md` | Anthropic Agent Skill entrypoint (YAML metadata + instructions) |
| `reference.md` | Tool catalog and parameters (progressive disclosure) |

## Install (Claude Code / filesystem Skills)

Clone into your Skills directory (see [Claude Code Skills](https://code.claude.com/docs/en/skills)) or unpack beside other skills:

```bash
git clone https://github.com/eonik-ai/eonik-mcp-skill.git
```

For **Claude.ai** or **API**, zip the folder (with `SKILL.md` at the root of the archive) and upload per product docs.

## MCP connection

Connect the **eonik MCP** SSE endpoint from your client using your eonik API key or OAuth flow documented on the server. This skill assumes those tools appear in the agent’s MCP tool list.

## Directory submission (copy/paste)

**Skill Name**

```text
eonik Marketing & Ads MCP Companion
```

**Skill Description**

```text
Teaches Claude to use the eonik MCP server for Meta Ads budgets, creative autopsy, insights, experimentation gaps, Ad Library search, and trends—while requiring explicit confirmation before any ad creation or Meta launch workflows.
```

**GitHub URL**

After creating the public repository, use:

```text
https://github.com/eonik-ai/eonik-mcp-skill
```

(Replace `eonik-ai` / repo name with your org and chosen slug.)

**Extra Information**

```text
Companion skill for the eonik remote MCP server (SSE). Read-heavy workflows are default; mutating tools (create run, compile seed spec, launch ad) are gated in SKILL.md. Optional reference.md lists tool names aligned with server registration. MIT licensed; no secrets in-repo—auth is via the client MCP connection.
```

**Related Plugins**

```text
None planned—cross-promote the separate MCP server listing only unless you publish a Claude Code plugin bundle later.
```

## License

MIT-0 (see [LICENSE](LICENSE)).

## Support

Product: [eonik.ai](https://eonik.ai)
