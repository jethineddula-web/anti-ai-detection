# Color

## Banned patterns (P0)

Do not use these as primary accents or decorative washes:

- `indigo-500` / `#6366f1`
- `violet-500` / `#8b5cf6`
- `purple-500` / `#a855f7`
- Gradients of the form indigo → purple, purple → pink, violet → cyan
- Gradient text on headlines (`bg-clip-text text-transparent`)

## Why AIs default here

Tailwind UI popularized indigo buttons. That token dominates open UI samples, so models treat purple-family accents as the safe “modern” choice when no brand is specified.

## Prefer instead

- One deliberate accent **outside** the purple family (terracotta, forest, ink, ochre, rust, teal with restraint).
- Neutrals with a slight warm or cool cast — not pure `#000` / `#fff` only unless intentional.
- Monochrome or single-hue gradients if a gradient is required; give it a functional reason.
- Document the choice in tokens or a short design note so agents stop re-rolling indigo.

## Quick checks

- [ ] Accent is not indigo / violet / purple
- [ ] No purple-leaning multi-stop hero gradient
- [ ] No gradient-filled H1
- [ ] Accent hex or token is written down somewhere the model can see

## Example direction

See `tokens/design-tokens.css` — terracotta accent, warm neutrals, no purple family.
