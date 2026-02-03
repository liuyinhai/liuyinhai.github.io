# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Hugo static site blog using the PaperMod theme (as a Git submodule).

## Common Commands

```bash
# Local development server (localhost:1313)
hugo serve

# Build for production (outputs to /public/)
hugo

# Create new post
hugo new content/posts/my-post.md

# Clone with submodules (for fresh clone)
git clone --recurse-submodules <repo>

# Initialize submodules (if already cloned without --recurse-submodules)
git submodule update --init --recursive
```

## Requirements

- Hugo >= 0.146.0
- PaperMod theme (Git submodule at themes/PaperMod)

## Architecture

- `hugo.toml` - Main Hugo configuration (baseURL, title, theme settings)
- `content/posts/` - Blog posts in Markdown with TOML frontmatter
- `archetypes/default.md` - Template for new posts (sets date, draft=true, title from filename)
- `themes/PaperMod/` - Theme submodule (do not edit directly; override in `layouts/`)
- `layouts/` - Custom layout overrides (takes precedence over theme)
- `static/` - Static assets served at site root
- `assets/` - Processed assets (CSS/JS with Hugo Pipes)

## Content Frontmatter Format

```toml
+++
date = '2026-02-03T23:44:47+08:00'
draft = true
title = 'Post Title'
+++
```

## Theme Customization

Override PaperMod templates by creating matching files in `layouts/`. Theme documentation: https://github.com/adityatelange/hugo-PaperMod/wiki
