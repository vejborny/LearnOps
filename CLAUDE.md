# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

Static HTML/CSS website for **LearnOps** – a Czech educational agency (vzdělávací agentura) offering IT, AI, and soft-skills courses. No build tools, no JavaScript framework, no package manager.

## Running the site

Open any `.html` file directly in a browser, or serve the directory with any static file server, e.g.:

```
npx serve .
python -m http.server 8080
```

There are no build, lint, or test commands.

## File structure

| File | Purpose |
|---|---|
| `index.html` | Homepage – hero, stats bar, category cards, USPs, testimonials, contact |
| `course-1.html` | IT/AI courses subpage – filter bar, course list, upcoming dates table, sidebar |
| `course-2.html` | Soft-skills courses subpage – same layout pattern as `course-1.html` |
| `styles.css` | Single shared stylesheet for all pages |

## CSS architecture

All design tokens are CSS custom properties in `:root` at the top of `styles.css` (colors, shadows, radii, container width). Use these variables rather than hardcoding values.

Naming follows a BEM-like convention (`.block`, `.block__element`, `.block--modifier`). Each component section is delimited by a large comment block (e.g., `/* === HEADER & NAV === */`).

Responsive breakpoints: `900px` (tablet) and `680px` (mobile), both in a single `@media` block at the bottom of `styles.css`.

## Page layout pattern

All pages share an identical sticky header and footer. Course subpages follow this structure:

```
.page-header          ← blue gradient banner with breadcrumb + badges
.filter-bar           ← sticky below header (top: 62px), anchor-link filters
.container > .course-layout   ← two-column grid: main list (1fr) + .sidebar (300px)
```

The sidebar becomes `position: static` below 900px. The `.sidebar-box--cta` variant uses the primary blue background.

## Content language

All visible text is in Czech. Keep new content in Czech unless asked otherwise.

## Git workflow

Always commit and push to the **master** branch.

Use the `/push-github` skill (`.claude/commands/push-github.md`) to stage, commit, and push changes.

### Commit message convention

Format: `<type>: <short description in Czech>`

| Type | When to use |
|------|-------------|
| `feat` | New feature or content (new page, section, component) |
| `fix` | Bug fix (broken link, layout issue, typo) |
| `style` | Visual-only change (colors, spacing, fonts) |
| `refactor` | Code restructure with no behavior change |
| `content` | Text, prices, or course date updates |
| `docs` | Documentation changes (CLAUDE.md, README) |
| `chore` | Config or non-web files |

Rules: lowercase description, max 72 characters on the first line, write in Czech.
