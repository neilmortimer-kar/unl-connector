# Unl

Unl is the product by Unlimitless ([unlimitless.ai](https://unlimitless.ai)).

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE)
[![npm](https://img.shields.io/npm/v/@unlimitless/ai-sdk.svg)](https://www.npmjs.com/package/@unlimitless/ai-sdk)

**Unl, your why agent. The infra agent for your fleet.**

Your other agents do the work; Unl makes sure they work from what you decided, and why.
Connect it once to Claude, ChatGPT, Cursor, Claude Code or any MCP client, and each agent
is served the decisions that bear on its task, with the reason each was made, before it
acts. Free to start.

## Connect

One URL, every surface.

```
https://api.unlimitless.ai/mcp
```

Add it wherever your tool takes an MCP server. You'll be asked to sign in; that sign-in
*is* the connection. Nothing to pay at the door, and no API key to paste.

### Claude Code

As a plugin, from this repo's marketplace:

```
/plugin install unl --marketplace neilmortimer-kar/unl-connector
```

Or as a plain MCP server:

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

## See it work

Clone [Unlimitless-Inc/unl](https://github.com/Unlimitless-Inc/unl) and run the demo.

```bash
node demo/changed-decision.mjs
```

## What this repo is

Unl's manifests and listing packaging. Not the product.

| path | what it is |
|---|---|
| `server.json` | MCP Registry entry |
| `mcp.json`, `.mcp.json` | server config, as a client expects it |
| `.claude-plugin/plugin.json` | Claude plugin manifest |
| `.claude-plugin/marketplace.json` | self-hosted Claude Code marketplace |
| `.cursor-plugin/plugin.json` | Cursor plugin manifest |
| `assets/logo.png` | the Unl mark |

Unl's behaviour is served from the connection, not shipped here, so it's the same on
every surface, and it improves without you reinstalling anything.

## Related

- [Unlimitless-Inc/unl](https://github.com/Unlimitless-Inc/unl), the main repository
- [`@unlimitless/ai-sdk`](https://www.npmjs.com/package/@unlimitless/ai-sdk) on npm

## Trust

- Nothing is written without your word.
- Your reasoning stays yours. Unl holds what you give it and never reaches into your
  model, your files, or your other tools.
- Disconnect whenever you like, from the portal.

## Support

[unlimitless.ai](https://unlimitless.ai) · hello@unlimitless.ai ·
[privacy](https://unlimitless.ai/privacy) · [terms](https://unlimitless.ai/terms)

## Licence

MIT, see [LICENSE](./LICENSE).
