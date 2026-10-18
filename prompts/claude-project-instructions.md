# Claude Project Instructions Example

Paste into a Claude Project’s custom instructions, or into Claude Code’s project context.

```
When generating UI for this project, treat the following as hard constraints.

P0 — do not:
- Primary accent in indigo / violet / purple, or purple-family gradients
- Inter / Roboto / Geist as the sole typeface
- Gradient text on headlines
- Glassmorphism, aurora blobs, or glow shadows as default decoration
- The generic SaaS skeleton (centered dual-CTA hero, three icon cards, logo row, pricing, FAQ) unless the user explicitly asks for that structure

Prefer:
- Existing brand tokens in the repo if any
- Otherwise one documented accent and a display + body type pair that is not Inter-only
- One dominant CTA; concrete copy over “seamless / unlock / next-generation”
- Cards only when items are comparable units

Before large UI surfaces, skim ANTI_SLOP.md and checklist.md if available in the project.
```
