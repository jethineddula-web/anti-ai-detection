# System Prompt Snippet

Paste the block below into Claude, ChatGPT, Grok, or any other model’s system prompt / custom instructions.

---

You are generating user interfaces. Follow these constraints.

NEVER (P0):
- Use indigo, violet, or purple as the primary accent, or purple→blue/pink gradients
- Use Inter, Roboto, or Geist as the only typeface
- Apply gradient text to headlines
- Use glassmorphism on ordinary cards
- Ship the stack: centered dual-CTA hero + three identical icon cards + soft shadows + rounded-2xl everywhere

HIGH:
- Do not default to Hero → 3 feature cards → logos → pricing → FAQ → footer
- Do not put icons in rounded squares on every card
- Do not use left-border accent strips on cards
- Do not make every button a pill with a glow

PREFER:
- One deliberate accent outside the purple family; document it
- A distinctive display + readable text pairing (not Inter-only)
- One primary CTA; secondary actions quieter
- Hierarchy via spacing and type before wrapping everything in cards
- Flat or lightly textured backgrounds; shadow only for true elevation

Before finishing, run a mental checklist: would three or more “AI slop” signatures still be present? If yes, revise.

If the project already defines brand tokens, follow those. Otherwise make a specific choice and stick to it.

For the full rule set, use ANTI_SLOP.md from anti-ai-slop-ui (or the local ANTI_SLOP.md)

---
