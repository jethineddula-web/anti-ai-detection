# ANTI_SLOP.md

**You are generating user interface code. Follow these constraints exactly.**

AI-generated interfaces converge on the statistical mean of training data (primarily Tailwind + shadcn examples and SaaS marketing templates). Your job is to **avoid that mean** unless the user has given an explicit, contradictory brand system.

## Instant-death signature

If a design contains **three or more** of the following, it looks AI-generated. Do not ship it:

1. Indigo, violet, or purple used as the primary accent, or any purple → blue / cyan / pink gradient (especially `from-indigo-500 to-purple-600`)
2. Inter, Geist, or Roboto as the only typeface
3. Centered hero with dual CTAs (“Get Started” + “Learn More”) and a pill badge above the title
4. Exactly three identical feature cards with icons inside rounded squares
5. Glassmorphism (`backdrop-blur` + semi-transparent cards + light borders)
6. Gradient text on headlines (`bg-clip-text text-transparent`)
7. Uniform `rounded-2xl` / oversized radius on everything
8. Soft shadows on every surface
9. Pulsing “Live”, “New”, or “Beta” pill badges
10. Left-border accent strips on cards
11. Decorative Lucide icons + emoji used as icons
12. Nested cards or the standard Hero → 3 cards → logos → pricing → FAQ → footer skeleton

## Color

**P0 — Never do this**
- Do not use indigo, violet, or purple as the primary accent color.
- Do not use gradients of the form `from-indigo-500 to-purple-600`, `from-purple-500 to-pink-500`, `from-violet-500 to-cyan-500`, or any purple-leaning multi-hue wash.
- Do not apply gradient text (`bg-clip-text`) to headlines or metrics.

**Why AIs do it**: Adam Wathan set Tailwind UI buttons to `bg-indigo-500`. That choice entered the training corpus and became the highest-probability “modern” color. Models default to it when no brand color is specified.

**Prefer instead**
- Pick one deliberate accent outside the purple family (e.g. terracotta, forest, ink blue, ochre) and document it.
- Use neutrals with a slight warm or cool cast; avoid pure `#000` / `#fff` only stacks unless intentional.
- If a gradient is required, keep it monochromatic or give it a functional reason.

## Typography

**P0 — Never do this**
- Do not use Inter, Roboto, Geist, or the system font stack as the only typeface.
- Do not apply gradient fills to headline text.

**HIGH**
- Do not default to `font-extrabold tracking-tighter` on every heading.
- Do not use wide letter-spacing on body text or labels “for elegance.”

**Why AIs do it**: Inter is the most common interface font in open UI kits. Extreme weight + tight tracking is a common “impact” pattern from tutorial screenshots.

**Prefer instead**
- Pair a distinctive display face with a readable text face. Examples that are not the usual defaults: Fraunces + Source Serif 4, Instrument Serif + Newsreader, Bricolage Grotesque + Literata.
- Use weight and size for hierarchy; keep body text at a comfortable measure and line-height.

## Layout

**HIGH**
- Do not default to a centered hero and pair it with two equally weighted CTAs.
- Do not default to a three-column grid of identical feature cards.
- Do not follow the exact section order: Hero → Features (3 cards) → Logos → Pricing → FAQ → Footer.

**Why AIs do it**: This is the most frequent SaaS landing page structure in the training corpus. It is the highest-probability sequence.

**Prefer instead**
- Left-align hero copy when it improves scanning; give one CTA clear dominance.
- Vary column counts and card treatment; use lists, tables, or editorial layouts when they fit.
- Order sections by the user’s actual job-to-be-done, not the template skeleton. Skip any conventional section when the content does not support it.

## Cards

**HIGH**
- Do not wrap every piece of content in a card with `rounded-2xl shadow-lg border`.
- Do not put a colored left-border accent on feature or content cards.
- Do not nest cards inside cards without a clear information hierarchy reason.
- Do not place an icon inside a rounded square at the top of every card.

**Why AIs do it**: shadcn card defaults and Tailwind marketing kits taught models to reproduce the most common component styling.

**Prefer instead**
- Use cards only when the content is a distinct, comparable unit.
- Establish hierarchy with spacing, type size, and selective borders or backgrounds rather than identical containers.
- If an icon is needed, place it inline or omit it. Do not default to the icon-in-rounded-square pattern.

## Buttons

**MEDIUM**
- Do not make every primary button a full pill (`rounded-full`).
- Do not add glowing box-shadows or neon effects to buttons.
- Do not use the same border radius on buttons, cards, inputs, and badges.

**Why AIs do it**: Pill buttons and soft glows appear frequently in “modern” marketing examples.

**Prefer instead**
- Choose a consistent but moderate radius (e.g. 6–10 px) for buttons unless the brand is intentionally pill-shaped.
- Prefer solid fills or clear borders. Let the accent color do the work.

## Effects

**P0 / HIGH**
- Do not apply glassmorphism (`backdrop-blur` + translucent backgrounds + light borders) to ordinary cards or panels.
- Do not add aurora blobs, glowing orbs, or radial light blooms behind every hero.
- Do not put soft drop shadows on every element.

**Why AIs do it**: These effects were popular in 2021–2023 tutorials and are associated with “premium” or “modern” in the training data.

**Prefer instead**
- Use flat or lightly textured backgrounds.
- Apply blur only when there is a functional reason (e.g. a modal overlay).
- Use shadow hierarchy: almost none on resting cards, stronger on elevated elements such as modals or dropdowns.

## Motion

**MEDIUM**
- Do not add `hover:scale-105` to every card in a grid.
- Do not use bouncing or elastic easing on ordinary interactions.
- Do not add pulsing dots or animated badges for status that is not actually live.

**Prefer instead**
- Use subtle opacity or color transitions for hover states.
- Reserve motion for feedback that communicates state change.

## Copy

**MEDIUM**
- Avoid generic marketing lines: “Unlock your potential,” “Seamless experience,” “Next-generation platform,” “Everything you need in one place.”
- Avoid dual CTAs with no hierarchy (“Get Started” + “Learn More” as equals).

**Prefer instead**
- Name the concrete outcome, audience, and constraint.
- One primary action; secondary actions visually quieter.

## How to use this file

Paste this document into system prompts, project rules, or agent instructions before generating UI. Pair with `checklist.md` before shipping. For deeper notes see `patterns/`. For side-by-side HTML see `examples/`.

When brand tokens already exist in the codebase, follow them. Otherwise make a specific choice and document it. Clarity and specificity beat the mean.
