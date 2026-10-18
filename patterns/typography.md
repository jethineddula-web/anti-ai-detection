# Typography

## Banned defaults (P0 / HIGH)

Do not use these as the sole or primary typeface without an explicit brand reason:

- Inter
- Roboto
- Geist
- system-ui / -apple-system / BlinkMacSystemFont stack as the only voice

Also avoid:

- Gradient fills on headlines
- `font-extrabold tracking-tighter` on every heading
- Wide letter-spacing on body copy “for elegance”

## Why AIs default here

Inter is the most common UI font in open kits and Tailwind examples. Extreme weight + tight tracking is a frequent “impact” pattern in tutorials.

## Prefer instead

Pair a distinctive display face with a readable text face. Examples that are not the usual defaults:

- Fraunces + Source Serif 4
- Instrument Serif + Newsreader
- Bricolage Grotesque + Literata

Guidelines:

- Use weight and size for hierarchy; keep body at a comfortable measure and line-height
- Limit display faces to headlines; keep UI chrome legible
- Load only the weights you use

## Quick checks

- [ ] Not Inter/Roboto/Geist-only
- [ ] No gradient headline text
- [ ] Headings are not all extrabold + ultra-tight
- [ ] Body line-length is readable (~45–75 characters)

## Note

If the product already has a brand type system, follow it. Do not “upgrade” back to Inter when a better pairing is available.
