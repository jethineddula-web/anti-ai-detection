# Anti-AI-Slop UI

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](./CONTRIBUTING.md)

A practical catalog of the visual patterns that make AI-generated interfaces look identical — and hard constraints so models stop shipping the same design.

AI tools (Claude, ChatGPT, Grok, v0, Lovable, Cursor, Bolt, and others) do not invent design. They reproduce the statistical mean of their training data: Tailwind defaults, shadcn examples, and SaaS marketing templates. The result is competent, polished, and interchangeable **AI slop**.

This repo documents those defaults, bans the worst of them, and gives you copy-paste rules for agents.

---

## Quick start

### 1. Any AI (Claude, ChatGPT, Grok, etc.)

Paste the full contents of [`ANTI_SLOP.md`](./ANTI_SLOP.md) into your system prompt, custom instructions, or project rules. Then ask it to design.

Shorter option: use [`prompts/system-prompt-snippet.md`](./prompts/system-prompt-snippet.md).

### 2. Cursor / Claude Code / similar

- Cursor: copy [`prompts/cursor-rules.md`](./prompts/cursor-rules.md) into `.cursorrules` or project rules.
- Claude: paste [`prompts/claude-project-instructions.md`](./prompts/claude-project-instructions.md) into project instructions.

### 3. Before you ship

Run [`checklist.md`](./checklist.md). Any “yes” means revise.

**Most important single file:** put **`ANTI_SLOP.md`** into your system prompt or project rules. That file has the negative constraints, severity levels, and alternatives an AI needs to stop defaulting to the mean.

---

## What’s in this repo

| Path | Purpose |
|------|---------|
| [`ANTI_SLOP.md`](./ANTI_SLOP.md) | Primary constraint file for models (P0 / HIGH / MEDIUM) |
| [`checklist.md`](./checklist.md) | Pre-ship review checklist |
| [`patterns/`](./patterns/) | Deep dives: color, type, layout, components, effects |
| [`examples/bad/`](./examples/bad/) | Side-by-side “slop” HTML |
| [`examples/better/`](./examples/better/) | Deliberate alternatives |
| [`prompts/`](./prompts/) | Ready-to-paste snippets for Cursor, Claude, system prompts |
| [`tokens/design-tokens.css`](./tokens/design-tokens.css) | Example tokens that avoid common defaults |

---

## The “you’ll know it when you see it” stack

These together almost always look AI-generated:

- Indigo / violet / purple → blue / cyan gradient (especially `from-indigo-500 to-purple-600`)
- Inter, Geist, or Roboto as the only typeface
- Centered hero with dual CTAs (“Get Started” + “Learn More”) and a pill badge
- Exactly three identical feature cards with icon-in-rounded-square
- Glassmorphism, aurora blobs, soft shadows and `rounded-2xl` on everything
- Hero → 3 cards → logos → pricing → FAQ → footer skeleton

This project exists so that stack is not the only design an AI can produce.

---

## Philosophy

- **Negative constraints work.** Models need “do not” more than vague “be original.”
- **Severity matters.** P0 items are instant-death; MEDIUM items are smell tests.
- **Examples beat lectures.** Bad vs better HTML makes the difference obvious.
- **Tokens are optional.** A deliberate accent and type pair beat another indigo/Inter kit.

---

## Contributing

Bug reports, better examples, and tighter rules are welcome. See [CONTRIBUTING.md](./CONTRIBUTING.md).

Please read the [Code of Conduct](./CODE_OF_CONDUCT.md) before participating.

---

## Security

This is a documentation and example kit (no runtime service). See [SECURITY.md](./SECURITY.md) if you find something sensitive or harmful in the repo.

---

## License

[MIT](./LICENSE) — use freely in prompts, products, and teaching.

---

## Related reading

- Pattern guides in [`patterns/`](./patterns/)
- Example tokens in [`tokens/`](./tokens/)
- Support: [SUPPORT.md](./SUPPORT.md)
- Changelog: [CHANGELOG.md](./CHANGELOG.md)
