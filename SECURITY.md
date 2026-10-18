# Security policy

## Supported versions

Anti-AI-Slop UI is a **documentation and static-example** project (Markdown, HTML, CSS). There is no hosted application, API, or package runtime to version-support in the usual sense.

| Content | Supported |
|---------|-----------|
| Latest `main` | Yes |
| Older commits / forks | Best effort only |

## What counts as a security issue here

Please report:

- Secrets, tokens, or credentials accidentally committed
- Malicious or unexpected scripts in example HTML
- Links that clearly distribute malware
- Social-engineering content aimed at contributors

Out of scope (use normal Issues instead):

- Design taste disagreements
- “This still looks like AI slop” feedback
- Typos and broken internal links

## Reporting a vulnerability

1. **Do not** open a public issue with exploit details if the report is sensitive.
2. Contact the repository owner on GitHub (security advisory if enabled, otherwise a private channel listed on their profile), or open a minimal public issue titled `Security: please contact me` without sensitive detail.
3. Include:
   - File path and commit (if known)
   - What is exposed or harmful
   - Suggested fix if you have one

You should receive an acknowledgment when someone is available. There is no bug bounty for this project.

## Safe use of examples

- `examples/bad/` intentionally demonstrates anti-patterns for teaching. Do not ship those files as production UI without revision.
- Prefer opening HTML examples locally or via GitHub’s raw/preview flows you trust.
- Treat third-party CDN links inside examples as convenience only; pin or self-host if you adopt them in real products.
