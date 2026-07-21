# Unl

**Stop re-explaining yourself to your AI.**

Every new session starts from zero — the decisions you made yesterday, the reasoning
behind them, the approach you already ruled out. Gone, so you type it all again. Unl
ends that.

Connect once, and Unl holds what you've settled — your decisions, the why behind them,
the threads you want to come back to — and serves them back at the exact turn they bear
on, unprompted. Your AI picks up where your thinking left off.

Tuned to Claude, Claude Code, Cursor and ChatGPT, and extending across the AI ecosystem
— model and platform agnostic: sign in once, and every surface you attach reads the same
workspace. Change the model; keep your world.

Unl never writes anything without your word, and never reaches into your model or your
files — a boundary that's enforced, not promised. It holds what you give it, and hands it
back when it matters.

## Connect

One URL, every surface:

```
https://api.unlimitless.ai/mcp
```

Add it wherever your tool takes an MCP server. You'll be asked to sign in; that sign-in
*is* the connection. Nothing to pay at the door, and no API key to paste.

### Claude Code

```bash
claude mcp add --transport http unl https://api.unlimitless.ai/mcp
```

### Cursor

Add to `~/.cursor/mcp.json` (global) or `.cursor/mcp.json` (per project):

```json
{ "mcpServers": { "unl": { "url": "https://api.unlimitless.ai/mcp" } } }
```

### Anything else

Any client that speaks MCP over streamable HTTP works with the same URL.

## What this repo is

The connector's manifests and listing packaging — not the product.

| path | what it is |
|---|---|
| `server.json` | MCP Registry entry |
| `mcp.json` | server config, as a client expects it |
| `.claude-plugin/plugin.json` | Claude plugin manifest |
| `.claude-plugin/marketplace.json` | self-hosted Claude Code marketplace |
| `.cursor-plugin/plugin.json` | Cursor plugin manifest |

Unl's behaviour is served from the connection, not shipped here — so it's the same on
every surface, and it improves without you reinstalling anything.

## Trust

- Nothing is written without your word.
- Your reasoning stays yours — Unl holds what you give it and never reaches into your
  model, your files, or your other tools.
- Disconnect whenever you like, from the portal.

## Support

[unlimitless.ai](https://unlimitless.ai) · hello@unlimitless.ai ·
[privacy](https://unlimitless.ai/privacy) · [terms](https://unlimitless.ai/terms)

## Licence

MIT — see [LICENSE](./LICENSE).
