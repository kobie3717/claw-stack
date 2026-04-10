# The Claw Stack 🦀

> **Memory → Evaluation → Credential → Access Control** for AI agents.
> One install command. The whole pipeline.

Most "AI memory" projects stop at *store and recall*. The Claw Stack keeps going:

1. **Memory** — Agents write experiences to SQLite (tiered working/episodic/semantic).
2. **Evaluation** — Dream mode consolidates, detects drift, validates claims against reality.
3. **Credential** — Proven competence is issued as W3C Verifiable Credentials (Ed25519-signed).
4. **Access Control** — Other agents present credentials to read scoped wing/room namespaces.

No other memory library ships the full loop. This one does.

## Install

Add the marketplace to Claude Code once, get both plugins:

```bash
/plugin marketplace add kobie3717/claw-stack
/plugin install ai-iq
/plugin install bot-circus
```

## What's Inside

| Plugin | Role | Repo |
|---|---|---|
| [`ai-iq`](https://github.com/kobie3717/ai-iq) | Memory + credentials | SQLite brain, FSRS decay, W3C VCs, drift detection |
| [`bot-circus`](https://github.com/kobie3717/bot-circus) | Multi-agent orchestrator | Telegram bot swarm with passport-gated memory sharing |

## The Flow

```
Bot Alice works → AI-IQ stores memories → dream mode validates
       ↓
AI-IQ issues Alice a "code:expert" W3C VC (signed, proof-of-work)
       ↓
Bot Bob presents Alice's credential → gains scoped read access
       ↓
Bob answers using Alice's earned knowledge
       ↓
Every access: capability-based, deny-by-default, audit-logged
```

## Why Bundle Them?

Either plugin is useful alone. Together they prove the thesis:

- **AI-IQ alone** — great memory for a single agent.
- **Bot-Circus alone** — great multi-bot orchestrator.
- **Both together** — the first open-source stack where agents *earn* access to each other's knowledge instead of broadcasting or siloing it.

## Standalone Use

Don't want the whole stack? Each plugin runs independently:

```bash
/plugin marketplace add kobie3717/ai-iq        # memory only
/plugin marketplace add kobie3717/bot-circus   # orchestrator only
```

## Author

Built by [Kobus](https://github.com/kobie3717) with Claude Code.

Part of the kobie3717 open-source ecosystem:
- [AI-IQ](https://github.com/kobie3717/ai-iq) — SQLite-backed AI memory
- [Bot-Circus](https://github.com/kobie3717/bot-circus) — Multi-agent orchestrator
- [WaSP](https://github.com/kobie3717/wasp) — WhatsApp Session Protocol
- [baileys-antiban](https://github.com/kobie3717/baileys-antiban) — Anti-ban for Baileys
- [PayBridge](https://www.npmjs.com/package/paybridge) — Unified payments SDK

## License

MIT
