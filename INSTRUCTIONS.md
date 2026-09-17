# Setup (2 minutes)

## Path A — Raw prompt (any model: Grok, GPT, Claude)

1. Open `SYSTEM_PROMPT.md` and copy the whole thing.
2. Paste it into the model's **system prompt** / **custom instructions** field
   (in ChatGPT: a Project's instructions; in Grok: the workspace/custom prompt).
3. Send your first message:
   ```
   Budget: $300 to start.
   Categories I can ship: small electronics, headphones, retro games.
   Margin floor: 35% net after fees.
   Sign-off required on any single buy over $80.
   Run Phase 1.
   ```
4. It will ask a few intake questions, then start scanning and pricing.

> Tip: give it real sold-comp data (paste the last 10 sold prices) so it works from
> facts, not guesses. The prompt is built to refuse a buy when comps are thin.

## Path B — Claude plugin

1. Clone this repo somewhere Claude Code can see it:
   ```bash
   git clone https://github.com/<you>/reseller-agent-kit.git
   ```
2. Add it as a plugin (Claude Code):
   ```
   /plugin marketplace add ./reseller-agent-kit
   /plugin install reseller-agent-kit
   ```
3. Use the commands:
   - `/source` — scan candidates and rank by net profit
   - `/list` — turn an approved item into a full, honest listing
   - `/report` — daily P&L + what needs a human decision

## Recommended workflow

1. `/source` a batch → it hands you a ranked shortlist with expected net.
2. You approve the buys (it never spends for you).
3. `/list` each item → clean title, honest description, photo checklist.
4. Let it manage offers/repricing within the floor.
5. `/report` at end of day.

That's it. Keep the floor sacred and let it turn inventory.
