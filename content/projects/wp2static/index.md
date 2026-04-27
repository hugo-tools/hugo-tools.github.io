---
title: "wp2static"
date: 2026-04-27T00:00:00Z
draft: false
weight: 20
name: "wp2static"
category: "support"
repo: "https://github.com/hugo-tools/wp2static"
homepage: ""
status: "active"
language: "Python"
description: "Migrate a WordPress MySQL dump to a Hugo or Jekyll content tree so the resulting static site can be built by any CI runner."
install: "Run as a container: `docker run --rm -v $PWD:/data ghcr.io/hugo-tools/wp2static:latest --sql /data/dump.sql --out /data/out`"
---

Streams a `mysqldump` of a WordPress site and emits a Hugo or Jekyll
content tree on the other side.

**What it does**

- Reads `wp_posts`, `wp_postmeta`, taxonomy tables and the FinalTiles
  Gallery plugin tables without ever needing MySQL.
- Emits one file per published post / page with YAML (Jekyll) or TOML
  (Hugo) front-matter.
- Cleans up bodies: `[caption]` → `<figure>`, `[gallery]` and
  FinalTiles shortcodes resolved to first-class gallery directives,
  `wp-content/uploads` links rewritten to `/uploads/`.
- Renders Elementor `_elementor_data` to plain HTML.
- Optional theme scaffolding: copies static assets, parses
  `style.css`, transpiles PHP templates to Liquid (Jekyll) or Go
  `html/template` (Hugo). It's a scaffold, not a drop-in port —
  unmapped PHP is left inline as a visible comment and summarised
  in `MIGRATION.md`.

Distributed as a GHCR container so the migration runs without
cloning or building anything.
