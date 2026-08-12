# SKILL.md Generator

A single-page static tool for preparing valid `SKILL.md` files. Experts fill in each section as plain text; the page assembles a properly formatted markdown file with YAML frontmatter and downloads it.

Why: markdown files exported from Google Docs/Word often contain smart quotes, backslash-escaped punctuation, and invisible unicode characters that make the file invalid. This tool sanitizes pasted text automatically and generates the file programmatically, so the output is always clean.

## Features

- Live preview of the generated file
- Automatic cleanup of Google Docs/Word paste artifacts (smart quotes, escaped `\*` `\#` etc., non-breaking/zero-width spaces)
- YAML frontmatter with a slugified `name:` and a safely quoted `description:` (taken from the first line of "When to Use This Skill")
- Download or copy-to-clipboard

## Deploy

Static site, no build step. On Vercel: **Add New Project → Import this repo → Deploy** (framework preset: Other). Every push to `main` redeploys automatically.
