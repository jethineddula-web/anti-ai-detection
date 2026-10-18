# Contributing to Anti-AI-Slop UI

Thanks for helping keep AI-generated interfaces from all looking the same.

## Ways to contribute

- **New banned patterns** — with severity (P0 / HIGH / MEDIUM), a short “why AIs do it,” and a prefer-instead note
- **Better examples** — paired HTML in `examples/bad/` and `examples/better/`
- **Prompt snippets** — Cursor, Claude, system-prompt variants that stay short and usable
- **Checklist items** — concrete yes/no checks, not vague taste advice
- **Docs fixes** — typos, clearer wording, broken links

## Ground rules

1. Prefer **specific, enforceable rules** over aesthetic essays.
2. Every new P0/HIGH rule should name **what to do instead**, not only what to ban.
3. Keep `ANTI_SLOP.md` scannable; put long explanation in `patterns/`.
4. Examples should open in a browser without a build step when possible.
5. Do not add telemetry, trackers, or minified third-party blobs without discussion.
6. Match existing tone: direct, practical, no hype.

## Local setup

This repo is mostly Markdown and static HTML. No install required.

```bash
git clone https://github.com/jethineddula-web/anti-ai-detection.git
cd anti-ai-detection
# open README.md, ANTI_SLOP.md, or examples/*/*.html in a browser / editor
```

## Pull request process

1. Fork (or branch) from `main`.
2. Make a focused change (one pattern or one docs area per PR when you can).
3. Update `CHANGELOG.md` under **Unreleased** if the change is user-visible.
4. Open a PR with:
   - **What** changed
   - **Why** (link to a real slop example if relevant)
   - Screenshots for HTML example changes

## Commit style

Clear present-tense messages are enough:

- `Add P0 ban for left-border card accents`
- `Improve better/hero.html type pairing`
- `Document Cursor rules install path`

## Code of conduct

Participation is covered by [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md).

## Questions

Use GitHub Issues for proposals and bugs. For large restructures (new top-level layout, renaming the project), open an issue first.
