# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is an interactive Python game development course that teaches students to build a Mario-style platformer using the [Arcade library](https://api.arcade.academy/). The course content is delivered as self-contained HTML worksheets (no build system, no framework, no server required) that students open directly in a browser.

## Architecture

Every worksheet is a single `.html` file containing all CSS (inline `<style>`) and JavaScript (inline `<script>`). There are no external dependencies beyond Google Fonts CDN. No build step, bundler, or package manager is used.

### Shared design system across all worksheets

- **Dark theme**: `--bg: #0f1117`, `--surface: #181c27`, etc.
- **Typography**: Fraunces (display), Literata (body), DM Mono (code) via Google Fonts
- **CSS variables** defined in each file's `:root` block — there is no shared stylesheet
- **Noise texture overlay** on `body::before` using inline SVG data URI

### File layout

- `index.html` — Course hub / landing page linking to all worksheets
- `arcade-intro.html` — First worksheet: Arcade setup and first window
- `sprites-graphics.html` — Sprites and image handling
- `basics/movement-physics.html` — Keyboard input and velocity
- `platformer/part1-part6` — Sequential platformer build worksheets (parts 7-9 not yet created)
- `challenges/` — Empty; planned for debugging/tracing/quiz exercises

### Worksheet interactive patterns

Each worksheet implements its own quiz/interaction system in vanilla JS:
- Multiple-choice questions with `checkAnswer(qId, correctIndex)` pattern
- Hint reveal toggles
- Code block syntax highlighting (manual spans, no external highlighter)
- Progress tracking via `localStorage` (key format: `python-arcade-{topic}-v1`)
- Checkpoint checklists for hands-on coding tasks
- Canvas/SVG visualizations for coordinate system demos

## Conventions

- All internal links between worksheets use relative paths
- No AI tool attribution in commit messages. Specifically, do NOT add `Co-Authored-By: Claude` (or any AI/assistant) trailers, and do not include "Generated with" lines or similar. Commit messages must contain only the change description.
- Atomic commits: stage files individually or in small logical groups
- The `.vibe/` directory contains config for Vibe CLI (a separate tool) and is untracked from the course content perspective
