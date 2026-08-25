# Connect eonik

The skill assumes the host already has eonik tools. Auth is the host connection. Nothing here stores keys.

## Cursor / Agent Plugins hosts (remote OAuth)

1. Install the eonik Agent Plugin from the marketplace or load this repository locally.
2. The plugin’s `mcp.json` connects to `https://api.eonik.ai/mcp`.
3. Complete the OAuth flow opened by the host, confirm eonik tools appear, then ask: “Orient me on this brand.”

## Claude Code / Grok Build (stdio)

1. Create an API key in eonik workspace settings.
2. The plugin’s `.mcp.json` runs `npx -y eonik-mcp@2.0.0`. Set `EONIK_API_KEY` in the host env (and optional `EONIK_API_URL`, `EONIK_BRAND_ID`).
3. Confirm tools appear, then ask: “Orient me on this brand.”

## Gemini CLI

Repo root has `gemini-extension.json`. After the GitHub topic `gemini-cli-extension` is on this public repo, the gallery crawls daily. Install:

```
gemini extensions install https://github.com/eonik-ai/eonik-mcp-skill.git
```

Set `EONIK_API_KEY` when prompted. Not gemini.google.com.

## Claude.ai / ChatGPT / Perplexity (remote)

Add connector URL `https://api.eonik.ai/mcp` and complete OAuth. Do not paste an API key into chat.

## Never

Do not install a listing that offers `launch_ad_run`, `run_budget_audit`, or spend actions. Those are retired. The assistant reads and drafts. You approve every cut on Mac.
