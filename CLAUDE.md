# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
# Install Mintlify CLI (requires Node.js v19+)
npm i -g mint

# Preview docs locally at http://localhost:3000
mint dev

# Check for broken links
mint broken-links

# Update CLI to latest version
npm mint update
```

## Architecture

This is a [Mintlify](https://mintlify.com) documentation site. All content is MDX with YAML frontmatter.

- **`docs.json`** — Central configuration: navigation structure, theme colors, logo, navbar, footer. All pages must be registered here under `navigation.tabs[].groups[].pages[]`.
- **`*.mdx` files** — Content pages. Each needs a `title` and `description` in frontmatter.
- **`snippets/`** — Reusable MDX content. Import with `import SnippetName from '/snippets/filename.mdx'`.
- **`api-reference/openapi.json`** — OpenAPI spec used to auto-generate API reference pages.
- **`.mintignore`** — Files Mintlify ignores when building; drafts go in `drafts/` or named `*.draft.mdx`.

### Navigation

Navigation is defined entirely in `docs.json`. Adding a new page requires both creating the `.mdx` file and adding its path (without extension) to the appropriate group in `docs.json`.

## Writing style

- Active voice and second person ("you")
- Sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, and inline code references
- One idea per sentence

## Mintlify skill

For Mintlify component reference and writing standards, the Mintlify skill can be installed:

```bash
npx skills add https://mintlify.com/docs
```
