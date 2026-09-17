# reseller-agent-kit

A system prompt + Claude plugin that turns any capable LLM into an **autonomous reseller operator** — one that only buys against real sold comps, keeps a hard margin floor, lists honestly, answers buyers, and reports daily.

It is a **decision engine**, not a money printer. It does the research, pricing, copy, and comms. You still make the buys it approves and hand the box to the carrier. No fake reviews, no faked condition, no "passive income" fantasy.

## What's in here

| File | What it is |
|------|-----------|
| `SYSTEM_PROMPT.md` | The full operator prompt. Paste into Grok / GPT / Claude and go. |
| `skills/reseller/SKILL.md` | Same logic as a Claude Code / Claude plugin skill. |
| `commands/` | Slash commands: `/source`, `/list`, `/report`. |
| `.claude-plugin/plugin.json` | Plugin manifest so it installs as a plugin. |
| `INSTRUCTIONS.md` | 2-minute setup for both paths. |

## Two ways to run it

**1. Raw prompt (fastest, any model)**
Copy all of `SYSTEM_PROMPT.md` into a new chat's system/custom-instructions field. Start with:
> "Here's my situation: [budget], [categories I can ship], [margin floor]. Run Phase 1."

**2. As a Claude plugin**
See `INSTRUCTIONS.md`. Gives you `/source`, `/list`, and `/report` as commands.

## The rules it will not break

- **No blind buys** — nothing gets sourced without sold comps showing margin above the floor.
- **Margin floor** — skips anything under 35% net *after* fees and shipping.
- **Sold comps only** — never prices off asking prices.
- **Fees in every number** — marketplace + payment + shipping, always.
- **Honesty** — every flaw named, no stock photos as the real item.
- **Approval gates** — never spends, refunds, or accepts a return over your limit without a yes.

## What it can't do (on purpose)

- It doesn't touch your money or your account for you — it recommends, you execute.
- It can't hand the box to the carrier.
- It won't invent comps, conditions, or numbers to make a deal look good.

## License

MIT — do whatever you want with it. Built by [@0xSolty](https://x.com/0xSolty).
