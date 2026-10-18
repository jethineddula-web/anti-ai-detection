# Pre-ship Checklist

Run this before considering a UI finished. Any “yes” is a signal to revise.

## Instant-death (fix immediately)

- [ ] Primary accent is indigo, violet, or purple, or the design uses a purple-leaning multi-stop gradient
- [ ] Only typeface is Inter, Roboto, Geist, or bare system-ui
- [ ] Headlines use gradient fill / `bg-clip-text`
- [ ] Hero is centered with a pill badge + two equal CTAs (“Get Started” / “Learn More”)
- [ ] Feature row is exactly three identical cards with icon-in-rounded-square
- [ ] Ordinary cards use glassmorphism (`backdrop-blur` + translucent fill + light border)
- [ ] Soft shadow + large uniform radius (`rounded-2xl`) on nearly every surface
- [ ] Page skeleton is Hero → 3 cards → logos → pricing → FAQ → footer with nothing justified by content

## High smell (usually fix)

- [ ] Left-border accent strips on content cards
- [ ] Pulsing “Live” / “New” / “Beta” badges that are not tied to real state
- [ ] Nested cards without a clear hierarchy reason
- [ ] Decorative emoji or generic Lucide icons as the main visual identity
- [ ] Every heading is extrabold + tight tracking
- [ ] Buttons, cards, inputs, and badges all share one oversized radius
- [ ] Glow / neon shadows on primary buttons

## Medium smell (judge in context)

- [ ] Every card in a grid scales up on hover
- [ ] Aurora blobs or light orbs behind the hero with no brand reason
- [ ] Dual CTAs with no visual hierarchy
- [ ] Generic copy (“seamless,” “unlock,” “next-generation,” “all-in-one”)
- [ ] Shadows on resting surfaces as strong as modal elevation

## Pass criteria

If you checked **any** instant-death item, do not ship until cleared.

If you checked **two or more** high-smell items, the UI will still read as AI-generated to most viewers. Revise before shipping.
