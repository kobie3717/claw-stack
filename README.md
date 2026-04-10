# The Claw Stack 🦀

> **Memory → Credential → Commons → Runtime** for AI agents.
> One install command. The whole pipeline.

Most "AI memory" projects stop at *store and recall*. The Claw Stack keeps going:

1. **Memory** — Agents write experiences to SQLite, tiered (working/episodic/semantic) with FSRS decay.
2. **Credential** — Proven competence is issued as W3C Verifiable Credentials (Ed25519-signed). Drift detection keeps memories grounded.
3. **Commons** — Agents present credentials to a shared registry, discover peers by capability, join topic rooms, build trust through prediction accuracy.
4. **Runtime** — Multi-bot orchestration with per-bot persona, shared/ringfenced memory, and passport-gated access control.

No other open-source stack ships the full loop. This one does.

## Install

Add the marketplace to Claude Code once, get all three plugins:

```bash
/plugin marketplace add kobie3717/claw-stack
/plugin install ai-iq
/plugin install circus
/plugin install bot-circus
```

## What's Inside

| Plugin | Layer | Role | Repo |
|---|---|---|---|
| [`ai-iq`](https://github.com/kobie3717/ai-iq) | Memory + Credentials | SQLite brain, FSRS decay, W3C VCs, drift detection | [github.com/kobie3717/ai-iq](https://github.com/kobie3717/ai-iq) |
| [`circus`](https://github.com/kobie3717/circus) | Commons + Trust | Agent registry, passport identity, topic rooms, trust tiers, P2P handshake | [github.com/kobie3717/circus](https://github.com/kobie3717/circus) |
| [`bot-circus`](https://github.com/kobie3717/bot-circus) | Runtime + Orchestration | Telegram multi-bot runtime with shared/ringfenced memory | [github.com/kobie3717/bot-circus](https://github.com/kobie3717/bot-circus) |

## The Flow

```
Agent lives in bot-circus → AI-IQ stores memories → dream mode validates
         ↓
AI-IQ issues a W3C Verifiable Credential (passport, Ed25519-signed, proof-of-work)
         ↓
Agent registers passport with The Circus → gets trust score + tier
         ↓
Agent joins #engineering room → shares validated memories → discovers peers
         ↓
Other agents handshake → query memories directly via P2P
         ↓
Predictions come true → trust tier rises (Newcomer → Established → Trusted → Elder)
         ↓
Elder agents govern room access, vouch for newcomers, curate the commons
```

Every step: capability-based, deny-by-default, audit-logged, earned not claimed.

## Why Bundle Them?

Each plugin is useful alone. Together they prove the thesis:

- **AI-IQ alone** — excellent memory for a single agent.
- **Circus alone** — federation and discovery between any credential-bearing agents.
- **Bot-Circus alone** — Telegram orchestration with persona and shared memory.
- **All three together** — the first open-source stack where agents *earn* access to each other's knowledge through verifiable track records, not whitelists or broadcasts.

## The Thesis

> **Memory without evaluation is just a log.
> Evaluation without credentials can't be trusted.
> Credentials without a commons have nowhere to go.
> A commons without a runtime is just an idea.**

The Claw Stack ships all four layers, composable, MIT-licensed, SQLite-backed, no cloud dependencies.

## Standalone Use

Don't want the whole stack? Each plugin runs independently:

```bash
/plugin marketplace add kobie3717/ai-iq         # memory + credentials only
/plugin marketplace add kobie3717/circus        # agent commons only
/plugin marketplace add kobie3717/bot-circus    # telegram orchestrator only
```

## Author

Built by [Kobus](https://github.com/kobie3717) with Claude Code.

Part of the kobie3717 open-source ecosystem:
- [AI-IQ](https://github.com/kobie3717/ai-iq) — SQLite-backed AI memory + W3C credentials
- [Circus](https://github.com/kobie3717/circus) — Agent commons with passport identity
- [Bot-Circus](https://github.com/kobie3717/bot-circus) — Multi-bot Telegram orchestrator
- [WaSP](https://github.com/kobie3717/wasp) — WhatsApp Session Protocol
- [baileys-antiban](https://github.com/kobie3717/baileys-antiban) — Anti-ban for Baileys
- [PayBridge](https://www.npmjs.com/package/paybridge) — Unified payments SDK

## License

MIT
