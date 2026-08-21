<div align="center">
  <br />
  <a href="https://www.eonik.ai">
    <img src="https://www.eonik.ai/logo.svg" alt="eonik" width="120" />
  </a>
  <h1 align="center">eonik MCP Companion · Agent Skill</h1>
  <p align="center">
    <strong>How Claude should think when it has eonik's brand-brain in its hands</strong>
  </p>
  <p align="center">
    <a href="https://www.eonik.ai">Website</a> •
    <a href="https://github.com/eonik-ai/eonik-mcp">eonik-mcp</a> •
    <a href="https://www.eonik.ai/mcp">MCP essay</a>
  </p>
</div>

---

## What this is

An **[Agent Skill](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview)** for hosts that load filesystem skills. It is **not** the MCP server.

- **[eonik-mcp](https://github.com/eonik-ai/eonik-mcp)** is the stdio bridge to `https://api.eonik.ai` (`GET /api/tools/manifest` + `POST /api/tools/dispatch`).
- **This skill** is the playbook: ground in brand + ledger, use the watch archive, deconstruct references, remember verbatim, author briefs from grounding. **Never launch or move budget.**

eonik is a Mac app for making ads. MCP does not replace the app. Agents read and draft; **you approve every cut.**

## Capability map (live `command_tools.py`)

Not Analyze → Ideate → Produce → Deploy. Deploy-to-Meta **does not exist**.

| Station | Tools (representative) | Behavior |
|---------|------------------------|----------|
| **Gather** | `get_brand_briefing`, `get_brand_context`, `get_context_ledger`, `get_account_condition`, `get_recent_slates`, `get_account_memory`, `list_my_ads`, competitor + swipe reads | Facts only |
| **Research** | `deconstruct_ad`, `get_ad_deconstruction`, `get_competitor_patterns`, `get_competitor_timeline`, `get_craft_playbook`, `probe_asset_duration` | eonik's labor; you reason |
| **Remember** | `save_context_note`, `save_brand_truth`, `save_plan`, `remember`, `recall` | Verbatim; reviewable in Brand |
| **Produce** | `get_brief_grounding` (prefer); `generate_creative_brief` (deprecated) | Agent authors from receipts |

Retired forever: `launch_ad_run`, `run_budget_audit`, `create_ad_creation_run`, `compile_seed_spec`, hypothesis / budget-leak tools.

## Install

Clone into the host's skills directory, or zip with **`SKILL.md` at the archive root**.

MCP connection is separate — install [eonik-mcp](https://github.com/eonik-ai/eonik-mcp) or the API SSE connector. This skill does not authenticate.

## Layout

```
eonik-mcp-skill/
├── SKILL.md
├── reference.md
├── README.md
└── LICENSE
```

## License

MIT-0 — see [LICENSE](LICENSE).
