<div align="center">
  <a href="https://www.eonik.ai">
    <img src="https://www.eonik.ai/logo.svg" alt="eonik" width="160" />
  </a>
  <h1>eonik</h1>
  <p><strong>Finished, on-brand ads without the busywork.</strong></p>
  <p>Your designer makes the master. eonik makes every size your media plan asks for, on-brand, in the eonik app on your Mac. This plugin teaches your assistant to ask eonik for it.</p>
  <p>
    <a href="https://www.eonik.ai">Website</a> ·
    <a href="https://www.eonik.ai/download">Download for Mac</a> ·
    <a href="https://www.eonik.ai/mcp">Connect an assistant</a>
  </p>
  <p>
    <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT--0-18181B?style=flat-square" alt="MIT-0 license" /></a>
  </p>
  <p>
    <strong>English</strong> ·
    <a href="docs/readme/README.es.md">Español</a> ·
    <a href="docs/readme/README.pt-BR.md">Português</a> ·
    <a href="docs/readme/README.fr.md">Français</a> ·
    <a href="docs/readme/README.hi.md">हिन्दी</a> ·
    <a href="docs/readme/README.zh-CN.md">简体中文</a> ·
    <a href="docs/readme/README.ja.md">日本語</a> ·
    <a href="docs/readme/README.ko.md">한국어</a>
  </p>
</div>

---

eonik makes a brand's **adapts**: every size a media plan asks for, from the designer's master,
with the brand's fonts, rules and layout kept the same way on every size, then checked, sent for
approval and delivered. The work runs in the **eonik app on your Mac**
([download](https://www.eonik.ai/download)), where your files and fonts are.

This plugin is the eonik connector plus a skill that teaches an assistant (Claude, Claude Code,
Cursor, Codex, Gemini CLI) how to work with it: start with where things stand, hand the work to
eonik in the person's own words, never edit their images itself, and never claim a choice that is
theirs. See [SKILL.md](skills/eonik/SKILL.md) and the tools in [reference.md](reference.md).

## Install

**Claude Code:** `/plugin install` this repository. Its `.mcp.json` connects to
`https://api.eonik.ai/mcp`; sign in with your eonik account and choose the brand when asked.

**Claude (Team, Enterprise):** an Owner adds the connector `https://api.eonik.ai/mcp` in
Organization settings, Connectors, and can deploy this skill to the organization.

**Cursor and Agent Plugins hosts:** install from the marketplace, or load this repository; its
`mcp.json` connects to the same server through the host's sign-in.

**Gemini CLI:** `gemini extensions install https://github.com/eonik-ai/eonik-mcp-skill.git`, with
an eonik API key and the brand's id.

Keep eonik open on your Mac while you work. Nothing is made, changed or sent until you say so.

## Also

| | |
|---|---|
| Download for Mac | [eonik.ai/download](https://www.eonik.ai/download) · editor free · macOS 15+ · Apple silicon |
| Connect an assistant | [eonik.ai/mcp](https://www.eonik.ai/mcp) |
| Homebrew | [homebrew-tap](https://github.com/eonik-ai/homebrew-tap) |
| Save ads you see | [Chrome extension](https://chromewebstore.google.com/detail/eonik/ikjbopcpohlogfbccbpcoglefjlbdcie) |

## License

MIT-0 — see [LICENSE](LICENSE).
