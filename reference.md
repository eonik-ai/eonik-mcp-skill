# eonik MCP — tool reference

Production MCP base path (typical): mounted at `/mcp` on the eonik API host. Clients discover tools via MCP `tools/list`; this file mirrors current server intent for agents.

## Read-oriented tools (`readOnlyHint: true`)

| Tool | Role |
|------|------|
| `run_budget_audit` | Budget leaks, burn-without-signal, creative decay. Params: `days` (default 30), optional `account_id`. |
| `get_creative_autopsy` | Creative Command Center–style report. Params: `days`. |
| `get_brand_context` | Brand, audience, competitor intelligence snapshot. |
| `search_ad_library` | Global Meta Ad Library search. Filters: `industry`, `hook_type`, `creative_style`, `brand_name`. |
| `discover_trends` | Trends / formats / audio cues. Params: `query`, `platform` (default `meta`). |
| `get_insights_feed` | Prioritized creative insights from genome performance. Params: `platform`, `days`. |
| `get_experimentation_gaps` | What genome combinations to test next. Params: `platform`. |

## Mutating tools (`readOnlyHint: false`)

Call only after explicit user approval.

| Tool | Role |
|------|------|
| `create_ad_creation_run` | Start ad video orchestration. Params: `brand`, optional `product`. |
| `compile_seed_spec` | Build seed spec from approved brief. Params: `run_id`, `target_market` (default `India`). |
| `launch_ad_run` | Mark launched toward Meta. Params: `run_id`, `experiment_id`, optional `meta_adset_id`. |

## Authentication

The MCP server validates `Authorization: Bearer` (OAuth JWT from eonik’s MCP OAuth flow) or `X-API-Key` depending on client configuration. Agents do not embed secrets in skill text—connection is established by the host product (Claude, Claude Code, etc.).
