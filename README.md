<div align="center">
  <br />
  <a href="https://eonik.ai">
    <img src="https://eonik.ai/logo.svg" alt="eonik" width="120" />
  </a>
  <h1 align="center">eonik MCP Companion · Agent Skill</h1>
  <p align="center">
    <strong>How Claude should think when it has eonik in its hands</strong>
  </p>
  <p align="center">
    <a href="https://eonik.ai">Website</a> •
    <a href="https://github.com/eonik-ai/eonik-mcp">eonik-mcp (stdio server)</a> •
    <a href="https://api.eonik.ai/docs">API Docs</a>
  </p>
</div>

---

## What this is

This repository is an **[Agent Skill](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview)** for products that support filesystem skills (Claude Code, Claude API with skills, Claude.ai custom skills, and similar). It is **not** the MCP server itself.

- **[eonik-mcp](https://github.com/eonik-ai/eonik-mcp)** is the stdio MCP bridge (`npx eonik-mcp@latest`) that talks to `https://api.eonik.ai`.
- **This skill** is the playbook: when to call which tool, how to ground answers in `get_brand_context`, and when to stop and ask the human before `create_ad_creation_run`, `compile_seed_spec`, or `launch_ad_run`.

Together, they turn a generic model into a **disciplined** marketing co-pilot: same tools, better judgment.

---

## Why it exists

Raw tool lists do not teach an agent to:

- Load **brand and competitor context** before giving strategy.
- Prefer **read-only** audits and insights before any **write** to Meta or eonik.
- Summarize in **plain language** instead of dumping JSON.

`SKILL.md` encodes those habits. `reference.md` is optional deep detail—loaded only when needed ([progressive disclosure](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview)).

---

## Capability map (aligned with eonik MCP)

The same four phases as the [eonik MCP server](https://github.com/eonik-ai/eonik-mcp) README:

| Phase | Tools | Skill behavior |
|--------|--------|----------------|
| **Analyze** | `run_budget_audit`, `get_creative_autopsy` | Run when the user wants account health, leaks, or creative Command Center–style diagnosis. |
| **Ideate** | `discover_trends`, `get_brand_context`, `search_ad_library`, `get_insights_feed`, `get_experimentation_gaps` | Start from `get_brand_context` when advice should be on-brand; use filters on Ad Library and trends when relevant. |
| **Produce** | `create_ad_creation_run`, `compile_seed_spec` | Only after **explicit** user confirmation; treat as creating or updating orchestration state in eonik. |
| **Deploy** | `launch_ad_run` | Only after **explicit** confirmation; affects Meta. |

Neural mapping, guardrails, and tenant isolation stay in the **eonik cloud**—this repo is instructions only.

---

## Install the skill

### Claude Code (filesystem)

Clone into your skills directory (see [Claude Code · Skills](https://code.claude.com/docs/en/skills)):

```bash
git clone https://github.com/eonik-ai/eonik-mcp-skill.git
```

### Claude.ai or API (upload)

Zip the repository so **`SKILL.md` is at the root** of the archive, then upload per your plan’s **custom Skills** flow.

### Relationship to MCP

Install **either** the remote SSE connector to `https://api.eonik.ai/mcp/sse` **or** the local **[eonik-mcp](https://github.com/eonik-ai/eonik-mcp)** stdio server—the skill does not replace authentication; it assumes MCP tools are already available to the agent.

---

## Repository layout

```
eonik-mcp-skill/
├── SKILL.md       # Metadata + agent instructions (required)
├── reference.md   # Tool parameters and lookup table
├── README.md      # This file
└── LICENSE        # MIT-0
```

---

## Security & privacy

- No API keys, OAuth tokens, or customer data belong in this repo.
- All execution and isolation are enforced by **api.eonik.ai** when tools run.
- Teach agents to treat mutating tools like production actions—**confirm first**.

---

## License

MIT-0 — see [LICENSE](LICENSE).

---

*Built for the same loop as [eonik-mcp](https://github.com/eonik-ai/eonik-mcp): analyze → ideate → produce → deploy — with guardrails in the skill layer.*
