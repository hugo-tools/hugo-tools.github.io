---
title: "Hugo Studio Plugins"
date: 2026-04-27T00:00:00Z
draft: false
weight: 30
name: "hugo-studio-plugins"
category: "core"
repo: "https://github.com/hugo-tools/hugo-studio-plugins"
homepage: "https://hugo-tools.github.io/hugo-studio-plugins/"
status: "active"
language: "Hugo"
description: "Community plugin marketplace for Hugo Studio — a Hugo site that doubles as a directory and a JSON feed the editor consumes."
install: "Browse at https://hugo-tools.github.io/hugo-studio-plugins/ — the editor's Browse tab pulls the same JSON feed."
---

A Hugo-powered directory of community plugins for the editor.
Submitting a plugin is just opening a PR with a new
`content/plugins/<name>/index.md`; CI validates the front-matter
shape against the schema and rebuilds the JSON feed at
`/plugins/index.json` that the editor's Browse tab consumes.

**Extension points the marketplace tracks**

- `panel` — adds a tab to the editor's site shell.
- `fieldRenderer` — replaces the front-matter form's renderer for a
  specific field key.
- `dataFormat` — adds support for additional file types under
  `data/` (e.g. `.xlsx`, `.kml`).
- `shortcode` — body-editor toolbar picker + Rich-editor preview
  node for a Hugo shortcode.
