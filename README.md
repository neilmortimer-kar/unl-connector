# Unlimitless connector

> **DRAFT** — all user-facing copy in this repo is draft, pending a wording pass.

Connect once, and carry the same context everywhere you work.

Unl holds what you have settled — decisions, the reasoning behind them, the things
you want to come back to — and serves them back on the turn they bear on. No
re-explaining yourself at the start of every chat, and no copying context between
tools by hand.

It works the same way in Claude, Claude Code, Cursor and ChatGPT, because the
connection is the account: sign in once and every surface you attach reads the same
workspace.

## Connect

One URL, every surface:

```
https://api.unlimitless.ai/mcp
```

Add it wherever your tool takes an MCP server. You will be asked to sign in; that
sign-in *is* the connection. There is nothing to pay for at the door and no API key
to paste.

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

The connector's manifests and listing metadata — the packaging, not the product.

| path | what it is |
|---|---|
| `server.json` | MCP Registry entry |
| `mcp.json` | server config, as a client expects it |
| `.claude-plugin/plugin.json` | Claude plugin manifest |
| `.claude-plugin/marketplace.json` | self-hosted Claude Code marketplace |
| `.cursor-plugin/plugin.json` | Cursor plugin manifest |
| `listings/` | draft listing copy per store |
| `checklists/` | submission checklists per store |

The connector's behaviour is served from the connection, not shipped here — so it is
the same on every surface, and it improves without you reinstalling anything.

## Trust

- Nothing is written without your say-so.
- Your reasoning stays yours — unl holds what you give it and never reaches into
  your model, your files, or your other tools.
- Disconnect whenever you like, from the portal.

## Support

[unlimitless.ai](https://unlimitless.ai) · hello@unlimitless.ai ·
[privacy](https://unlimitless.ai/privacy) · [terms](https://unlimitless.ai/terms)

## Licence

MIT — see [LICENSE](./LICENSE).
