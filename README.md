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
| `plugin.json`, `mcp.json` | the Agent Plugins 1.0 package (one folder, every host that reads the open format) |
| `skills/unl/SKILL.md` | the Unl agent itself, its jobs and rules, as an Agent Skill |
| `.mcp.json` | server config for the Claude and Cursor manifests |
| `.claude-plugin/plugin.json` | Claude plugin manifest |
| `.claude-plugin/marketplace.json` | self-hosted Claude Code marketplace |
| `.cursor-plugin/plugin.json` | Cursor plugin manifest |
| `assets/logo.png` | the Unl mark |

Unl's behaviour is served from the connection, not shipped here, so it's the same on
every surface, and it improves without you reinstalling anything. The skill only tells
the host's own model how to work as Unl, so the agent runs on the AI you already use.

## Related

- [Unlimitless-Inc/unl](https://github.com/Unlimitless-Inc/unl), the main repository
- [`@unlimitless/ai-sdk`](https://www.npmjs.com/package/@unlimitless/ai-sdk) on npm

## What this plugin connects to

- **One remote MCP server, `https://api.unlimitless.ai/mcp`**, run by Unlimitless. It is the
  only place the plugin sends anything. Nothing runs on your machine: no scripts, no hooks,
  no packages to install.
- **What your AI sends it:** the message Unl is asked about, so it can serve the decisions
  that bear on it, and whatever you ask it to keep. The messages your AI sends are kept in
  your own workspace so you can see what it asked, and you can clear them at any time
  ("forget what I sent Unl today").
- **Sign-in:** OAuth, the first time your AI connects. No key is stored in this plugin.
- **Your own tools:** if you connect one of your tools to Unl (analytics, error tracking and
  the like), Unl reads it only when your AI asks, with the key you gave it. Changes go
  through a separate write tool, and anything that deletes or overwrites is shown back
  first and runs only once it is confirmed.

Privacy policy: [unlimitless.ai/privacy](https://unlimitless.ai/privacy).

## Trust

- Nothing is written without your word.
- Your reasoning stays yours. Unl holds what you give it and never reaches into your
  model or your files. It reads a tool of yours only after you connect it, and only when
  your AI asks.
- Disconnect whenever you like, from the portal.

## Support

[unlimitless.ai](https://unlimitless.ai) · hello@unlimitless.ai ·
[privacy](https://unlimitless.ai/privacy) · [terms](https://unlimitless.ai/terms)

## Licence

MIT, see [LICENSE](./LICENSE).
