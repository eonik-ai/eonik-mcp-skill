# Connect eonik

The skill assumes the host already has eonik's tools. Auth is the host's connection; nothing here
stores a key. Keep the eonik app open on the Mac that holds the files.

## Remote (Claude, ChatGPT, VS Code, Cursor, Claude Code)

Add the connector `https://api.eonik.ai/mcp`, sign in with your eonik account and choose the brand
the connection is about. Then ask: "Where are we?"

## Local hosts (Claude Desktop config file, Codex, Gemini CLI)

1. Create an API key in eonik (Settings, API keys).
2. Run `npx -y eonik-mcp@5.0.0` with `EONIK_API_KEY`, and `EONIK_BRAND_ID` if you have more than
   one brand (eonik never guesses which client's work you mean).
3. Ask: "Where are we?"

## Never

The assistant never launches, pauses or spends, never predicts how an ad will perform, and never
makes a choice that is yours.
