# Components

## Buttons

**Do not**
- Make every primary button `rounded-full` (pill).
- Add glowing `box-shadow` or neon effects.
- Use the same oversized radius on buttons, cards, and inputs.

**Prefer**
- A moderate, consistent radius (roughly 6–10 px) unless the brand is explicitly playful.
- Solid fills or clear borders. Let the accent color carry the emphasis.
- Clear visual hierarchy between primary and secondary actions.

### Before (slop)
```html
<button class="rounded-full bg-gradient-to-r from-indigo-500 to-purple-600 px-6 py-3 text-white shadow-lg shadow-indigo-500/50">
  Get Started
</button>
```

### After
```html
<button class="rounded-md bg-[#c45c26] px-5 py-2.5 text-white hover:bg-[#a34a1d]">
  Start free trial
</button>
```

## Cards

**Do not**
- Apply `rounded-2xl shadow-lg border` to every card.
- Add a colored left-border accent strip to ordinary content cards.
- Place an icon inside a rounded square at the top of every card.
- Nest cards without a clear hierarchy reason.

**Prefer**
- Use cards only for distinct, comparable items.
- Rely on spacing and typography for grouping when possible.
- If a border or background is needed, keep it subtle and consistent with the rest of the system.

### Before (slop)
```html
<div class="rounded-2xl border border-gray-200 bg-white p-6 shadow-lg">
  <div class="mb-4 flex h-12 w-12 items-center justify-center rounded-xl bg-indigo-100">
    <!-- Lucide icon -->
  </div>
  <h3 class="text-lg font-semibold">Feature title</h3>
  <p class="text-gray-600">Short generic description.</p>
</div>
```

### After
```html
<div class="border-b border-stone-200 py-6">
  <h3 class="font-serif text-xl text-stone-900">Specific capability</h3>
  <p class="mt-2 text-stone-600">Concrete description of what the user can do.</p>
</div>
```

## Badges and pills

**Do not**
- Place a pulsing “Live”, “New”, or “Beta” pill above every headline.
- Use fully rounded badge chips as decoration across the page.

**Prefer**
- Reserve badges for genuine status or category information.
- Style them simply; avoid animation unless the status is actually changing.

## Heroes

See `layout.md`. Avoid the centered dual-CTA + badge pattern and gradient text.

## Icons

**Do not**
- Default to Lucide (or similar) icons inside rounded squares for every feature.
- Use emoji as icons in production interfaces.

**Prefer**
- Omit decorative icons when the text is clear.
- Use icons only when they improve scanning and are consistent in weight and style.
