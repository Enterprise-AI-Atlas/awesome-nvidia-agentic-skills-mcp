# Contributing

Contributions are welcome. Please read this guide before opening a pull request.

## What belongs in this list

This registry is for resources that help AI agents, coding assistants, and MCP clients interact with NVIDIA products. Acceptable entries include:

- Agentic skills for NVIDIA products (OpenCode skills, Cursor rules, Claude Code instructions, etc.).
- MCP servers that expose NVIDIA products or APIs.
- Provider extensions or configurations that connect coding agents to NVIDIA endpoints.
- Official reference implementations with clear agent-facing interfaces.

## What does **not** belong

- General SDK documentation or tutorials that are not agent/coding-assistant oriented.
- Projects where NVIDIA support is one of many interchangeable LLM providers.
- Closed-source or paywalled-only tools with no public documentation.
- Duplicate entries.

## Quality bar

Every submission must be:

1. **Publicly accessible** — open source or publicly documented.
2. **Actively maintained** — last meaningful commit or release within the last 12 months (exceptions for official NVIDIA reference repos).
3. **Documented** — a real README with setup or install instructions.
4. **Correctly categorized** — placed under the NVIDIA product it primarily targets.
5. **Honestly labeled** — use the `Official` or `Community` badge.

## Entry format

Use this pattern:

```markdown
- **[Name](URL)** `Official` — One-sentence description.
  - Install: `command here`
```

If there is no install command, omit the install line.

## Product sections

The README is organized by **NVIDIA product line**, not by resource type. New product sections are allowed only if they contain at least three entries.

## Pull request process

1. Fork the repository.
2. Add your entry in the correct product section.
3. Run `./scripts/validate-links.sh` and fix any broken links or anchors.
4. Open a pull request with a clear description of the resource and why it fits.

One resource per pull request is preferred.
