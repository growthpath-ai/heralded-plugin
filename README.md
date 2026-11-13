# Heralded

See how AI answers talk about your brand, and what to do about it, from Claude or ChatGPT.

Heralded measures how AI assistants such as ChatGPT, Gemini, Perplexity and Google's AI Overviews answer the questions your buyers ask. This plugin connects your assistant to your Heralded account. It can read your Heralded Score and its trend, the questions where you are mentioned or recommended, the competitors AI recommends instead of you, the sources and pages AI cites, how AI describes your brand, and the actions Heralded proposes next. With Full access, it can also run a Heralded Snapshot of any website.

You need a Heralded account. Get one at [heralded.ai](https://heralded.ai).

## What you can ask

| Skill | Ask, for example |
|---|---|
| `visibility-review` | "How visible is my brand in AI answers this week?" |
| `explain-a-change` | "Why did our Heralded Score drop?" |
| `competitor-gaps` | "Who does AI recommend instead of us, and why?" |
| `source-outreach` | "Which sites should we pitch to get mentioned?" |
| `content-opportunities` | "What should we write to show up in AI answers?" |
| `run-snapshot` | "Run a Snapshot of acme.com." |

## Install

In Claude, ChatGPT or Codex, find Heralded in the plugin directory and install it. To install from this repository instead:

- **Claude** (web, desktop and mobile): in claude.ai, open **Customize** > **Plugins** > **Add marketplace** and enter `growthpath-ai/heralded-plugin`.
- **Claude Code:** `claude plugin marketplace add growthpath-ai/heralded-plugin`, then `claude plugin install heralded@heralded`.
- **Codex and the ChatGPT desktop app:** `codex plugin marketplace add growthpath-ai/heralded-plugin`, then `codex plugin add heralded@heralded`.

Then connect Heralded: sign in to Heralded, pick the workspace, and choose **Read only** or **Full access**. [Connect an AI assistant](https://docs.heralded.ai/assistants) has the details.

## What it sends and stores

The plugin runs no code on your computer. It holds instructions (the skills in `skills/`) and the address of Heralded's MCP server, `https://api.heralded.ai/v1/mcp` (`mcp.json`).

When you ask about your brand, your assistant calls that server with the request's parameters, such as a brand's domain or a filter, using the access you granted when you signed in. Heralded answers with your workspace's data: figures, questions, AI answers, competitors, sources, actions, reports and the names of the people on them. Your assistant's provider processes that data under its own terms. The plugin sends nothing anywhere else.

You can see and revoke each connected assistant in Heralded under **Workspace settings** > **Connections**. The [privacy policy](https://heralded.ai/privacy/) covers how Heralded handles your data.

## Support

[docs.heralded.ai/support](https://docs.heralded.ai/support), or email hello@heralded.ai.

## License

MIT
