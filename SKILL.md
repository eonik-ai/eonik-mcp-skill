---
name: eonik-mcp-companion
description: >-
  Guides effective use of the eonik MCP server for Meta Ads creative
  intelligence — budget audits, creative autopsy, competitor research,
  experimentation planning, and ad launching. Activates when eonik is connected
  or user asks about ad performance.
---

# eonik MCP companion

Use this skill whenever **eonik MCP tools** are in scope. The server authenticates the user (API key or OAuth); tools run against **their** connected Meta workspace and eonik data.

## Principles

1. **Ground first:** Call `get_brand_context` before giving strategic or creative advice so recommendations match their audience, positioning, and saved intelligence.
2. **Read before write:** Prefer audit and insight tools. Mutating tools (`create_ad_creation_run`, `compile_seed_spec`, `launch_ad_run`) require **explicit user confirmation** before invocation.
3. **One question at a time for synthesis:** Pull raw data with read tools, then summarize in plain language with clear next actions—do not dump opaque JSON.
4. **Account scope:** `run_budget_audit` accepts optional `account_id`; if omitted, the server resolves the user’s default Meta ad account when available.

## Read-focused workflows

| Goal | Typical tool sequence |
|------|------------------------|
| Health check on spend and leaks | `run_budget_audit` → summarize leaks / decay signals |
| Creative performance story | `get_creative_autopsy` → `get_insights_feed` |
| What to test next | `get_experimentation_gaps` (optionally after `get_brand_context`) |
| Competitor creative references | `search_ad_library` with industry / hook / style filters |
| Cultural or format trends | `discover_trends` with `query` and `platform` |

## Mutating workflows (user must confirm)

1. **Create an orchestrated video run:** `create_ad_creation_run` — capture returned `id` / stage.
2. **Compile seed spec after brief approval:** `compile_seed_spec` with `run_id` and optional `target_market`.
3. **Launch to Meta:** `launch_ad_run` with `run_id`, `experiment_id`, and optional `meta_adset_id`.

State clearly what will change in Meta or eonik (new run, spec compile, or launch) **before** calling these tools.

## Response quality

- Lead with **3–7 bullet insights**, then optional detail.
- Cite **tool names** only when useful for transparency; avoid raw field-by-field JSON unless the user asks.
- If a tool returns `error`, relay it faithfully and suggest configuration fixes (e.g. Meta not connected, missing run).

## Further detail

For a concise catalog of tools, parameters, and hints, see [reference.md](reference.md).
