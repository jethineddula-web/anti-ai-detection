# Effects

## Banned or heavily restricted (P0 / HIGH)

Do not apply these by default:

- Glassmorphism on ordinary cards or panels:
  ```css
  backdrop-filter: blur(12px);
  background: rgba(255, 255, 255, 0.1);
  border: 1px solid rgba(255, 255, 255, 0.2);
  ```
- Aurora blobs, glowing orbs, or radial light blooms behind heroes for pure decoration.
- Soft drop shadows on every surface (`shadow-lg` or equivalent on all cards, buttons, and containers).
- Neon box-shadows on buttons or interactive elements.
- Gradient text as a decorative effect on headlines or metrics.

### Why these appear

Glassmorphism, soft shadows, and glowing gradients were popular in 2021–2023 design tutorials and marketing examples. Models associate them with “modern” and “premium” and apply them whenever the prompt asks for something polished.

## Preferred treatments

**Backgrounds**
- Flat or very lightly textured surfaces.
- Near-neutrals with a slight temperature (warm off-white, cool gray, true charcoal).
- Avoid pure white + pure black + cyan/purple accents as the automatic dark mode.

**Shadows**
- Almost none on resting content.
- Use shadow only for true elevation (modals, dropdowns, popovers).
- Prefer a single, controlled shadow definition rather than Tailwind’s default scale applied everywhere.

**Blur**
- Use `backdrop-filter` only when there is a functional reason (modal overlay, sticky header over scrolling content, etc.).
- Do not apply it to feature cards or marketing panels by default.

**Gradients**
- See `color.md`. If used, keep them single-hue and purposeful.

## Example of restrained elevation

```css
.card {
  background: var(--bg);
  border: 1px solid var(--border);
  border-radius: 8px;
  /* no shadow */
}

.modal {
  background: var(--bg);
  border-radius: 12px;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.12);
}
```

Remove decorative effects first. Add them back only when they communicate something specific.
