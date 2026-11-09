# Connect eonik

The skill assumes the host already has eonik's tools. Auth is the host's connection; nothing here
stores a key. Making and resizing need the eonik app open on the Mac that holds the files; setting
up, competitors and the brand's own ads work without it.

## One command, every assistant on this computer

`npx eonik-mcp init` adds eonik to Claude Code, VS Code, Cursor and Codex, and says the steps for
Claude Desktop. Each assistant signs you in to eonik the first time.

## Remote (Claude, ChatGPT, VS Code, Cursor, Claude Code)

Add the connector `https://api.eonik.ai/mcp` and sign in with your eonik account, or make one.
Then ask: "Set eonik up for my brand." or "Where are we?"

## Local hosts (Claude Desktop config file, Gemini CLI)

1. Create an API key in eonik (Settings, API keys).
2. Run `npx -y eonik-mcp@5.0.0` with `EONIK_API_KEY`. `EONIK_BRAND_ID` is optional: with more than
   one brand you choose in the conversation, and eonik never guesses which client's work you mean.
3. Ask: "Where are we?"

## Never

The assistant never launches, pauses or spends on an ad, never buys anything, never predicts how an
ad will perform, and never makes a choice that is yours.
